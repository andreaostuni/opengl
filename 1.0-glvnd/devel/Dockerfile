ARG from

# Download the official headers from github.com/KhronosGroup
FROM centos:7 as khronos

RUN yum install -y \
        git && \
    rm -rf /var/cache/yum/*

RUN git clone https://github.com/KhronosGroup/OpenGL-Registry.git && cd OpenGL-Registry \
    git checkout 681c365c012ac9d3bcadd67de10af4730eb460e0 && \
    cp -r api/GL /usr/local/include

RUN git clone https://github.com/KhronosGroup/EGL-Registry.git && cd EGL-Registry \
    git checkout 0fa0d37da846998aa838ed2b784a340c28dadff3 && \
    cp -r api/EGL api/KHR /usr/local/include


FROM ${from}

RUN yum install -y \
        pkgconfig \
        libXau-devel libXau-devel.i686 \
        libXdmcp-devel libXdmcp-devel.i686 \
        libxcb-devel libxcb-devel.i686 \
        libXext-devel libXext-devel.i686 \
        libX11-devel libX11-devel.i686 && \
    rm -rf /var/cache/yum/*

COPY --from=khronos /usr/local/include /usr/local/include

ENV PKG_CONFIG_PATH /usr/local/lib64/pkgconfig:/usr/local/lib/pkgconfig

COPY usr /usr
