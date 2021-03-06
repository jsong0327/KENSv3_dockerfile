# KENSv3 Environment Dockerfile

Dockerfile to quickly setup KENS environment


## Getting Started

Let's set up the environment.
This was tested on Mac OS X and Ubuntu, 
but steps should be similar in other OSes (ex Windows)

### Prerequisites

- Docker
- KENSv3 (either cloned from KENSv3 github page or KENSv3 you are working on)


### Setting up the environment
- Build docker image
```
$ git clone https://github.com/jsong0327/KENSv3_dockerfile.git
$ cd KENSv3_dockerfile
$ docker build -t kens .
```

### Run docker image and generate a container (remove '-it' to run container in background)
```
$ docker run -it --rm -v PATH/TO/KENSv3/FOLDER:/KENSv3 -u $(id -u ${USER}):$(id -g ${USER}) --name kens_container kens
```

## Access running container
```
$ docker exec -it kens_container /bin/bash
```

### Happy Coding!
