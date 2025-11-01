# ExplorViz K8S Deployment

## Prerequisites

Make sure you have the following installed:

- [Docker](https://docs.docker.com/get-docker/)
- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [kubectl](https://kubernetes.io/docs/tasks/tools/)
- [Helm](https://helm.sh/docs/intro/install/)

# 1. Start Minikube

`minikube start`

Verify the cluster is running:

`kubectl get nodes`

# 2. Deploy Helm Chart

When doing this the first time, you need to install the Helm charts:

`helm upgrade --install explorviz ./observability-demo`

Check that everything is running:

`kubectl get pods`

# 3. Add a Port-Forward to Access the ExplorViz Frontend

Once your application’s service is running, forward port to an available port (e.g. port 8080):

`kubectl port-forward service/frontend 8080:80`

Now, open your browser and go to:

http://localhost:8080
