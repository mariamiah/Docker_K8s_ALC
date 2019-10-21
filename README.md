# ALC CLOUD PROJECT
## Description
- Create a React application
- Containerize the appication with Docker
- Push the Docker image to Docker hub
- Deploy the application to Google Kubernetes Engine

## Creating the REACT application
```npx create-react-app my-app
cd my-app
npm start 
```

## Containerize the Application
- Install docker on your local ubuntu machine using this [link](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-16-04)
- Add a Dockerfile in the projects root
- Build an image with `docker build -t <image_name> .`
- Tag the image for dockerhub by running `docker tag <imageId> <targetrepository/imagename>`
- Push the image by running `docker push <taggedImage>`

## Deploy to Google Cloud(GKE)
- use gcloud to login into google cloud using `gcloud auth login`
- set up a kubernetes cluster on google cloud using `gcloud container clusters create mycluster`
- connect to the kubernetes cluster using kubectl
- Add a deployment config file
- Set up a service.yml file
- use kubectl to apply the configurations
- Navigate to the service load balancer address to view the deployed application

## Deployed application
http://35.223.212.51/