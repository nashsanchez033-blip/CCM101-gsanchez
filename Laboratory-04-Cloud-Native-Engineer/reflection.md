# Mission Reflection

This laboratory helped me understand why containers are useful in cloud computing and modern software development. One major difference between Docker containers and Virtual Machines is their boot time and setup process. A Virtual Machine needs to start a complete operating system, which can take minutes and requires more CPU, RAM, and storage. In comparison, a Docker container shares the host operating system kernel and only includes the application and its required dependencies, allowing it to start within seconds.

Port mapping is necessary when running a web server inside a container because the application is running in an isolated environment. In this activity, the Nginx web server uses port 80 inside the container, while port 8080 is exposed on the host machine. The `-p 8080:80` option connects the host port to the container port, allowing users to access the Nginx web server through `http://localhost:8080`.

When the `docker rm` command is used, the container itself is permanently removed. Data stored only inside the container can also be lost if it was not saved using a volume or external storage. This is important because applications that need persistent data should use appropriate storage solutions.

Containerization also changes how developers and IT operations teams work together. Developers can package applications and their dependencies into containers, while operations teams can deploy the same containers consistently in different environments. This supports DevOps by improving collaboration, consistency, automation, and deployment speed.

Finally, my GitHub portfolio is evolving from basic cloud computing activities into a collection of practical technical projects. This laboratory adds Docker, containerization, Nginx deployment, and technical documentation to my portfolio. It shows my progress from learning cloud concepts to performing actual cloud-native deployment tasks.
