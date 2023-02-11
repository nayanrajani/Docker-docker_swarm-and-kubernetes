# Docker-docker_swarm-and-kubernetes

- <img width="532" alt="image" src="https://user-images.githubusercontent.com/57224583/218272989-24e7ba38-45e3-4fac-96b0-7f6181c2ae2e.png">

- So first of all, you have to get a container environment.
- Risk environment can be based on the virtual machine on which you deploy a darker and darker layer.
- When one visa environment is being built, you can create within subsequent call images immediately just so you can be your applications.
- Okay, that's you on which you are embedded.
- You have embedded or revert or a requirement or a dependencies that has been or requires or for visa image.
- Okay, we can have different types of images.
- You can have rabbits and Q images, so you can have an engine excite images or you can have your home
- or application image.
- Okay, so to do this image one cause your source code is already let me or Landry.
- So once your source code is ready, for example, we can build this image or based on what's, what is called very decora file.
- And to create view image your use of a command docker builds okay and be followed by the name of your image.
- Once this image is built as been built okay and or created, you can push this image or on a public
- registry or you can let it out locally if you went up to you.
- Okay.
- But with push come in, permit you to push a visa imager on any registry areas that you want.
- It can be a very private registry of your company or it can be a public what used to be a rovi internet only cloud.
- And or or you can let this image simply locally in your environment handle that and risk and comment is your reporter comment okay.
- If you don't have the image or locally in your environment, it can logically comment which is the pull comment, which means that's how I - want to get this type of image in my environment, in my look docker environment.
- So this content will go in the public registry or a proof private registry if you configure it by default.
- Or this comment will go on the public registry and or looking for this this specific or image that you are looking for.
- And the pull it locally in your environment.
- So owners on that would be able to run your new container because you have to have come the and differentiate the image from we continued - a container is a new instance of a image.
- So when you're rules comment docker run for example followed by the name of the container or or the contents to know that we want to run a new instance of image will be create and this new instance will be what's called container.
- Okay, so we container it's zero.
- It is a new instance of the image and or when the country in the container is lost, we will be able to have access or to your - applications just so we saw vis a vis steps that we have to follow to be able to get a new container in your environment.
- So and let's talk a bit about your own command.
- We were in command is just so we command that permission to launch a new instance of an image.
- And one new logic in this command we're looking locally.
- If this container instance that you went to launched is this image is really easy locally is locally in your in your environment.
- If this image is don't is not there in this environment, it will go to Vista.
- The corridor is free by default and or pull this image locally before able to be here or lost this new instance and build your container image.
- Okay, so is that whole for this global stature and now you to move on our labor or environment.

## Install Docker on ubuntu

- check Install+Docker.txt

- start a vm with ubuntu image on it.
  - you require an key-pair to access and security group with ssh and all traffic access on it.
- then do ssh into your machine, and run below command
  - sudo su -
  - sudo apt-get update
  - sudo mkdir -m 0755 -p /etc/apt/keyrings
  - 6 curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
  - echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
    \$(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
  - sudo apt-get update
  - sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
  - docker version

## Docker hub Public repository

- Docker Hub is the world’s largest repository of container images with an array of content sources including container community developers, open source projects and independent software vendors (ISV) building and distributing their code in containers. Users get access to free public repositories for storing and sharing images or can choose subscription plan for private repos.

- Docker Commands

  - docker –version – Display the current versions.
  - docker pull <image> – Docker repository images can be pulled using the docker pull command.
  - docker ps -a – Displays running and exited containers.
  - docker exec -it <container id> bash – Command for accessing running container.
  - docker kill <container id> – Command for stopping the execution of a container immediately.
  - docker commit <container id> <username/image name> – This command creates a new image of an edited container on the local system.
  - docker push <username/image name> – This Docker command is used to push an image to the docker hub repository.
  - docker images – Listing all images stored in a docker.
  - docker rm <container id> – Deleting a container which has stopped execution.
  - docker checkpoint command – This Docker command is used for managing checkpoints.
  - docker save [OPTIONS] IMAGE [IMAGE…] – Saving more than one image to tar archives.
  - docker stats [OPTIONS][container…] – Displaying resource usage statistics.
  - docker system command – It is Used for Managing a docker.
  - <img width="492" alt="image" src="https://user-images.githubusercontent.com/57224583/218275722-8fdb8a04-0f78-4902-99c2-4d29fa0f564b.png">
  - docker unpause CONTAINER [CONTAINER…] – Unpause all processes within one or more containers.
  - docker import [OPTIONS] file|URL|- [REPOSITORY[: TAG]] – Importing contents from the tarball to create a system image of the file.
  - docker info [OPTIONS] – Display system-wide information
  - docker logout [SERVER] – Logging out of a Docker registry.

- Advance commands

  - docker-machine upgrade default – To upgrade the docker to the latest version. How this upgrade happens depends on the underlying distribution used on the created instance.
  - docker build –rm=false – Boolean options take the form -d=false. The value you see in the help text is the default value which is set if you do not specify that flag. If you specify a Boolean flag without a value, this will set the flag to true, irrespective of the default value.

- Tips and Tricks to Use Docker Commands
  - Use -f flag for activating the logging.

## Add container Image

- check Add+Image.txt

- docker pull mysql
- docker images
- docker pull ubuntu
- docker images
- docker ps
- docker ps -a
- docker pull jenkins:2.60.3
- docker run -d -p jenkins:2.60.3
- docker run -d -p 9080:8080 jenkins:2.60.3
- docker ps -a
  - now check the jenkins is running or not, by below command
    - <yourVMPublicIPAddress>:9080

## Basic Commands

- check Basic+commands.txt

- docker run -it jenkins:2.60.3 /bin/bash
- docker attach 9c6334210840
- docker inspect 9b6ad91eb286
- docker rm 9b6ad91eb286
- docker ps -a
- docker images
- docker rmi mysql
- docker rmi ubuntu
- docker rmi jenkins
- docker rmi jenkins:2.60.3
- docker images-
