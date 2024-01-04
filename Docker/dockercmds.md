# Docker Commands

docker pull ***image_name*** -> Pulls the image from docker hub. It pulls latest image.

docker pull ***image_name:version*** -> Pulls image with specified version. 

docker run ***image_name*** -> Runs the image/creates container(creates new container every single time you run this command).

docker run -d ***image_name*** -> Runs docker image in detached mode.

docker log ***container_id*** -> Shows log of container.

docker images -> Shows list of all locally available images.

docker ps -> Shows list of all running images i.e containers.

docker stop ***container_id*** -> Stops running container.

docker run -p ***Host_port:container_port*** -> This port binding helps in running container from container port to host port.

docker ps -a -> Show list of all containers whether they are running or stopped.

docker start ***container_id*** -> start exited container.

docker run --name ***name_of_your_choice*** -> Docker containers have random names given by docker hub but using this command you can give name to your container manually. 

docker build -t ***image_name_of_your_choice:tag*** -> builds docker image



***Note: Wherever we have used container_id there we can use container names also***