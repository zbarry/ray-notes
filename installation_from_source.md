# Installing / compiling Ray from source

Only tested this on Linux.

## CMake old version

On CentOS 7, `cmake` version is 2. Ray needs 3.

`sudo yum install cmake`

`mkdir ~/bin`

`ln -s /usr/bin/cmake3 ~/bin/cmake`

add `~/bin` to your path in `~/.bashrc`.
