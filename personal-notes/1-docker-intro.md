# Docker Introduction:
- Docker is a tool for creating and managing container.
- A container is a standardized unit of software.
- The same container always yields the exact same application and execution behavior.
- Support for container has now started to be built into all the major operating system.

# Getting Started with Docker:
- Sample program:
```Dockerfile
    FROM node:14

    WORKDIR /app

    COPY package.json

    RUN npm install

    COPY . .
     
    EXPOSE 3000
    
    CMD ["node", "app.mjs"]

```
- To build this image, simply run `docker build .` on the same level as the Dockerfile.
- The above step will build an image, to run that image with port mapping: `docker run -p [HOST_PORT]:[CONTAINER_PORT] [IMAGE]`
- List running containers: `docker ps`.