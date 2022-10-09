# linux-automake-notes

## example_project

### Building example project
``` bash
cd example_project
autoreconf --install
./configure
make
cd ./src
./hello
```