**Requires nvidia-docker 2.0**

- Leverages https://github.com/NVIDIA/libglvnd
- Display (e.g. X11, Wayland) is not officially supported.
- GPU isolation requires driver 390+.

Example Dockerfiles: https://gitlab.com/nvidia/samples/tree/master/opengl

## End User License Agreements

The images are governed by the following NVIDIA End User License Agreements. By pulling and using the NVIDIA OpenGL container images, you accept the terms and conditions of these licenses.

Since the images may include components licensed under open-source licenses such as GPL, the sources for these components are archived [here](https://developer.download.nvidia.com/compute/cuda/opensource/image).

### NVIDIA Deep learning Container License

To view the NVIDIA Deep Learning Container license, click [here](https://developer.nvidia.com/ngc/nvidia-deep-learning-container-license)

## Tags

OpenGL images come in three flavors:

* ```base```: for legacy NVIDIA drivers that do not use libglvnd.
* ```<version>-glvnd-runtime```: uses libglvnd for properly dispatching OpenGL API calls to the NVIDIA libraries.
  Use this image if you have a pre-built application.
* ```<version>-glvnd-devel```: extends the `glvnd-runtime` image by adding the official Khronos headers.
  Use this image to compile an OpenGL application from sources.

## Ubuntu 20.04

- [`base`, `base-ubuntu20.04` (*base/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu20.04/base/Dockerfile)
- [`1.0-glvnd-runtime`, `1.0-glvnd-runtime-ubuntu20.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu20.04/glvnd/runtime/Dockerfile)
- [`1.0-glvnd-devel`, `1.0-glvnd-devel-ubuntu20.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu20.04/glvnd/devel/Dockerfile)
- [`1.1-glvnd-runtime`, `1.1-glvnd-runtime-ubuntu20.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu20.04/glvnd/runtime/Dockerfile)
- [`1.1-glvnd-devel`, `1.1-glvnd-devel-ubuntu20.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu20.04/glvnd/devel/Dockerfile)
- [`1.2-glvnd-runtime`, `1.2-glvnd-runtime-ubuntu20.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu20.04/glvnd/runtime/Dockerfile)
- [`1.2-glvnd-devel`, `1.2-glvnd-devel-ubuntu20.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu20.04/glvnd/devel/Dockerfile)

## Ubuntu 18.04

- [`base-ubuntu18.04` (*base/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu18.04/base/Dockerfile)
- [`1.0-glvnd-runtime-ubuntu18.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu18.04/glvnd/runtime/Dockerfile)
- [`1.0-glvnd-devel-ubuntu18.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu18.04/glvnd/devel/Dockerfile)
- [`1.1-glvnd-runtime-ubuntu18.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu18.04/glvnd/runtime/Dockerfile)
- [`1.1-glvnd-devel-ubuntu18.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu18.04/glvnd/devel/Dockerfile)
- [`1.2-glvnd-runtime-ubuntu18.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu18.04/glvnd/runtime/Dockerfile)
- [`1.2-glvnd-devel-ubuntu18.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu18.04/glvnd/devel/Dockerfile)

## Ubuntu 16.04

- [`base-ubuntu16.04` (*base/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/base/Dockerfile)
- [`1.0-glvnd-runtime-ubuntu16.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/glvnd/runtime/Dockerfile)
- [`1.0-glvnd-devel-ubuntu16.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/glvnd/devel/Dockerfile)
- [`1.1-glvnd-runtime-ubuntu16.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/glvnd/runtime/Dockerfile)
- [`1.1-glvnd-devel-ubuntu16.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/glvnd/devel/Dockerfile)
- [`1.2-glvnd-runtime-ubuntu16.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/glvnd/runtime/Dockerfile)
- [`1.2-glvnd-devel-ubuntu16.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/glvnd/devel/Dockerfile)

## Centos 8

WARNING: POSSIBLE MISSING IMAGE TAGS

The opengl image tags for centos7 and 8 may be missing or out-of-date on NGC and Docker Hub. Centos upstream images often fail security scans required by Nvidia before publishing images. Please check https://gitlab-master.nvidia.com/cuda-installer/opengl/-/issues for any security notices!

- [`base-centos8` (*base/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos8/base/Dockerfile)
- [`1.0-glvnd-runtime-centos8` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos8/glvnd/runtime/Dockerfile)
- [`1.0-glvnd-devel-centos8` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos8/glvnd/devel/Dockerfile)
- [`1.1-glvnd-runtime-centos8` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos8/glvnd/runtime/Dockerfile)
- [`1.1-glvnd-devel-centos8` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos8/glvnd/devel/Dockerfile)
- [`1.2-glvnd-runtime-centos8` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos8/glvnd/runtime/Dockerfile)
- [`1.2-glvnd-devel-centos8` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos8/glvnd/devel/Dockerfile)

## Centos 7

WARNING: POSSIBLE MISSING IMAGE TAGS

The opengl tags for centos7 and 8 may be missing or out-of-date on NGC and Docker Hub. Centos upstream images often fail security scans required by Nvidia before publishing images. Please check https://gitlab-master.nvidia.com/cuda-installer/opengl/-/issues for any security notices!

- [`base-centos7` (*base/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos7/base/Dockerfile)
- [`1.0-glvnd-runtime-centos7` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos7/glvnd/runtime/Dockerfile)
- [`1.0-glvnd-devel-centos7` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos7/glvnd/devel/Dockerfile)
- [`1.1-glvnd-runtime-centos7` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos7/glvnd/runtime/Dockerfile)
- [`1.1-glvnd-devel-centos7` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos7/glvnd/devel/Dockerfile)
- [`1.2-glvnd-runtime-centos7` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos7/glvnd/runtime/Dockerfile)
- [`1.2-glvnd-devel-centos7` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos7/glvnd/devel/Dockerfile)

## HOW TO BUILD CUSTOM IMAGES USING THE DOCKER SCRIPTS

Procedure is similar to the [CUDA Container Images](https://gitlab.com/nvidia/container-images/cuda#building-from-source).

Run this script from the cloned opengl repo parent path (making changes where necessary):

```
#/bin/bash

export IMAGE_NAME="my/nvidia/opengl"
export LIBGLVND_VERSION="1.2"

export FROM="${OS}:${OS_VERSION}"
export OS="ubuntu"
export OS_VERSION="20.04"

# Example for building unsupported debian images:
# export FROM="debian:10"
# export OS="debian"
# export OS_VERSION="10"

cp NGC-DL-CONTAINER-LICENSE base/

echo -e ">>> Building BASE Image\n"

docker build -t "${IMAGE_NAME}:base-${OS}${OS_VERSION}" --build-arg "from=${FROM}" "base/"

echo -e "\n>>> Building RUNTIME Image\n"

docker build -t "${IMAGE_NAME}:${LIBGLVND_VERSION}-runtime-${OS}${OS_VERSION}" \
             --build-arg "from=${IMAGE_NAME}:base-${OS}${OS_VERSION}" \
             --build-arg "LIBGLVND_VERSION=${LIBGLVND_VERSION}" \
             "glvnd/runtime"

echo -e "\n>>> Building DEVEL Image\n"

docker build -t "${IMAGE_NAME}:${LIBGLVND_VERSION}-devel-${OS}${OS_VERSION}" \
             --build-arg "from=${IMAGE_NAME}:${LIBGLVND_VERSION}-runtime-${OS}${OS_VERSION}" \
             "glvnd/devel"
```
