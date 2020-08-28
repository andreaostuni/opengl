**Requires nvidia-docker 2.0**

- Leverages https://github.com/NVIDIA/libglvnd
- Display (e.g. X11, Wayland) is not officially supported.
- GPU isolation requires driver 390+.

Example Dockerfiles: https://gitlab.com/nvidia/samples/tree/master/opengl

## Tags

OpenGL images come in three flavors:

* ```base```: for legacy NVIDIA drivers that do not use libglvnd.
* ```1.0-glvnd-runtime```: uses libglvnd for properly dispatching OpenGL API calls to the NVIDIA libraries.
  Use this image if you have a pre-built application.
* ```1.0-glvnd-devel```: extends the `glvnd-runtime` image by adding the official Khronos headers.
  Use this image to compile an OpenGL application from sources.

## Ubuntu 18.04 [![build status](https://gitlab.com/nvidia/container-images/opengl/badges/ubuntu18.04/pipeline.svg)](https://gitlab.com/nvidia/container-images/opengl/commits/ubuntu18.04)

- [`base-ubuntu18.04` (*base/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu18.04/base/Dockerfile)
- [`1.0-glvnd-runtime-ubuntu18.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu18.04/glvnd/runtime/Dockerfile)
- [`1.0-glvnd-devel-ubuntu18.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu18.04/glvnd/devel/Dockerfile)

## Ubuntu 16.04 [![build status](https://gitlab.com/nvidia/container-images/opengl/badges/ubuntu16.04/pipeline.svg)](https://gitlab.com/nvidia/container-images/opengl/commits/ubuntu16.04)

- [`base`, `base-ubuntu16.04` (*base/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/base/Dockerfile)
- [`1.1-glvnd-runtime`, `runtime`, `1.1-glvnd-runtime-ubuntu16.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/glvnd/runtime/Dockerfile)
- [`1.1-glvnd-devel`, `devel`, `1.1-glvnd-devel-ubuntu16.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/glvnd/devel/Dockerfile)
- [`1.0-glvnd-runtime`, `runtime`, `1.0-glvnd-runtime-ubuntu16.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/glvnd/runtime/Dockerfile)
- [`1.0-glvnd-devel`, `devel`, `1.0-glvnd-devel-ubuntu16.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/glvnd/devel/Dockerfile)

## Ubuntu 14.04 [![build status](https://gitlab.com/nvidia/container-images/opengl/badges/ubuntu14.04/pipeline.svg)](https://gitlab.com/nvidia/container-images/opengl/commits/ubuntu14.04)

- [`base-ubuntu14.04` (*base/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu14.04/base/Dockerfile)
- [`1.1-glvnd-runtime-ubuntu14.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu14.04/glvnd/runtime/Dockerfile)
- [`1.1-glvnd-devel-ubuntu14.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu14.04/glvnd/devel/Dockerfile)
- [`1.0-glvnd-runtime-ubuntu14.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu14.04/glvnd/runtime/Dockerfile)
- [`1.0-glvnd-devel-ubuntu14.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu14.04/glvnd/devel/Dockerfile)

## CentOS 7 [![build status](https://gitlab.com/nvidia/container-images/opengl/badges/centos7/pipeline.svg)](https://gitlab.com/nvidia/container-images/opengl/commits/centos7)

- [`base-centos7` (*base/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos7/base/Dockerfile)
- [`1.1-glvnd-runtime-centos7` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos7/glvnd/runtime/Dockerfile)
- [`1.1-glvnd-devel-centos7` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos7/glvnd/devel/Dockerfile)
- [`1.0-glvnd-runtime-centos7` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos7/glvnd/runtime/Dockerfile)
- [`1.0-glvnd-devel-centos7` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/centos7/glvnd/devel/Dockerfile)
