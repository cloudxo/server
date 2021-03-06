# Installation

Latest Version: **GITHUB_VERSION**

?> Before starting Screego you may read [Configuration](config.md).

## Docker

Setting up Screego with docker is pretty easy, you basically just have to start the docker container, and you are ready to go:

The [screego/server](https://hub.docker.com/r/screego/server) docker images are multi-arch docker images. 
This means the image will work for `amd64`, `i386`, `ppc64le` (power pc), `arm64`, `arm v7` (Raspberry PI).

```bash
$ docker run -p 3478:3478 -p 8080:5050 -e SCREEGO_EXTERNAL_IP=0.0.0.0 screego/server:GITHUB_VERSION
```

By default, Screego runs on port 5050.

### docker-compose.yml

```yaml
version: "3.7"
services:
  screego:
    image: screego/server:GITHUB_VERSION
    ports:
      - 8080:5050
      - 3478:3478
    environment:
      SCREEGO_EXTERNAL_IP: "0.0.0.0"
```

## Binary

### Supported Platforms:

* linux_amd64 (64bit)
* linux_i386 (32bit)
* armv7 (32bit used for Raspberry Pi)
* armv6
* arm64 (ARMv8)
* ppc64
* ppc64le
* windows_i386.exe (32bit)
* windows_amd64.exe (64bit)

Download the zip with the binary for your platform from [screego/server Releases](https://github.com/screego/server/releases).

```bash
$ wget https://github.com/screego/server/releases/download/vGITHUB_VERSION/screego_GITHUB_VERSION_{PLATFORM}.tar.gz
```

Unzip the archive.

```bash
$ tar xvf screego_GITHUB_VERSION_{PLATFORM}.tar.gz
```

Make the binary executable (linux only).

```bash
$ chmod +x screego
```

Execute screego:

```bash
$ ./screego
# on windows
$ screego.exe
```

## Arch-Linux(aur)

TODO

## Source

TODO
