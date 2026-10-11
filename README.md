# Birthright: The Gorgon's Alliance

## Building on Linux

Install CMake 3.10 or later, a C/C++ compiler, and the SDL2 development
libraries. Then, from the repository root, configure and build the game:

```sh
cmake -S src -B build-linux -DCMAKE_BUILD_TYPE=Release
cmake --build build-linux --parallel
```

The executable is created at `build-linux/Birthrt`.

## Extracting the game data

The game needs the original data files to run. With the Birthright ZIP file in
the repository root and the `7z` command installed, extract the ISO and then
extract the ISO contents:

```sh
7z x -oBirthright-The-Gorgons-Alliance_Win_EN_ISO-Version \
  Birthright-The-Gorgons-Alliance_Win_EN_ISO-Version.zip
7z x -oBirthright-The-Gorgons-Alliance_Win_EN_ISO-Version/disc_contents \
  "Birthright-The-Gorgons-Alliance_Win_EN_ISO-Version/Birthright - The Gorgon's Alliance.iso"
```

This creates `Birthright-The-Gorgons-Alliance_Win_EN_ISO-Version/disc_contents`,
which contains `BRSETUP.CFG` and the game data. From the repository root, run:

```sh
(cd assets/disc_contents && ../../build-linux/Birthrt)
```

Note: audio doesn't work inside the devcontainer.  Copy assets and build outside and run.