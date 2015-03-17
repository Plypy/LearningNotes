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
