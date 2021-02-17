# Streaming-service

This is a collection of docker containers to run an easy to deploy streaming site. I used this to provide stream an event during the pandemic. It constist of a nginx with rtmp support and two normal nginx to serve the video content (hls stream).

## How to run this service

### What type of server

To run this service you would at least need three machines. On needs more power than the others because it serves as ingest and transcoding server, the other two can have less power because they only distribute the video feed.

### Edit configs to your needs

You only need to change the ninx.conf for your needs. 

### Running

Copy the cache dir on to the machines dedicated to serve the content and the ingest server on the other machine.