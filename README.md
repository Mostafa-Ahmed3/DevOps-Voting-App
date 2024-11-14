# DevOps-Voting-App

Deploying app on Kubernetes
## Architecture

![architecture](https://github.com/user-attachments/assets/ea132ba4-3d41-4872-886e-2473099202b7)


A front-end web app in Python which lets you vote between two options

A Redis which collects new votes

A .NET worker which consumes votes and stores them in…

A Postgres database backed by a Docker volume

A Node.js web app which shows the results of the voting in real time


## Deployment

To deploy this project run

```bash
  kubectl create -f Postgres-deployment.yaml
  kubectl create -f Postgres-service.yaml
  kubectl create -f Redis-deployment.yaml
  kubectl create -f Redis-service.yaml
  kubectl create -f Result-app-deployment.yaml
  kubectl create -f Result-app-service.yaml
  kubectl create -f Voting-app-deployment.yaml
  kubectl create -f Voting-app-service.yaml
  kubectl create -f Worker-app-deployment.yaml
```

