FROM ubuntu:14.04
MANTAINER Tiago A. Reul <tiagoreul@gmail.com>

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update

# Default jdk
RUN apt-get install -y default-jdk

# 32-bit dependencies of android and utils
RUN apt-get install -y \
    bison \
    git \
    gperf \
    lib32gcc1 \
    lib32bz2-1.0 \
    lib32ncurses5 \
    lib32stdc++6 \
    lib32z1 \
    libc6-i386 \
    libxml2-utils \
    make \
    zip


# Download and unzip Android Studio for Linux
ADD http://dl.google.com/dl/android/studio/ide-zips/1.2.1.1/android-studio-ide-141.1903250-linux.zip /opt/android-studio.zip
RUN cd /opt/ && unzip android-studio.zip && rm android-studio.zip

# The command to run
CMD /opt/android-studio/bin/studio.sh


