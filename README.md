# Introducation
This docker file loads a default instalation of rocq with the coq compatibility layer.  

# Setting up Docker
If you are running Windows or OSX, you should start by downloading docker desktop here:

[https://www.docker.com/products/docker-desktop/](https://www.docker.com/products/docker-desktop/)

For docker desktop, you will need to start it in order to build and run docker images.

Under linux, either docker or podman should work.  The versions of linux that I have run have had both installed by default.

# Building the image
    
## to build:
Go to the directory that has the dockerfile.rocq in it.

```
    docker build -f dockerfile.rocq -t rocq .
```

## To Run:
### On OSX:
Go to the directory that has the logical foundations directories.
```
    docker run --rm -it --entrypoint bash -v `pwd`:/home/opam/src rocq
```
Note: -v mounts the directory 'pwd' in the container under the directory /home/opam/src

### On Windows
Go to the directory that has the logical foundations directories.
```
    docker run --rm -it --entrypoint bash -v <your directory here>:/home/opam/src rocq
```
Note: on windows there is no pwd command, so you have to copy the directory in the command (Like ... -v C:\home\users\rob\sf:/home/opam/src ...)

## docker-compose up
```
```

## to run from commandline
```
     % env $(opam env)
```

## Building project from commandline - this will need to be done when you complete a section:
```
   % make coqMakefile
   % make build
```
# Setting up and running rocq through VS Code
## download the modules required for docker/rocq
1) VsRocq
2) Coq Elpi Lang (probably not needed)
3) Docker (not really needed)

## connect to the running container:

1) click on the box with >< in the lower left corner to connect with a remote container
2) from the dropdown select the option to connect to a running container
3) select the running container to connect to.
4) install VsRocq into the running container
5) open the .v file (like basics.v).  The code should be highlighted.
6) You should be able to step through the file.

