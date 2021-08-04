# LoggedFS - Filesystem monitoring with Fuse

## dependency
```bash
sudo apt-get install libfuse-dev libpcre3-dev libxml2-dev
```

## build
```bash
$ make
```

## launch file system
```bash
$ sudo ./loggedfs -f -p [absolute_path]
```

## Use case #1
```bash
$ cd [absolute_path]
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

### Use case #2
```bash
$ sudo ./loggedfs -f -p /home/user/project/binutils-2.31.1
```

```
$ cd /home/user/project/binutils-2.31.1/x64/clang/pie/o0-bfd/
$ make clean; make
```



