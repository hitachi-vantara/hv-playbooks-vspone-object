

# This File explains how to run a YAML file to configure Storage components.

User Pre-requisites:
VSP One Object User permission should have permissions to make changes on storage components by being part of the group S3_Administrator
Storage Node user should also have administrative rights.

## 1. Enter the VSP details and Storage components details in the file:
   s3_bucket_vars.yml


   ### Required fields:
   - cluster_name: "provide your VSP One Object"
   - region: "provide region of VSP One Object"
   - oneobject_node_username: "user of VSP One Object"
   - oneobject_node_userpass: "user password of VSP One Object"
   - s3_bucket_name: "Provide bucket name"
   - enable_object_lock: "enter true if object lock is needed or else enter false"
   - s3_endpoint: "Enter S3 service endpoint url"
   - access_key: "Enter Access key"
   - secret_key: "Enter Secret key"

	example:
	cluster_name: "vsponeobject.content.local"
   	region: "us-west-2"
   	oneobject_node_username: "administrator"
   	oneobject_node_userpass: "Password123"
    s3_bucket_name: "ansibelbucket"
    enable_object_lock: "false"
    s3_endpoint: "https://s3.cluster01.vmvsp1o1.gpsecontent.local"
    access_key: "AKIAIcZZKXpft93GBA"
    secret_key: "ZDAwM2ZkYN2MxZ00ZTQ35VrfJmODEtMGU4Mzg1"
   
### 2. To trigger the YAML file to create the storage component:
   - Locate the YAML file: s3_bucket.yml
   - Run the following command:

     		ansible-playbook s3_bucket.yml
