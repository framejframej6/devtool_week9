```docker stop $(docker ps -aq)
docker rm $(docker ps -aq)
docker rmi -f $(docker images -aq)
rm -rf devtool_week9
git clone https://github.com/framejframej6/devtool_week9.git
cd devtool_week9/backend
docker build -t fastapi-docker_lab5 .
cd ..
cd frontend
docker build -t flask-docker-app .
docker run -p 8088:80 fastapi-docker_lab5 
docker run -p 8081:8081 -d --name container_building.jpg  -e APP_COLOR=building.jpg flask-docker-app```
