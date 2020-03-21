# A Docker Image for running Jupyter Notebook

## Description
Using this Dockerfile you can create a Docker image for running Jupyter Notebook 
with Anaconda and Tensorflow installed.

## Building the Docker image
```bash
docker build -t jupyter-docker .
```

## Running the container
Enter the following command from terminal:
```bash
docker run --name jupyter-docker -p 8888:8888 -v "$PWD/notebooks:/opt/notebooks" -d jupyter-docker
```

Open the following link from your browser:
```text
http://localhost:8888/
```

Enter the password: "root"

## Stopping the container
```bash
docker rm -f jupyter-docker
```