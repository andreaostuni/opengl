ARG from

# Build libglvnd
FROM centos:7 as glvnd

RUN yum install -y \
        git \
        make \
        libtool \
        gcc \
        pkgconfig \
        python \
        libXext-devel \
        libX11-devel \
        xorg-x11-proto-devel && \
    rm -rf /var/cache/yum/*

WORKDIR /opt/libglvnd
RUN git clone --branch=v1.0.0 https://github.com/NVIDIA/libglvnd.git . && \
    ./autogen.sh && \
    ./configure --prefix=/usr/local --libdir=/usr/local/lib64 && \
    make -j"$(nproc)" install-strip && \
    find /usr/local/lib64 -type f -name 'lib*.la' -delete

RUN yum install -y \
        glibc-devel.i686 \
        libgcc.i686 \
        libXext-devel.i686 \
        libX11-devel.i686 && \
    rm -rf /var/cache/yum/*

# 32-bit libraries
RUN make distclean && \
    ./autogen.sh && \
    ./configure --prefix=/usr/local --libdir=/usr/local/lib --host=i386-linux-gnu "CFLAGS=-m32" "CXXFLAGS=-m32" "LDFLAGS=-m32" && \
    make -j"$(nproc)" install-strip && \
    find /usr/local/lib -type f -name 'lib*.la' -delete


FROM ${from}
LABEL maintainer "NVIDIA CORPORATION <cudatools@nvidia.com>"

COPY --from=glvnd /usr/local/lib64 /usr/local/lib64
COPY --from=glvnd /usr/local/lib /usr/local/lib

COPY 10_nvidia.json /usr/local/share/glvnd/egl_vendor.d/10_nvidia.json

RUN echo '/usr/local/lib64' >> /etc/ld.so.conf.d/glvnd.conf && \
    echo '/usr/local/lib' >> /etc/ld.so.conf.d/glvnd.conf && \
    ldconfig && \
    echo '/usr/local/$LIB/libGL.so.1' >> /etc/ld.so.preload && \
    echo '/usr/local/$LIB/libEGL.so.1' >> /etc/ld.so.preload
