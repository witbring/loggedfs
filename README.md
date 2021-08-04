# LoggedFS - Filesystem monitoring with Fuse

## dependency
```bash
sudo apt-get install libfuse-dev libpcre3-dev libxml2-dev xml2-config
```

## build
```bash
$ make
```bash

## launch file system
```bash
$ sudo ./loggedfs -f -p [absolute\_path]
```

## now rock & roll
```bash
$ cd [absolute\_path]
$ echo '#include<stdio.h>\nint main(){printf("hello world\\n");return 0;}' > hello.c
$ gcc --save-temps hello.c -o hello
$ ls
hello hello.c  hello.i  hello.o  hello.s
$ gcc --save-temps hello.c
$ ls
backup  hello  hello.c  hello.i  hello.o  hello.s
$ ls backup
hello\_0.s
```
