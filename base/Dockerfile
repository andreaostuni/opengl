ARG from

FROM ${from}
LABEL maintainer "NVIDIA CORPORATION <cudatools@nvidia.com>"

RUN yum upgrade -y && yum install -y \
        libXau libXau.i686 \
        libXdmcp libXdmcp.i686 \
        libxcb libxcb.i686 \
        libXext libXext.i686 \
        libX11 libX11.i686 && \
    rm -rf /var/cache/yum/*

# nvidia-container-runtime
ENV NVIDIA_VISIBLE_DEVICES \
        ${NVIDIA_VISIBLE_DEVICES:-all}
ENV NVIDIA_DRIVER_CAPABILITIES \
        ${NVIDIA_DRIVER_CAPABILITIES:+$NVIDIA_DRIVER_CAPABILITIES,}graphics

# nvidia-docker v1
RUN echo "/usr/local/nvidia/lib" >> /etc/ld.so.conf.d/nvidia.conf && \
    echo "/usr/local/nvidia/lib64" >> /etc/ld.so.conf.d/nvidia.conf

# Required for non-glvnd setups.
ENV LD_LIBRARY_PATH /usr/local/nvidia/lib:/usr/local/nvidia/lib64

# Required for non-glvnd setups.
RUN echo '/usr/$LIB/libGL.so.1' > /etc/ld.so.preload && \
    echo '/usr/$LIB/libEGL.so.1' >> /etc/ld.so.preload

# ld.so will print errors when this statement is executed, this is normal.
ONBUILD RUN rm /etc/ld.so.preload
