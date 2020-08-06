# Move kubernetes workload between clusters.

Run ``` kubectl proxy --context source-cluster-context ```
Run ``` kubectl proxy --port 8011 --context destination-cluster-context ```

Run the script.

tsc && node /dist/index.js  cluster123-d cluster456 --ns sg-test

# Docker

Run as a docker container

``` docker run -v {path to kubeconfig file}:/cfg/config gr4b4z/kubemover  -s {source context} -d {destination context} --ns {namespace} ``` 

Examples:

``` 
docker run -v ~/.kube/config:/cfg/config gr4b4z/kubemover  -s cluster123 -d cluster456 --ns mynamespace 

docker run -v ~/.kube/config:/cfg/config gr4b4z/kubemover  -s cluster123 -d cluster456 --ns mynamespace --ns mynamespace2

docker run -v ~/.kube/config:/cfg/config gr4b4z/kubemover  -s cluster123 -d cluster456 --ns mynames*

``` 


