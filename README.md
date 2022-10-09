# linux-automake-notes

## example_project

### Building the example_project
``` bash
cd example_project
autoreconf --install
./configure
make
cd ./src
./hello
```

## configure.ac notes
This file is M4 macros file that used to configure both autoconf and automake.  

Here is configure.ac content from the example project:  
``` M4
AC_INIT([amhello], [1.0], [bug-automake@gnu.org])
AM_INIT_AUTOMAKE([-Wall -Werror foreign])
AC_PROG_CC
AC_CONFIG_HEADERS([config.h])
AC_CONFIG_FILES([
Makefile
src/Makefile
])
AC_OUTPUT
```

`AC_` macros configure autoconfig, while `AM_`  macros  
configure the automake.  
