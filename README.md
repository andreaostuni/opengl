**Requires nvidia-docker 2.0**

- Leverages https://github.com/NVIDIA/libglvnd
- Display (e.g. X11, Wayland) is not officially supported.
- GPU isolation requires driver 390+.

Example Dockerfiles: https://gitlab.com/nvidia/samples/tree/master/opengl

## Tags

OpenGL images come in three flavors:

* ```base```: for legacy NVIDIA drivers that do not use libglvnd.
* ```<version>-glvnd-runtime```: uses libglvnd for properly dispatching OpenGL API calls to the NVIDIA libraries.
  Use this image if you have a pre-built application.
* ```<version>-glvnd-devel```: extends the `glvnd-runtime` image by adding the official Khronos headers.
  Use this image to compile an OpenGL application from sources.

# Ubuntu 20.04

- [`base`, `base-ubuntu20.04` (*base/Dockerfile*)](https://gitlab.com/container-images/opengl/blob/ubuntu20.04/base/Dockerfile)
- [`1.0-glvnd-runtime`, `1.0-glvnd-runtime-ubuntu20.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu20.04/glvnd/runtime/Dockerfile)
- [`1.0-glvnd-devel`, `1.0-glvnd-devel-ubuntu20.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu20.04/glvnd/devel/Dockerfile)
- [`1.1-glvnd-runtime`, `1.1-glvnd-runtime-ubuntu20.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu20.04/glvnd/runtime/Dockerfile)
- [`1.1-glvnd-devel`, `1.1-glvnd-devel-ubuntu20.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu20.04/glvnd/devel/Dockerfile)
- [`1.2-glvnd-runtime`, `1.2-glvnd-runtime-ubuntu20.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu20.04/glvnd/runtime/Dockerfile)
- [`1.2-glvnd-devel`, `1.2-glvnd-devel-ubuntu20.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu20.04/glvnd/devel/Dockerfile)

## Ubuntu 18.04

- [`base-ubuntu18.04` (*base/Dockerfile*)](https://gitlab.com/container-images/opengl/blob/ubuntu18.04/base/Dockerfile)
- [`1.0-glvnd-runtime-ubuntu18.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu18.04/glvnd/runtime/Dockerfile)
- [`1.0-glvnd-devel-ubuntu18.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu18.04/glvnd/devel/Dockerfile)
- [`1.1-glvnd-runtime-ubuntu18.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu18.04/glvnd/runtime/Dockerfile)
- [`1.1-glvnd-devel-ubuntu18.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu18.04/glvnd/devel/Dockerfile)
- [`1.2-glvnd-runtime-ubuntu18.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu18.04/glvnd/runtime/Dockerfile)
- [`1.2-glvnd-devel-ubuntu18.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu18.04/glvnd/devel/Dockerfile)

## Ubuntu 16.04

- [`base-ubuntu16.04` (*base/Dockerfile*)](https://gitlab.com/container-images/opengl/blob/ubuntu16.04/base/Dockerfile)
- [`1.0-glvnd-runtime-ubuntu16.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/glvnd/runtime/Dockerfile)
- [`1.0-glvnd-devel-ubuntu16.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/glvnd/devel/Dockerfile)
- [`1.1-glvnd-runtime-ubuntu16.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/glvnd/runtime/Dockerfile)
- [`1.1-glvnd-devel-ubuntu16.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/glvnd/devel/Dockerfile)
- [`1.2-glvnd-runtime-ubuntu16.04` (*glvnd/runtime/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/glvnd/runtime/Dockerfile)
- [`1.2-glvnd-devel-ubuntu16.04` (*glvnd/devel/Dockerfile*)](https://gitlab.com/nvidia/container-images/opengl/blob/ubuntu16.04/glvnd/devel/Dockerfile)

## Centos 8 and 7

Release is currently impacted by a known CVE detected in the upstream base images:

```
vulnerabilities package HIGH Vulnerability found in os package type (rpm) - libX11 (CVE-2020-14363 - https://access.redhat.com/security/cve/CVE-2020-14363) stop
vulnerabilities package HIGH Vulnerability found in os package type (rpm) - libX11-common (CVE-2020-14363 - https://access.redhat.com/security/cve/CVE-2020-14363) stop
```

Images will be released as soon as this package is fixed upstream.
