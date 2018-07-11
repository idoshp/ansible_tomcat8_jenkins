
#### Description

- The playbook will install tomcat8 on target server, install Jenkins and mount Jenkins workspace to AWS S3 bucket


#### prerequisites

- Ansible Installed >v2.4.
- Store the .pem key file of the target server in the Ansible server where you execute the playbook.
- Create inventory.ini file with the following:
-   [node1]
-   (public dns) ansible_ssh_user=(target user)
- create a bucket in AWS S3 using a new IAM user with S3 privileges. 
- update group_vars/tomcat-servers with your local parameters.

#### Installation

- execute the playbook: ansible-playbook -i inventory.ini tomcat.yml --private-key (path to key file)
