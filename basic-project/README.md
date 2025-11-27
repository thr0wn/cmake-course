[![](https://img.shields.io/badge/c++-black?logo=c++&style=for-the-badge)](https://learnxinyminutes.com/c++/)
[![](https://img.shields.io/badge/cmake-black?logo=cmake&style=for-the-badge)](https://cmake.org/)

## Basic project
Basic project with two targets: `executable` and `library`.

### Build
```shell
cmake -S . -B build -DCMAKE_BUILD_TYPE=Release && cmake --build build
```

### Build a single target
```shell
cmake -S . -B build -DCMAKE_BUILD_TYPE=Release && cmake --build build --target library
```

### Run
```shell
./build/executable
```
