<h1 align=center>Dockette / Factorio</h1>

<p align=center>
   <a href="https://github.com/sponsors/f3l1x"><img src="https://img.shields.io/badge/sponsor-GitHub%20Sponsors-ea4aaa" alt="GitHub Sponsors"></a>
   <a href="https://github.com/orgs/dockette/discussions"><img src="https://img.shields.io/badge/support-discussions-6f42c1" alt="Support/Discussions"></a>
</p>

<p align=center>
   🎁 Factorio desktop game in Docker
</p>

-----

> [!WARNING]
> **Deprecated.** These Dockerfiles are no longer maintained, and the repository is archived. They target Factorio
> 0.12.x (2016) on `debian:sid` via the `dockergames/factorio` base image, which is not published on Docker Hub. For a
> maintained Factorio image, use [`factoriotools/factorio`](https://hub.docker.com/r/factoriotools/factorio) (dedicated server).

Dockerfiles and a launcher script for running the Factorio desktop game (X11, needs a graphics card) in Docker. The
base image is built on `debian:sid` with the libraries the game needs. Versions `0.12.33` and `0.12.35` live in
`linux/x64`, and `sources` runs an existing Factorio directory.

## Usage

```sh
# download the startup script
wget https://raw.githubusercontent.com/dockergames/factorio/master/bin/run -O factorio

# run it and see usage
sh factorio
```

```
Usage: run [-p | -s | -t] <folder> [-h]

  -h            Display this help and exit.
  -p <folder>   Portable mode. Folder points to your custom data dir.
  -s <folder>   Sources mode. Folder points to factorio root dir.
  -t            Temporary mode (no volumes).
```

- **Portable** downloads a fresh installation of the game and keeps its data in the given folder.
- **Sources** uses a Factorio game you already have downloaded.
- **Temporary** starts the game once, nothing is stored after exit.

Requires Docker >= 1.7.0. To run an X server in a container, see the [ROS GUI tutorial](http://wiki.ros.org/docker/Tutorials/GUI).

## Maintenance

See [how to contribute](https://github.com/dockette/.github/blob/master/CONTRIBUTING.md) to this package. Consider to
[support](https://github.com/sponsors/f3l1x) **f3l1x**. Thank you for using this package.
