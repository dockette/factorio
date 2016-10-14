FROM dockergames/factorio:base

# Author
MAINTAINER Milan Sulc <sulcmil@gmail.com>

# Variables
ENV FACTORIO_VERSION=sources
ENV FACTORIO_BIN=$FACTORIO_HOME/bin/x64/factorio

# Change user
USER $FACTORIO_USER

# Volumes
VOLUME $FACTORIO_HOME

# Run factorio
ENTRYPOINT $FACTORIO_BIN
