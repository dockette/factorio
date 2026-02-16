# Factorio in Docker

See [dockergames/factorio](https://hub.docker.com/r/dockergames/factorio/) on Docker Hub.

![Factorio in Docker container](https://raw.githubusercontent.com/whaleapps/factorio/master/docs/factorio.png)

## Prerequisites

- Docker >= 1.7.0
- Graphic card

## Containers

Base container is based on debian sid. 
Some additional libraries are downloaded for running this game.

## Prolog

Here you can find more information about how to run X server in docker containers.

http://wiki.ros.org/docker/Tutorials/GUI

## Install

```sh
# download startup script
wget https://raw.githubusercontent.com/dockergames/factorio/master/bin/run -O factorio 

# run script 
sh factorio

# and see usage..
```

## Usage

This repo contains a starter bash script, which is located in **/bin** folder.

```sh
Usage: run [-p | -s | -t] <folder> [-h]

Run factorio in isolated docker container.

Options:

  -h            Display this help and exit.
  -p <folder>   Portable mode. Folder points to your custom data dir.
  -s <folder>   Sources mode. Folder points to factorio root dir.
  -t            Temporary mode (no volumes).
```

### Portable mode

If you want to download a fresh installation of game a just started. 
You should pick this mode.

### Sources mode

If you have your factorio game already downloaded. Just pick this mode.

### Temporary mode

Just start game one-time. There will be no stored data after exit. 

-----

That's all. I've tested this container on multipl linux machines.

- Linux Mint 17.3 [x64]
- Linux Mint 18 [x64]
- Ubuntu 14.04 LTS [x64]
- Ubuntu 15.10 [x64]

If you will have a troubles with it, please open issue ticket. 

Thanks Felix.

## Maintenance

See [how to contribute](https://github.com/dockette/.github/blob/master/CONTRIBUTING.md) to this package. Consider to [support](https://github.com/sponsors/f3l1x) **f3l1x**. Thank you for using this package.
