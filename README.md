# Docker Introduction
[docker_try](https://github.com/jin237/docker_try) is the repository for Docker Introduction.
<br>


### Refereces
- [Docker超入門①〜Dockerってなに？〜【初心者向け】<br>https://datawokagaku.com/whatisdocker/](https://datawokagaku.com/whatisdocker/)
- [Docker超入門②〜Dockerってなに？〜【初心者向け】<br>https://datawokagaku.com/startdocker/](https://datawokagaku.com/startdocker/)
- [Docker超入門③〜Dockerってなに？〜【初心者向け】<br>https://datawokagaku.com/howtouse_container/](https://datawokagaku.com/howtouse_container/)
- [Docker超入門④〜Dockerってなに？〜【初心者向け】<br>https://datawokagaku.com/container_commit_upload/](https://datawokagaku.com/container_commit_upload/)
- [Docker超入門⑤〜Dockerってなに？〜【初心者向け】<br>https://datawokagaku.com/howtousedockerfile/](https://datawokagaku.com/howtousedockerfile/)
- [Docker超入門⑥〜Dockerってなに？〜【初心者向け】<br>https://datawokagaku.com/dockerbasicflow/](https://datawokagaku.com/dockerbasicflow/)
- [Docker超入門⑦〜Dockerってなに？〜【初心者向け】<br>https://datawokagaku.com/dockerfile_commands/](https://datawokagaku.com/dockerfile_commands/)
<br>


### Memo & Note

Each terminal command charts

```terminal
// Login docker hub
$ docker login

// Pull to docker
$ docker pull {IMAGE_NAME:TAG_NAME}

// List in dicker hub
$ docker images 

// run
$ docker run {IMAGE_NAME}

// Authentication Container
$ docker ps -a

// Entering the container without leaving the container
// = Create a container from an image and put it inside. And run
$ docker run -it {IMAGE名:TAG名} bash
```







