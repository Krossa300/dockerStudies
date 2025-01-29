The following command runs an ubuntu container, attaches interactively to your local command-line session, and runs /bin/bash.


 docker run -i -t ubuntu /bin/bash
When you run this command, the following happens (assuming you are using the default registry configuration):

If you don't have the ubuntu image locally, Docker pulls it from your configured registry, as though you had run docker pull ubuntu manually.

Docker creates a new container, as though you had run a docker container create command manually.

Docker allocates a read-write filesystem to the container, as its final layer. This allows a running container to create or modify files and directories in its local filesystem.

Docker creates a network interface to connect the container to the default network, since you didn't specify any networking options. This includes assigning an IP address to the container. By default, containers can connect to external networks using the host machine's network connection.

Docker starts the container and executes /bin/bash. Because the container is running interactively and attached to your terminal (due to the -i and -t flags), you can provide input using your keyboard while Docker logs the output to your terminal.

When you run exit to terminate the /bin/bash command, the container stops but isn't removed. You can start it again or remove it.