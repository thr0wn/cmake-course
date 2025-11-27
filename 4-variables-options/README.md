[![](https://img.shields.io/badge/c++-black?logo=c++&style=for-the-badge)](https://learnxinyminutes.com/c++/)
[![](https://img.shields.io/badge/cmake-black?logo=cmake&style=for-the-badge)](https://cmake.org/)

## Variables and options
Project with subdirectories, multiples targets, variables and options. Specifically, there is the option COMPILE_EXECUTABLE to compile or not the `main.cpp`.

### Build
```shell
cmake -S . -B build -DCOMPILE_EXECUTABLE=ON && cmake --build build
```

### Build a single target
```shell
cmake -S . -B build -DCOMPILE_EXECUTABLE=ON && cmake --build build --target library
```

### Run
```shell
./build/executable
```
