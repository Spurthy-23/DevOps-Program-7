
# Program 7 - Deploy Web Application to Kubernetes Using Minikube

## Objective
To deploy a simple Nginx web application on a local Kubernetes cluster using Minikube.

## Technologies Used
- Docker
- Kubernetes
- Minikube
- kubectl
- Nginx
- Ubuntu Linux

## Steps to Execute

### 1. Start Minikube
```bash
minikube start --driver=docker
```

### 2. Check Minikube Status
```bash
minikube status
```

### 3. Deploy the Application
```bash
kubectl apply -f nginx-deployment.yaml
```

### 4. Check Deployments
```bash
kubectl get deployments
```

### 5. Check Pods
```bash
kubectl get pods
```

### 6. Expose the Application
```bash
kubectl expose deployment nginx-deployment --type=NodePort --port=80
```

### 7. Check Services
```bash
kubectl get services
```

### 8. Open the Application
```bash
minikube service nginx-deployment
```

## Expected Output
The Nginx welcome page should open in the web browser.

## Cleanup
```bash
kubectl delete svc nginx-deployment
kubectl delete deployment nginx-deployment
```
