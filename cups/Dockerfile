FROM microsoft/aspnetcore:2.0.3
MAINTAINER Shabbir Akolawala <sakolawala@webuy.com>

RUN apt-get update && apt-get install -y debian-keyring

RUN echo "deb http://archive.ubuntu.com/ubuntu xenial main \n\
deb http://archive.ubuntu.com/ubuntu xenial multiverse "\
>> /etc/apt/sources.list

RUN gpg --keyserver pgp.mit.edu --recv-keys 40976EAF437D05B5 && gpg --armor --export 40976EAF437D05B5 | apt-key add -

RUN gpg --keyserver pgp.mit.edu --recv-keys 3B4FE6ACC0B21F32 && gpg --armor --export 3B4FE6ACC0B21F32 | apt-key add -

RUN apt-get update && apt-get install -y --no-install-recommends \
    cups-client \
    cups-bsd \
    libgdiplus \
    ttf-mscorefonts-installer \
    ttf-ubuntu-font-family

EXPOSE 80
