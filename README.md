# Birthright: The Gorgon's Alliance

## Building on Linux

Install CMake 3.10 or later, a C/C++ compiler, and the SDL2 development
libraries. Then, from the repository root, configure and build the game:

```sh
cmake -S src -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build --parallel
```

The executable is created at `build/Birthrt`. Run it from the repository root:

```sh
./build/Birthrt
```

The game requires its original data files to run; they are not included here.