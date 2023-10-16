# CodeSandbox supports debian & ubuntu based images
FROM ubuntu:latest

# Example; install htop by default
RUN apt update -y && apt install -y libappindicator-dev

RUN curl -fsSl https://downloads.ortussolutions.com/debs/gpg | gpg --dearmor | tee /usr/share/keyrings/ortussolutions.gpg > /dev/null
RUN echo "deb [signed-by=/usr/share/keyrings/ortussolutions.gpg] https://downloads.ortussolutions.com/debs/noarch /" | tee /etc/apt/sources.list.d/commandbox.list
RUN apt update -y && apt install -y apt-transport-https

RUN apt update -y && apt install -y commandbox
RUN apt install -y openjdk-11-jdk


# The project will be mounted in /workspace by default

# Every new shell will open inside the built container

# On top of this build, we install `zsh`, `git` and `docker` as additional
# Docker layers.

