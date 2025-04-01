# Docker

## Docker Definition
**Docker** is an open-source platform that enables developers to build, package, and distribute applications in lightweight, portable containers. These containers include everything the application needs to run, ensuring consistency across different environments (development, testing, production).

🚀 ## Key Features:

**Isolation**: Runs applications independently of the underlying system.

**Portability**: Works the same on any machine (local, cloud, or server).

**Efficiency**: Uses fewer resources than traditional virtual machines.


## Docker in Simple Terms 🐳
**Docker** is like a container for your app. It packs everything your app needs (code, libraries, dependencies) so it runs the same way everywhere—on your laptop, a server, or the cloud.

Think of it like a lunchbox 🍱:

Your app = The food 🍔

Docker = The box that keeps everything together ✅

No matter where you take the lunchbox, the food inside stays the same! 🎯

With Docker, you don’t need to worry about "it works on my machine but not on yours" problems. 🚀



## Docker Images vs. Containers (With Example)
1️⃣ **Docker Image** 🖼️
A Docker image is like a blueprint 📜 or a recipe 🍳. It contains everything needed to run an application (code, dependencies, system libraries).

Example:

A Python Flask app image may contain:

Python

Flask framework

Required libraries (requirements.txt)

Command to Build an Image:

docker build -t my-flask-app .

This creates an image named my-flask-app.

2️⃣ **Docker Container** 📦
A Docker container is a running instance of a Docker image. It's like making a dish from the recipe 🍕.

Example:

If an image is a Flask app, then a container is the Flask app running on a server.

Command to Run a Container:

docker run -p 5000:5000 my-flask-app

This starts a container from my-flask-app, making it accessible at localhost:5000.

Real-World Analogy 🍱
Docker Image = A frozen pizza box (ready to cook)

Docker Container = The pizza after being cooked and served


## Relationship Between Docker Image and Docker Container
Think of Docker Images and Docker Containers as related but distinct concepts:

Docker Image 🖼️	Docker Container 📦
A blueprint or template	A running instance of an image
Read-only	Read-write (temporary changes)
Created with docker build	Created with docker run
Can be stored and shared	Runs temporarily, can be restarted
 
Like a frozen pizza (ready to cook) 🍕	Like a hot pizza (ready to eat) 🔥
 
 Docker Image 🖼️	Docker Container 📦
A blueprint or template	A running instance of an image
Read-only	Read-write (temporary changes)
Created with docker build	Created with docker run
Can be stored and shared	Runs temporarily, can be restarted
 
Like a frozen pizza (ready to cook) 🍕	Like a hot pizza (ready to eat) 🔥
 
 
How They Work Together:
1️⃣ Build an Image → docker build -t my-app .

Creates an image from a Dockerfile
2️⃣ Run a Container → docker run -p 5000:5000 my-app

Starts a container using the image
3️⃣ Stop/Delete Container → docker stop <container_id> / docker rm <container_id>
4️⃣ Image Remains, Containers Can Be Restarted 🚀


## Basic Docker Commands
Once installed, here are some essential commands:

🔹 **Check Docker Version**

docker --version

🔹 **Run a Container**

docker run hello-world
This runs a test container to verify Docker is working.

🔹 **List Running Containers**

docker ps
To list all containers (including stopped ones):

docker ps -a

🔹 **Stop a Running Container**

docker stop <container_id>

🔹 **Remove a Container**

docker rm <container_id>

🔹 **Download a Docker Image**

docker pull ubuntu
This pulls the Ubuntu image from Docker Hub.

🔹 **Run an Interactive Ubuntu Container**

docker run -it ubuntu bash