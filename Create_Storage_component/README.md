

# This File explains how to run a YAML file to configure Storage components.

## User Pre-requisites:
VSP One Object User permission should have permissions to make changes on storage components by being part of the group S3_Administrator
Storage Node user should also have administrative rights.

## 1. Enter the VSP One Object details and the S-Node Storage components details in the file:
   open file S-node_storage_component_vars.yml ,
   located in the same directory


   ### Required fields:
   - cluster_name: "provide your VSP One Object"
   - region: "provide region of VSP One Object"
   - oneobject_node_username: "user of VSP One Object"
   - oneobject_node_userpass: "user password of VSP One Object"

	example:
	cluster_name: "vsponeobject.content.local"
   	region: "us-west-2"
   	oneobject_node_username: "adminuser"
   	oneobject_node_userpass: "<Password>"

   ### Mandatory Storage Component Details to be entered in :
   - s_node_bucket: "Name of the bucket created at storage node"
   - storage_component_name: "Label for storage component in VSP One Object"
   - s_node_endpoint_host: "Storage component FQDN"
   - storage_fault_domain: "Fault domain on VSP One Object used by Storage component"
   - s_node_region: "Region of the Storage node"
   - s_node_access_key: "Access key of a Storage node user"
   - s_node_secret_key: "Secret key of a Storage node user"
   - s_node_management_user: "User of Storage node"
   - s_node_management_password: "Password of Storage node user"
	
	example:
	s_node_bucket: "s3bucket"
	storage_component_name: "S-node"
	s_node_endpoint_host: "s31.content.local"
	storage_fault_domain: "test-domain"
	s_node_region: "us-east-1"
	s_node_access_key: "<accessKey>"
	s_node_secret_key: "<SecretKey>"
	s_node_management_user: "admin"
	s_node_management_password: "<Password>"

### 2. To trigger the YAML file to create the storage component:

   - Locate the YAML file: Create_S-node_storage_component.yml
   - Run the following command:

     		ansible-playbook Create_S-node_storage_component.yml
