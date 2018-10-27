# docker-info

## Docker Image

Docker can build an image by reading the build instructions from 
a file that’s generally referred to as Dockerfile. 
So, first, check your connectivity with the “dockerhost” and then create a folder called `nginx`. 
In that folder, we have created a file called `dockerfile` and in the dockerfile,
we have used different instructions, like FROM, RUN, EXPOSE, and CMD.

To build an image, we’ll need to use the docker build command. 
With the -t option, we can specify the image name,
and with a “.” at the end, we are requesting Docker to look at the current folder to find the dockerfile,
and then build the image.

## Docker Hub

On the Docker Hub, we also see the repositories — for example, for nginx, redis, and busybox.
For a given repository, you can have different tags, which will define the individual image.
On the repository page, we can also see a respective Dockerfile, from which an image is created.
for example, you can see the Dockerfile of the nginx image. 

If you don’t have an account on Docker Hub, I recommend creating one at this time.
After logging in, you can see all the repositories we’ve created.
Note that the repository name is prefixed with our username.

To push an image to Docker Hub, make sure that the image name is prefixed with the username used to log into the Docker Hub account.
With the docker image push command, we can push the image to the Docker Registry, which would, by default, go to the Docker Hub.  

## Automated build

DockerHub has a functionality called Docker automated builds, that can trigger a build on DockerHub as soon as you commit a code on your GitHub repository.
On GitHub, we have a repository called docker-automated-build, in which we have a Dockerfile, using which the image will be created. In the real-world example, we would have our application code with Dockerfile.

To create the automated build, we need to first log into our DockerHub account, and then, link our GitHub account with DockerHub. Once the GitHub account is linked, we click on “Create” and then on “Create Automated Build.”

Next, we provide a short description and then click on “Create.” Then, we select the GitHub repository that we want to link with this DockerHub automated build procedure.
Now, we can go to our GitHub repository and change something there. As soon as we commit the change, a Docker build process would start on our DockerHub account.

Our image build is currently in queue, which will be scheduled eventually, and our image would be created.
After that, anybody would be able to download the image.