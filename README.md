# Waterloop Docker Images
Docker images for wio, see [Docker Hub](https://hub.docker.com/r/waterloop/wio-images)

## Build Images

### AVR Image
Contains build tools for embedded development. Image includes avr and build-essential.
This image can be used to build and test AVR projects using wio.

Usage for .gitlab-ci.yml: 
```yaml
image: waterloop/build:avr

stages:
  - build
  
build:
  stage: build
  script:
    - wio install
    - wio build -all
```

### C++ Boost Image
Contains build tools for C++ development. Image includes compilers, boost and build-essential.
It also contains proto library and proto compiler. This image can be used to build and test C++ projects using wio.

Usage for .gitlab-ci.yml: 
```yaml
image: waterloop/build:cpp

stages:
  - build
  
build:
  stage: build
  script:
    - wio install
    - wio build -all
```

## Codecheck Images

### C++ Image
Contains code checking tools for C++. These tools are: `cppcheck` and `cpplint`

Usage for .gitlab-ci.yml: 
```yaml
image: waterloop/cppcheck:cpp

stages:
  - check
  
check:
  stage: check
  script:
    - cpplint --recursive src tests vendor/*/src vendor/*/include vendor/*/tests
    - cppcheck src tests vendor/*/src vendor/*/include vendor/*/tests
```
