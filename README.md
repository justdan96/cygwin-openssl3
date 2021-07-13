# Cygwin OpenSSL 3 Dockerfile

[Docker](http://docker.com) container to build [OpenSSL v3](https://wiki.openssl.org/index.php/OpenSSL_3.0) as a Windows executable through Cygwin on Linux.

## Usage

### Install

This Dockerfile is best used with Docker BuildKit, so when you build the `cygwin-openssl3` Docker container from source, during the container's build it will create the installation and copy it to the `out` folder on the host machine. 

To create the Docker container from scratch and copy the binaries to the `out` folder in the current working directory, run the commands below:
```
git clone https://github.com/justdan96/cygwin-openssl3.git
cd cygwin-openssl3
export DOCKER_BUILDKIT=1
docker build --target export -t cygwin-openssl3 . --output out
```
