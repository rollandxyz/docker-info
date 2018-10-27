
# Docker Hub Introduction Tutorial

An introduction to Docker Hub Docker remote repository. We pull an image from Docker Hub, make some edits, commit those edits to a new image then push that new image to our Docker Hub account in the cloud.
Docker hub hosts images (not container, container is an instance of the image you run/start)

```bash
sudo docker -v                          // check docker version
sudo docker run hello-world             // run docker test image (will be downloaded automatically)

sudo docker images                      // list images (blueprints)
sudo docker ps -a                       // list containers (actual instances)
sudo docker pull ubuntu                 // pull ubuntu image from docker hub library/ubuntu
sudo docker run -it -d ubuntu           // run and detach ubuntu, you should see it in your container
sudo docker exec -it <image_id> bash    // login to docker image
                                        // make some changes to the container
sudo docker exit                        // exit from container


sudo docker commit <image>  <to-image>  // commit your changes to a image or your docker hub account

sudo docker login                       // must login before your push
sudo docker push <to-image>             // push your changes docker hub account
sudo docker logout
                                        // you can go to your docker hub cloud now

sudo docker stop <image_id>             // stop docker container
sudo docker ps -a                       // verify docker container is not running

sudo docker rm  <image_id>              // remove docker container
sudo docker rm  -f  <image_id>          // remove docker container
sudo docker images                      // verify docker container is removed

sudo docker rmi <image_id>              // remove docker image
sudo docker rmi -f <image_id>           // remove docker image
                                            
sudo docker pull    <acount>/<to-image>         // download the image from docker hub
sudo docker images                              // check if downloaded   
suod docker run -it <acount>/<to-image>         // run image 
sudo docker exec -it <image_id> bash            // login to container              

// image format: <user-name>/<image-name>:<tag>
```





---

https://hub.docker.com/
https://cloud.google.com/container-registry/