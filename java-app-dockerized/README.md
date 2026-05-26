## How to run this app


### Run the code in the terminal to build image:
    docker build -t java-hello .

### Run and map container port 8080 to your host::
    docker run --rm -d -p 8080:8080 --name java-app java-hello

### Open in your browser:
    localhost:8080

### Curl on the terminal:
    curl http://localhost:8080

### You should see:
    "Walla, hello from Dockerized Java!"

### Stop all containers and Images and Delete them:
    docker stop $(docker ps -aq) && docker rm -f $(docker ps -aq) && docker rmi -f $(docker images -q)