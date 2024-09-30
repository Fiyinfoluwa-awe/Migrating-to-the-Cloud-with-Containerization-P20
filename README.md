# Migrating-to-the-Cloud-with-Containerization-P20
Docker

Until now I have been using VMs(AWS EC2) in the Amazon Virtual Private Cloud (AWS VPC) to deploy my web solutions , and it worked well in many cases. I have learnt how to easily spin up and configure a new EC2 manually or with such tools as Terraform and Ansible to automate provisioning and configuration. I have also deployed two different websites on the same VM; this approach is scalable, but to some extent; imagine if you need to deploy many small applications ( it can be web front-end, web-backend, processing jobs, monitoring, logging solutions, etc.) and some of the applications will require various OS and runtimes of different version sand conflicting dependencies- in such case, you would need to spin up servers for each group of applications with  the exact OS, runtime and dependencies requirements. When it scales out to tens, hundreds and even thousands of applications (e.g, when we talk of mmicroservice architecture), this approach becomes very tedious and challenging to maintain.

In this Project, I will be learning how to solve this problem and begin to practice the technology that revolutionized application distribution and deployment back in 2013! We are talking of Containers and imply [Docker](https://en.wikipedia.org/wiki/Docker_(software)). Even though there are othe application containerization technologies, Docker is the standard and the default choice for shipping your app in a container!

**Side self study:** Before starting to work with this project, it is very important to understand what Docker is and what it is used for. To get a sufficient level of theoretical knowledge it is recommended to read up Docker, before going on with the project.

**Install Docker and prepare for migration to the Cloud**

First, I need to install [Docker engine](https://docs.docker.com/engine/), ehich is a client-server application that contains;

* A server that with a long-running daemon process `dockerd`
* APIs that specify interfaces that programs can use to talk and instruct the Docker daemon.
* A Command-Line Interface (CLI) client `docker`.

We can learn how to install Docker engine on a PC [here](https://docs.docker.com/engine/install/). 

Before I proceed further, let's us understand why we need to move from VM to Docker.

As I have learnt- unlike a VM , Docker allocated not the whole guest OS for your application, but only isolated minimal part of it - this isolated container has all that that your application needs and the same time is lighter and faster , and can be shipped as a Docker image to multiple physical  or virtual environments, as long as this environment can run Docker engine. This approach also solves the enviroment incompatibility issue. It is a well-known problem when a developer sends his application to you, you try to deploy it , deployment fails, and the developer replies, *"-it works on my machine!"*. With Docker - if the application is shipped as a container, it has its own environment isolated from the rest of the world, and it wil always work the same way on any server that has Docker engine.


```
      ¯\_(ﭣ)_/¯
 IT WORKS ON MY MACHINE
```




