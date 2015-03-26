##Using gdb to debug nginx
If we want to use gdb for debugging, the first thing we need is to compile the
nginx with debugging symbols. For GCC, we need to add build flags `-g`,
furthermore we'd better turn off the optimization to make things easier.
Hence,
```sh
export CFLAGS="g -O0"
./configure
```
The `CFLAGS` is used to dictate the compilers, GCC in our case.

##Configuration files
The configurations consists simple directives and block directives.
Simple directives use spaces as delimiter and ended with semicolons.
Block directives is like a block statement in C, they are composed of other
simple directives or block directives. They looks like this
```
http {
    server {
    }
}
```
