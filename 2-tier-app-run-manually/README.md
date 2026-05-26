# Run App containers manually

## Create custom bridge network
    docker network create my_network
    docker network ls

## Copy code from run_containers_script/mysql.txt and paste into nterminal
    It will start mysql database container

    Wait 10s for MySQL to initialize

## Build the Flask Docker Image (it will use Dockerfile)
docker build -t flask-app .

## Copy code from run_containers_scripts/pythonapp.txt and paste into nterminal
    It will start the python-flask container

## Copy code from run_containers/pythonapp.txt and paste into nterminal
    It will start the python-flask container

### Open in your browser:
    localhost:5000

### Curl on the terminal:
    curl http://localhost:5000

### Stop all containers and Images and Delete them:
    docker stop $(docker ps -aq) && docker rm -f $(docker ps -aq) && docker rmi -f $(docker images -q)