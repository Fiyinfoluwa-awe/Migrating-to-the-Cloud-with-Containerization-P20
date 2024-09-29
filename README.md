# Migrating-to-the-Cloud-with-Containerization-P20
Docker

Until now I have been using VMs(AWS EC2) in the Amazon Virtual Private Cloud (AWS VPC) to deploy my web solutions , and it worked well in many cases. I have learnt how to easily spin up and configure a new EC2 manually or with such tools as Terraform and Ansible to automate provisioning and configuration. I have also deployed two different websites on the same VM; this approach is scalable, but to some extent; imagine if you need to deploy many small applications ( it can be web front-end, web-backend, processing jobs, monitoring, logging solutions, etc.) and some of the applications eil require various OS and runtimes of different version sand conflicting dependencies- in such case, you would need to spin up servers for each group of applications with  the exact OS, runtime and dependencies requirements. When it scales out to tens, hundreds and even thousands of applications (e.g, when we talk of mmicroservice architecture), this approach becomes very tedious and challenging to maintain.

In this Project, I will be learning how to solve this problem and begin to practice the technology that revolutionized application distribution and deployment back in 2013! We are talking of Containers and imply Docker. Even though there are othe application containerization technologies, Docker is the standard and the default choice for shipping your app in a container!

**Side self study:** Before starting to wprk with this project, it is very important to understand what Docker is and what it is used for. To get a sufficient level of theoretical knowledge it is recommended to read up Docker, before going on with the project.

**Install Docker and prepare for migration to the Cloud**

First, I need to install Docker engine, ehich is a client-server application that contains;

* A server that with a long-running daemon process `dockerd`
* APIs that specify interfaces that programs can use to talk and instruct the DOker daemon.
* A Command-Line Interface (CLI) client `docker`.

