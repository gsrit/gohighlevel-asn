
# DevOps Assignment (K8, Terraform,Wordpress)


Task:
- :heavy_check_mark: Provision a highly available kubernetes cluster on Google Cloud or AWS or any other cloud. 
- :heavy_check_mark: Create a simple wordpress site and  deploy it on the kubernetes cluster.
- :heavy_check_mark: Create a mechanism so that webservice pod scales down to zero if there is no traffic on the page and automatically scales up if there is traffic (ignore the initial delay from 0 to 1 pod)
- :heavy_check_mark: Configure the deployment to have FTP access.
- :heavy_check_mark: Provision the above infrastructure using terraform ( Deployment of pods through terraform is not required )


Detailed Information.

- Provision a highly available kubernetes cluster on Google Cloud or AWS or any other cloud.

Status : The GKE Cluster is provisioned using terraform, refer terrform files.

- Create a simple wordpress site and  deploy it on the kubernetes cluster.

Status: Facing issue with the Loadbalancer while exposing the app to internet ,  the app is provisioned on the GKE Cluster successfully but still unmanaged.

- Create a mechanism so that webservice pod scales down to zero if there is no traffic on the page and automatically scales up if there is traffic

