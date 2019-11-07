## pod needs permissions to call api server

`kubectl create clusterrolebinding --user system:serviceaccount:default:default xxx --cluste rrole cluster-admin`

## to run image on k8s

compile frontend to go file running

`npm run build --prefix web-client`
`statik -src=./web-client/build`

```
# Start minikube
minikube start

# Set docker env
eval $(minikube docker-env)

# Build image
docker build -t foo:0.0.1 .

# Run in minikube
kubectl run hello-foo --image=foo:0.0.1 --image-pull-policy=Never

# Check that it's running
kubectl get pods
```