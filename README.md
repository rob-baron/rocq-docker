# Introducation
This docker file loads a default instalation of rocq with the coq compatibility layer

# to build:
```
    docker build -f dockerfile.rocq -t rocq .
```

# to run:
```
    docker run --rm -it --entrypoint bash -v `pwd`:/home/opam/src rocq
```

# docker-compose up
```
```

# to run from commandline
```
     % env $(opam env)
```

# Building project from commandline:
```
   % make coqMakefile
   % make build
```
