# Week4 Containers & Kubernetes - Docker & K8s (Days 27–33)

## Goal

Learn how to containerize an app and run it on Kubernetes locally.

## Time Commitment

2 hours per day, 5–7 days (this week is denser).

## What To Expect

By the end of Week 4, you should:

- Be able to write a basic Dockerfile
- Build and run a container locally
- Understand Kubernetes primitives (pod, deployment, service)
- Deploy a simple app on Minikube

You don’t need to master production-grade K8s yet.

![Demo animation](images/k8s.gif)

## Step-by-Step

1. Learn Docker basics

   Play with Docker:
   https://labs.play-with-docker.com/

   Docker beginner labs:
   https://github.com/docker/labs/tree/master/beginner

• Learn: image, container, Dockerfile, docker run, docker ps, docker logs.

2.  Containerize a simple app
    • Take a basic Node.js or Python Flask app
    • Write a Dockerfile (using an example from the Docker labs)
    • Build image: docker build -t myapp:v1 .
    • Run image: docker run -p 8080:8080 myapp:v1.

3.  Install Minikube

    https://minikube.sigs.k8s.io/docs/start/
    • Install and start Minikube
    • Confirm kubectl get nodes works.

4.  Learn Kubernetes basics

    Kubernetes interactive tutorial:
    https://kubernetes.io/docs/tutorials/kubernetes-basics/

    Hello Minikube:
    https://kubernetes.io/docs/tutorials/hello-minikube/

    • Concepts: pod, deployment, service, ingress (at least the first three in depth).

5.  Deploy your container to Minikube
    • Create a Deployment YAML for your container image
    • Create a Service (NodePort)
    • Access the app using Minikube service URL.

## Checklist

- You can explain what a container is and how it differs from a VM
- You have built and run a Docker image locally
- You understand pod, deployment, and service at a high level
- You have deployed at least one app to Minikube

## Practice Resources

    https://kodekloud.com/free-labs/kubernetes
    https://labs.play-with-docker.com/
    https://github.com/docker/labs/tree/master/beginner
    https://minikube.sigs.k8s.io/docs/start/
    https://kubernetes.io/docs/tutorials/kubernetes-basics/
    https://kubernetes.io/docs/tutorials/hello-minikube/

## What Won’t Work

    Jumping to managed Kubernetes before you’ve run Minikube locally.
