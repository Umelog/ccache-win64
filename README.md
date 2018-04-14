# ccache-win64

ccache binary file (executable file) for 64bit Windows.

## what's ccache ?

ccache is a compiler cache. It speeds up recompilation by caching the result of previous compilations and detecting when the same compilation is being done again. Supported languages are C, C++, Objective-C and Objective-C++.

* [Official web site](https://ccache.samba.org)
* [Official Documentation](https://ccache.samba.org/documentation.html)
* [License and copyright](https://ccache.samba.org/license.html)

## How to install ccache for win64 ?

Just download ccache.exe and zlib1.dll, and set PATH to these files.

## How to use ?


For example, if you use gcc manually, what you need to is prepend ccache.

```
ccache gcc foo.c -c -o foo.o

```

If you use Makefile, you should change pattern rule like following sample code.

```
%.o : %.c
	ccache $(CC) $(CFLAGS) -c $< -o $*.o

```
If you need more detail, see [Official Documentation](https://ccache.samba.org/documentation.html).
