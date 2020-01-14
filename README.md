# llvm-docker
LLVM development docker container on Linux
- ubuntu 16.04
- LLVM 9

```shell
$ mkdir workspace
$ docker build -t llvm .
# sync host workspace and container workspace
$ docker run -it --rm -v $(pwd)/workspace:/root/workspace llvm

# for local development
$ sudo ln -s /home/ubuntu/llvm-docker/llvm-9/llvm /usr/include/llvm
$ sudo ln -s /home/ubuntu/llvm-docker/llvm-c-9/llvm-c /usr/include/llvm-c
```
