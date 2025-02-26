# Building Your First Neural Network in Python

This repository provides a setup for running **JupyterLab** inside a Docker container.  
The Docker image includes everything you need to run JupyterLab, and the setup allows you to open and work with the notebook **`softmax_exercise.ipynb`**.

Within the notebook, you will find a short explanation and an exercise to help you understand and implement the softmax function.

**Have happy learning!**

## Prerequisites

Make sure you have the following installed on your machine:
- **Docker**: [Install Docker](https://docs.docker.com/get-docker/)
- **Git**: [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

## Steps to Run JupyterLab in Docker

Follow the steps below to clone this repository, build the Docker image, and run JupyterLab.

### 1. Clone the Repository

Open a terminal and run the following command to clone this repository:

```bash
git clone https://github.com/julianfm7/softmax_exercise.git
```

Navigate into the cloned repository directory:

```bash
cd softmax_exercise
```

### 2. Build the Docker Image

Once you're in the repository directory, build the Docker image using the following command:

```bash
docker build -t sm-exercise-image .
```

This will build the Docker image named `sm-exercise-image` from the `Dockerfile` in the repository.

### 3. Run the Docker Container

After building the Docker image, run the Docker container with the following command:

```bash
docker run -p 8888:8888 sm-exercise-image
```

This command will:
- Run the container in the foreground.
- Expose port `8888` on your local machine, which is the default port for JupyterLab.

### 4. Open JupyterLab in Your Browser

Once the container is running, open your web browser and navigate to:

```
http://localhost:8888/lab/tree/softmax_exercise.ipynb
```

JupyterLab should now be running, and you’ll be able to create, edit, and execute **`softmax_exercise.ipynb`**.