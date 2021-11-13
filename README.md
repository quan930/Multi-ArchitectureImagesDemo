# Multi-Architecture Images Demo


docker buildx build --platform linux/amd64,linux/arm/v7,linux/arm/v6,linux/s390x -t lilqcn/multi-architecture-demo:v1 --push .
