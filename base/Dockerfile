FROM debian:sid

# Author
MAINTAINER Milan Sulc <sulcmil@gmail.com>

# Variables
ENV FACTORIO_USER=factorio
ENV FACTORIO_HOME=/home/factorio

# Update OS	
RUN apt-get update  && \
	apt-get upgrade -y && \
	apt-get install -y wget

# Install necessary libraries
RUN apt-get install -y \
	libasound2 \
	libx11-6 \
	libxcursor1 \
	libxinerama1 \
	libxrandr2 \
	libxi6 \
	libglu1-mesa

# Add user
RUN useradd -u 1000 -ms /bin/bash $FACTORIO_USER
RUN gpasswd -a $FACTORIO_USER audio
RUN gpasswd -a $FACTORIO_USER video

# Cleanup
RUN apt-get clean && apt-get autoremove
RUN rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# Workdir
WORKDIR $FACTORIO_HOME
