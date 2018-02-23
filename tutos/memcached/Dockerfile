# Memcached
#
# VERSION	1.0

# use the ubuntu base image provided by dotCloud
FROM ubuntu

MAINTAINER Thibaud R. strackam@gmail.com

# make sure the repository is up to date
RUN echo "deb http://archive.ubuntu.com/ubuntu precise main universe" > /etc/apt/sources.list
RUN apt-get update

# install memcached
RUN apt-get install -yq memcached

# Launch memcached when launching the container
ENTRYPOINT ["memcached"]

# run memcached as the daemon user
USER daemon

# expose memcached port
EXPOSE 11211
