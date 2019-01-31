# wio-images
Docker images for wio, see [Docker Hub](https://hub.docker.com/r/waterloop/wio-images)

## Master Image
Contains build tools for native, embedded, and pod systems.
Image includes boost, avr and build-essential

Usage for .gitlab-ci.yml: 
```
image: waterloop/wio-images:latest

stages:
  - build
  
build:
  stage: build
  script:
    - wio install
    - wio build -all
```

## Boost-CPP Image
Contains build tools for native, pod systems.
Image just includes boost and build-essential

Usage: (Replace frist line in yml file)
```
image: waterloop/wio-images:boost-cpp
```

## AVR Image
Contains build tools for native and embedded development.
Image just includes avr and build-essential

Usage: (Replace frist line in yml file)
```
image: waterloop/wio-images:avr
```
