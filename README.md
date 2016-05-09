# Factorio in Docker

## Prerequisites

- Docker >= 1.7.0
- Graphic card

## Containers

Base container is based on debian sid. 
Some additional libraries are downloaded for running this game.

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

That's all. I've tested this container on Linux Mint 17.3 x64.

If you will have a troubles with it, please open issue ticket. 

Thanks Felix.
