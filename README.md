Usage Info
==========

Example Usage (use image)
-------------------------

```shell
# create new VM (optional)
$ docker-machine create -d virtualbox YoutubeDL

# list VM`s (optional)
$ docker-machine ls

# pointing shell (optional)
$ eval $(docker-machine env YoutubeDL)

# pull from DockerHub (optional)
$ docker pull slorenz/youtubedl

# create new directory
$ mkdir mp3

# run container
$ docker run --rm -v /root/mp3:/mp3 slorenz/youtubedl --no-check-certificate --extract-audio --audio-format mp3 -o "%(title)s.%(ext)s" <url>
```