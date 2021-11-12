# tetgen

Mirror of the latest stable version of `tetgen`. 

https://wias-berlin.de/software/tetgen/

### Compiling tetgen on Linux/Mac

Follow the [compilation instructions](https://wias-berlin.de/software/tetgen/1.5/doc/manual/manual004.html#sec%3Acompile).

### Compiling tetgen on Windows

1. Install MinGW using [MSYS2](https://www.msys2.org/)

2. Follow the installation instructions!

   -  Install/update packages:

          pacman -Syu

   -  Install development toolchain:

          pacman -S –needed base-devel mingw-w64-x86_64-toolchain

3. Add `C:\msys64\mingw64\bin` to the Windows Path environment
   variable. Click [here](https://code.visualstudio.com/docs/languages/cpp#_add-the-mingw-compiler-to-your-path) for info.

4. Compiling/installing tetgen:

   -  Compilation steps:

          g++ -O0 -c predicates.cxx 
          g++ -O3 -o tetgen tetgen.cxx predicates.o -lm

   -  Move `tetgen.exe` to a location on your system path

### Pushing a new release

If the code is updated, a new release will be created automatically when a tag is pushed:

    git tag 1.x.y
    git push origin 1.x.y

This will trigger the github actions to build/upload the binaries for `tetgen`.
