<pre>
docker --version
# more details
docker info
#To verify process
docker run hello-world

docker container ls -a
docker ps
docker ps -a

docker --version
docker info
docker run hello-world
#to list container
docker container ls -a
docker ps
docker ps -a
#to name a container
docker run --name toyota hello-world
docker ps -a
#To see image history
docker image  {imgname} history

docker images
docker run hello-world
docker run --name hello-world

docker run --name introserver -d -p 8000:80 lotech/dockerintro:latest
docker run --name introserver2 -p 1000:80 lotech/dockerintro:latest
docker  ps
docker stop 43c7f268bb30
docker start 43c7f268bb30
docker ps
\
docker run -d -p 8000:80 --rm --name goodbye lotech/dockerintro:latest
docker rm introserver
docker stop introserver
docker rm introserver
docker container ls -a
docker system prune
docker images
docker container rm cc3f2ff51cab cd20b396a061
docker container prune
docker container stop $(docker container ls -aq)
docker kill $(docker ps -q)
docker rm $(docker ps -a -q)
docker rmi $(docker images -q)
docker volume ls -qf dangling=true | xargs -r docker volume rm
docker ps -qa | xargs docker stop

docker kill [ID]

#stop all containers:
docker stop $(docker ps -a -q)

#stop all containers by force
docker kill $(docker ps -q)

#remove all containers
docker rm $(docker ps -a -q)

#remove all docker images
docker rmi $(docker images -q)

#purge the rest
docker system prune --all --force --volumes

docker container stop $(docker container ls -q)
docker rm -f $(docker ps -a -q)

#kill all docker containers at once...

docker ps -q | xargs docker stop ; docker system prune -a

docker restart wonderful_kalam

docker log {container id}


</pre>