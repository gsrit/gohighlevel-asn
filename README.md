
# DevOps Assignment (K8, Terraform,Wordpress)


Task:
- Provision a highly available kubernetes cluster on Google Cloud or AWS or any other cloud. 
- Create a simple wordpress site and  deploy it on the kubernetes cluster.
- Create a mechanism so that webservice pod scales down to zero if there is no traffic on the page and automatically scales up if there is traffic (ignore the initial delay from 0 to 1 pod)
- Configure the deployment to have FTP access.
- :heavy_check_mark: Provision the above infrastructure using terraform ( Deployment of pods through terraform is not required )


Detailed Information.

- **Provision a highly available kubernetes cluster on Google Cloud or AWS or any other cloud.**

Status : The GKE Cluster is provisioned using terraform, refer terrform folder/files.

- **Create a simple wordpress site and  deploy it on the kubernetes cluster.**

Status: Wordpress app was deployed using manifest files ,kindly refer the files in kubernetes folder for the manifest that was used to deploy the wordpress app.

- **Create a mechanism so that webservice pod scales down to zero if there is no traffic on the page and automatically scales up if there is traffic**

Status: Could't configure the scale down to zero mechanism, it will require additional time as I would do it using the KEDA 
Kubernetes will allow the scaling to zero only by calling API and the Horizontal Pod Autoscaler will allow scaling down to only one replica.

- **Configure the deployment to have FTP access.**

**GUI Method**
 
Status: FTP Access to the wordpress can be configured using the Control Panel, steps required are as below.
1. Access the setting/control panel of the wordpress.
2. Add the user credentials for FTP Access.
3. Define the directories to be access over FTP.
4. 

**wp-config.php**
Open the File Manager or FTP access to view and edit the wp-config.php file. 
This file is located in the top directory of the account, listed above the /wp-content directory.

```
define('WP_DEBUG', false);

define('FTP_USER', 'gaurav');
define('FTP_PASS', '*******');
define('FTP_HOST', 'gauravrtr.in:21');
define('FTP_SSL', false);
```


:heavy_check_mark:
