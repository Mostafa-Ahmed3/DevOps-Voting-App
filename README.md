# DevOps-Voting-App

Deploying app on Kubernetes
## Architecture

![Voting architecture excalidraw](https://github.com/user-attachments/assets/46d53d8b-7c49-4ac3-b5e9-5003926a124c)

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

