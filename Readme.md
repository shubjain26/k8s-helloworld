0. Setup Kubernetes Cluster

1. Build and Push Docker images
    make buildd
    make pushd

2. Create k8s secret
    kubectl create secret docker-registry NEW-SECRET-NAME --docker-server=docker.io --docker-username=USERNAME --docker-password=PASS --docker-email=USER_EMAIL@EXAMPLE.COM

3. Apply spec file, pod or deployment (either one)
    - kubectl apply -f pod_helloworld.yml
    - kubectl apply -f deployment_helloworld.yml

4. Open the port in the VM and test
    Refresh the page and notice hostname changes