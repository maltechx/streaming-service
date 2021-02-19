# Streaming-service

This is a collection of docker containers to run an easy to deploy streaming site. I used this to provide a livestream for an event during the pandemic. It consist of a nginx with rtmp support and two normal nginx to act as caching server. They reduced the network load on the main (ingest) server.

## How to run this service

### What type of server

To run this service you would at least need three machines. On needs more power than the others because it serves as ingest and transcoding server, the other two can have less power because they only distribute the video feed.

### Edit configs

You only need to change the nginx.conf for your needs. 

### Running

This uses docker to run the nginx services, so you should have docker and docker-compose already installed.
First clone the repo on all servers. On the ingest server cd into `ingest` and on the caching server into `cache`. Now edit the nginx.conf to your needs, maybe add certificates and start the docker container with `docker-compose up -d`. 