
## Commands used to run the app

### Build the image

```docker
docker build -t flask-hello-world .
```
- This command must be performed inside the folder containing the dockerfile.

### Run the container

```docker
docker run -p 5000:5000 flask-hello-world
```
- The -p 5000:5000 maps thje port 5000 of the container to the port 5000 of the machine
