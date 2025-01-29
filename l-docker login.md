Sign in from the Docker CLI client
Run:
docker login -u dockkrossa
At the password prompt, enter the personal access token:

Create an image repository
Now that you have an account, you can create an image repository. Just as a Git repository holds source code, an image repository stores container images.

Go to Docker Hub.

Select Create repository.

On the Create repository page, enter the following information:

Repository name - getting-started-todo-app
Short description - feel free to enter a description if you'd like
Visibility - select Public to allow others to pull your customized to-do app
Select Create to create the repository.

Build and push the image
Now that you have a repository, you are ready to build and push your image. An important note is that the image you are building extends the Node image, meaning you don't need to install or configure Node, yarn, etc. You can simply focus on what makes your application unique.

What is an image/Dockerfile?

Without going too deep yet, think of a container image as a single package that contains everything needed to run a process. In this case, it will contain a Node environment, the backend code, and the compiled React code.

Any machine that runs a container using the image, will then be able to run the application as it was built without needing anything else pre-installed on the machine.

A Dockerfile is a text-based script that provides the instruction set on how to build the image. For this quick start, the repository already contains the Dockerfile.

CLI VS Code
To get started, either clone or download the project as a ZIP file to your local machine.


 git clone https://github.com/docker/getting-started-todo-app
And after the project is cloned, navigate into the new directory created by the clone:


 cd getting-started-todo-app
Build the project by running the following command, swapping out DOCKER_USERNAME with your username.


 docker build -t DOCKER_USERNAME/getting-started-todo-app .
For example, if your Docker username was mobydock, you would run the following:


 docker build -t mobydock/getting-started-todo-app .
To verify the image exists locally, you can use the docker image ls command:


 docker image ls
You will see output similar to the following:


REPOSITORY                          TAG       IMAGE ID       CREATED          SIZE
mobydock/getting-started-todo-app   latest    1543656c9290   2 minutes ago    1.12GB
...
To push the image, use the docker push command. Be sure to replace DOCKER_USERNAME with your username:


 docker push DOCKER_USERNAME/getting-started-todo-app
Depending on your upload speeds, this may take a moment to push.