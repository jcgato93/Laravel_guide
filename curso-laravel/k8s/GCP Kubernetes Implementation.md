# GCP Kubernetes Implementation

## Step by Step

1. Create a name space

    - get the current namespaces

            $ kubectl get ns

    - Apply namespace file

            $ kubectl apply -f 01-name-space.yml


### Deploy App

1. Apply deployment with a LoadBalancer and ClusterIP services in the
specific namespace

            $ kubectl -n production apply -f 02-deployment-app.yml    
