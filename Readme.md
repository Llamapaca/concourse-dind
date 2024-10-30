# Minimum Example for Running Docker in Docker on Concourse

## Usage:
    - `make up`
    - `make fly'
    - `cd pipelines`
    - `make login`
    - `make set`
    - `make run`

### Output:
```
/pipelines# make run
fly -t main trigger-job -j test/dind
started test/dind #11
fly -t main watch -j test/dind
initializing
initializing check: image
selected worker: 0a570036cf84
selected worker: 0a570036cf84
INFO: found existing resource cache

selected worker: 0a570036cf84
running sh -exc dockerd >/dev/null 2>&1 < /dev/null &
sleep 15
docker run hello-world

+ sleep 15
+ dockerd
+ docker run hello-world
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
c1ec31eb5944: Pull complete Digest: sha256:d211f485f2dd1dee407a80973c8f129f00d54604d2c90732e8e320e5038a0348
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/

succeeded
```
