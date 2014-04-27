Sample Automake Flow
====================

Basic Flow
----------

0.  Prepare automake (i.e. brew install automake)
1.  Move sorces to /src directory
2.  Add Makefile.am
3.  autoscan
4.  mv configure.scan configure.ac
5.  Add AM_INIT_AUTOMAKE line to configure.ac
6.  autoheader
7.  aclocal
8.  Make required files (i.e. touch NEWS README AUTHORS ChangeLog)
9.  automake --add-missing
10. autoconf
11. ./configure
12. make
13. src/hello


Sample Makefile.am
------------------

Makefile.am
```
SUBDIRS = src
```

src/Makefile.am
```
bin_PROGRAMS = hello
hello_SOURCES = hello.cc hello.h main.cc
```


REFERENCES
----------

- http://www.02.246.ne.jp/~torutk/cxx/automake/automake.html
- http://www.jaist.ac.jp/~kiyoshiy/memo/autoconf.html
- https://www.sourceware.org/autobook/autobook/autobook_25.html
- https://developer.gnome.org/anjuta-build-tutorial/stable/create-autotools.html.en
