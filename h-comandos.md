The following command runs an `ubuntu` container, attaches interactively to your local command-line session, and runs `/bin/bash`.

```console
$ docker run -i -t ubuntu /bin/bash
```

```console
docker run -d -p 8080:80 docker/welcome-to-docker
```


aa aa

docker ls -a 
When you run this command, the following happens (assuming you are using the default registry configuration):


1. To get started, either clone or [download the project as a ZIP file](https://github.com/docker/getting-started-todo-app/archive/refs/heads/main.zip) to your local machine.
    
    ```console
    $ git clone https://github.com/docker/getting-started-todo-app
    ```
    
    And after the project is cloned, navigate into the new directory created by the clone:
    
    ```console
    $ cd getting-started-todo-app
    ```
    
2. Once you have the project, start the development environment using Docker Compose.
    
    To start the project using the CLI, run the following command:
    
    ```console
    $ docker compose watch
    ```


--------

1. To get started, either clone or [download the project as a ZIP file](https://github.com/docker/getting-started-todo-app/archive/refs/heads/main.zip) to your local machine.
    
    ```console
    $ git clone https://github.com/docker/getting-started-todo-app
    ```
    
    And after the project is cloned, navigate into the new directory created by the clone:
    
    ```console
    $ cd getting-started-todo-app
    ```
    
2. Build the project by running the following command, swapping out `DOCKER_USERNAME` with your username.
    
    ```console
    $ docker build -t DOCKER_USERNAME/getting-started-todo-app .
    ```
    
    For example, if your Docker username was `mobydock`, you would run the following:
    
    ```console
    $ docker build -t mobydock/getting-started-todo-app .
    ```
    
3. To verify the image exists locally, you can use the `docker image ls` command:
    
    ```console
    $ docker image ls
    ```
    
    You will see output similar to the following:
    
    ```console
    REPOSITORY                          TAG       IMAGE ID       CREATED          SIZE
    mobydock/getting-started-todo-app   latest    1543656c9290   2 minutes ago    1.12GB
    ...
    ```
    
4. To push the image, use the `docker push` command. Be sure to replace `DOCKER_USERNAME` with your username:
    
    ```console
    $ docker push DOCKER_USERNAME/getting-started-todo-app
    ```
    
    Depending on your upload speeds, this may take a moment to push.

```console
docker build -t DOCKER_USERNAME/getting-started-todo-app .
docker build -t huhusseyn/getting-started-todo-app .
    ```

    ```console
    $ docker push huhusseyn/getting-started-todo-app
    ```


    ----
## Imagens

    docker run --name=base-container -ti ubuntu

    apt update && apt install -y nodejs

    node -e 'console.log("Hello world!")'


    docker container commit -m "Add node" base-container node-base

    docker run node-base node -e "console.log('Hello again')"
