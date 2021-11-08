docker pull
docker images
docker run -d -p <ip:port> <image name/id>  // -p specific port number. -d detached mode , -it interactive mode. Ctrl +C to come out of container as exit
docker ps
docker ps -a
docker run -d -P --name <name> <image name> // -P randome port number
docker stop, restart, start

docker exec -it <cont id> bash      // go inside of a container // prompt will be change as root will be docker OS
docker run -it -P nginx bash.      // create a container and log in to it
cd usr/share/nginx/html/index.html  // where the content of page is displaying, can remove the file and add a file with same name with desired content
ctrl pq  //come outside of your container //exit will kill the process so the contaioner will be shutdown

// create an new image with customized container
docker commit -m "modified container" <cont id> <anyname>:<version>
