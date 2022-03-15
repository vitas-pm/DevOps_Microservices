## Cloud DevOps ND - C4- Microservices at Scale using AWS & Kubernetes 

[![CircleCI](https://circleci.com/gh/vitas-pm/DevOps_Microservices.svg?style=svg)](https://circleci.com/gh/vitas-pm/DevOps_Microservices)

This repository is associated with Cloud DevOps ND - Course 04 - Microservices at Scale using AWS & Kubernetes. 
1. A summary of the project
2. Instructions on how to run the web app
3. A short explanation of the files in the repository

---

### 1. Summary

The parts of the project that have been completed by me are as follows:
1. Cloning this Repository
3. Creating and Activating the `.devops` Environment
4. Installing other Dependencies (Docker, Hadolint, Kubernetes, Minikube)
5. Completing the Project Tasks:
   1. Completing the `Dockerfile`
   3. Completing `run_docker.sh`
   4. Completing `make_prediction.sh`
   5. Improving the Logging of `app.py`
   6. Completing `upload_docker.sh`
   7. Configuring Kubernetes to Run Locally
   8. Completing `run_kubernetes.sh`
   9. CircleCI Integration
   10. Writing this `README.md`

---

### 2. Instructions

Firstly if you plan to upload the Docker image to your personal Docker Hub you have to add a `docker_pw.txt` file
to the `project-ml-microservice-kubernetes` folder which contains only your Docker Hub password. Then change the 
`vitaspm` in `upload_docker.sh` to your own Docker Hub username.

To use the scripts in this repository, firstly change into the project folder using:\
`cd project-ml-microservice-kubernetes`

Create a venv and install the dependencies using:\
`make setup`\
`make install`

Also install the additional dependencies: Docker, Hadolint, Kubernetes, Minikube

You can then:

- `./run_docker.sh` to build a Docker container containing the web app
- `./upload_docker.sh` to upload the Docker container to your Docker Hub account
- `./run_kubernetes.sh` to run the Docker container on a Kubernetes cluster

Once the container with your app is running you can run `./make_prediction.sh` to create a prediction using the app. 

---

### 3. Files

Firstly the folders other than `project-ml-microservice-kubernetes` can be ignored since they are part of 
the repository but not related to the project. With the exception of `.circleci` which contains the 
`config.yml` which specifies the instructions of the CircleCI pipeline.

The project folder contains:
- `app.py and model_data` which are the necessary files for the prediction app to work
- `output_txt_files` which contains two logs of app tests using docker and kubernetes deployments
- `Dockerfile` which is used to build the Docker container to run the application
- `Makefile` which contains definitions of commands used by the circleci config and in the terminal
- `requirements.txt` which contains the libraries the app needs to work
- `.sh files` which can be used as explained in 2. Instructions


