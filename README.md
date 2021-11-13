# Multi-Architecture Images Demo

### context
+ docker
+ docker buildx
+ dockerhub, quay.io, etc account

### test
+ docker login (need have container image registry's account) and create repository
+ git clone & cd
    ```shell
    git clone git@github.com:quan930/Multi-ArchitectureImagesDemo.git
    cd Multi-ArchitectureImagesDemo
    ```
+ docker buildx builder config
    ```shell
    docker buildx create --name lilqbuilder
    docker buildx use lilqbuilder
    docker buildx inspect lilqbuilder --bootstrap
    docker buildx ls
    ```
+ build images and push images
    ```shell
    docker buildx build --platform linux/amd64,linux/arm/v7,linux/arm/v6,linux/s390x -t lilqcn/multi-architecture-demo:v1 --push .
    ```