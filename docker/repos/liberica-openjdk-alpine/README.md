# What is Liberica?

Liberica is a 100% open-source Java implementation.
It is built from OpenJDK which BellSoft contributes to, is thoroughly
tested and passed the JCK provided under the license from OpenJDK.
Liberica supports the following architectures: x86_64, ARMv8, ARMv7
Liberica binaries for the Raspberry Pi also contain JavaFX with hardware-accelerated EGL support and Device IO API as additional modules.

Liberica is built, tested, supported and made available by BellSoft.

https://bell-sw.com/java.html

This repository contain Alpine Docker images of Liberica OpenJDK and available for following architectures:
* x86_64 (aka amd64)
* aarch64 (i.e. ARM64)
* armhf (for devices like Raspberry Pi 2/3)

# Tags

The Liberica repository bellsoft/liberica-openjdk-alpine provides multiple tagged images. The latest Liberica versions are:
* [`latest`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/13/Dockerfile),
[`13.0.2-9`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/13/Dockerfile),
[`13.0.1`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/13.0.1/Dockerfile)
[`13`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/13.0.0/Dockerfile)
* [`12.0.2`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/12.0.2/Dockerfile),
[`12.0.1`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/12.0.1/Dockerfile),
[`12`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/12.0.0/Dockerfile)
* [`11.0.6-10`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/11/Dockerfile),
[`11.0.5-11`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/11.0.5/Dockerfile),
[`11.0.5`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/11.0.5/Dockerfile),
[`11.0.4`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/11.0.4/Dockerfile),
[`11.0.3`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/11.0.3/Dockerfile),
[`11.0.2`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/11.0.2/Dockerfile),
[`11.0.1`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/11.0.1/Dockerfile),
[`11`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/11.0.0/Dockerfile)
* [`10.0.2`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/10.0.2/Dockerfile)
* [`10.0.1`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/10.0.1/Dockerfile)
[`10`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/10.0.0/Dockerfile) - armhf only (Raspberry Pi 2/3)
* [`9.0.4`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/9.0.4/Dockerfile),
[`9.0.1`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/9.0.1/Dockerfile) - armhf only (Raspberry Pi 2/3)
* [`8u`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/8/Dockerfile),
[`8u242-7`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/8/Dockerfile),
[`8u232-10`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/8u232/Dockerfile),
[`8u232`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/8u232/Dockerfile),
[`8u222`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/8u222/Dockerfile),
[`8u212`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/8u212/Dockerfile),
[`8u202`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/8u202/Dockerfile),
[`8u192`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/old/8u192/Dockerfile),
[`8`](https://github.com/bell-sw/Liberica/blob/master/docker/repos/liberica-openjdk-alpine/8/Dockerfile)   - amd64 and aarch64 only

# Build

Dockerfile accepts the following parameters:

`LANG` – Specifies a `locale` for this image. By default it's set to en_US.UTF-8, for locale names see https://www.gnu.org/software/gettext/manual/html_node/Locale-Names.html#Locale-Names. Note that the specified locale cannot be changed in runtime. 

# Usage

For example, you can run a Liberica OpenJDK 11 container with the following command:

 `docker run -it --rm bellsoft/liberica-openjdk-alpine:11 java -version`

To run some application you can create Dockerfile, based on bellsoft/liberica-openjdk-alpine image or mount volume with your code/applicaiton, for example:

 `docker run -it --rm  -v /home/user/project/:/data bellsoft/liberica-openjdk-alpine:11 java -jar /data/MyApp.jar`
