## How to run this app

### Copy multi-stage code to Dockerfile
### run the code in the terminal to build image:
    docker build -t flask-app:latest .

### run the code in the terminal to run container from image:
    docker run -d -p 5000:5000 flask-app:latest

### Open in your browser:
    localhost:5000

### Curl on the terminal:
    curl http://localhost:5000

### Stop all containers and Images and Delete them:
    docker stop $(docker ps -aq) && docker rm -f $(docker ps -aq) && docker rmi -f $(docker images -q)