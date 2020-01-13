# llvm-docker
```shell
$ mkdir workspace
$ ls workspace
main.cpp

$ docker build -t llvm .
$ docker run -it --rm -v $(pwd)/workspace:/root/workspace llvm
$ docker run -it --rm -v $(pwd)/workspace:/root/workspace llvm sh -c 'clang++ -std=c++11 $(llvm-config --system-libs --cppflags --ldflags --libs core) main.cpp'

$ ls workspace
a.out*  main.cpp
```
