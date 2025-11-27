[![](https://img.shields.io/badge/c++-black?logo=c++&style=for-the-badge)](https://learnxinyminutes.com/c++/)
[![](https://img.shields.io/badge/cmake-black?logo=cmake&style=for-the-badge)](https://cmake.org/)

## Cpp project template
Template project using basic cmake configuration to compile a single file in `src/main.cpp`.

### Build
```shell
cmake -S . -B build -DCMAKE_BUILD_TYPE=Release && cmake --build build
```

### Run
```shell
./build/executable
```
