0. Setup Kubernetes Cluster

1. Build and Push Docker images
    make buildd
    make pushd

2. Create k8s secret
    kubectl create secret docker-registry NEW-SECRET-NAME --docker-server=docker.io --docker-username=USERNAME --docker-password=PASS --docker-email=USER_EMAIL@EXAMPLE.COM

Apply Pod Spec
3. Apply pod spec file
    kubectl apply -f pod_helloworld.yml

OR 

Apply Deployment Spec
3. Apply Deployment spec file
    kubectl apply -f deployment_helloworld.yml

4. Open the port in the VM and test
    Refresh the page and notice hostname changes