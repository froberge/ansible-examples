## AWS Execution environment, Playbook and Roles

This repository contain different element to interact with AWS, from the creation of and Execution environment, These playbook or role are use to manage element inside and AWS environment.


#### Available playbooks
* [Create AWS EC2 infra](create_aws_ec2_infra.yml)
* [Delete AWS EC2 infra](delete_aws_ec2_infra.yml)* [Install a Load Balancer](install_lb.yml)
* [Install a Web Server](install_ws.yml)
* [Test Connection to VM](test_connections.yml)
* 

#### Required

Different element for python and ansible need to be added in order to execute this outside of an execution environment.

The Ansible collection:
* Amazon Certify 
``` ansible-galaxy collection install amazon.aws ```

The python libraries:
* None

#### Execute:warning: Lot's of var have been externalize to represent running in a real environment, they must be provider to the playbook in order to work.

:exclamation: __COPY__ the file `inventory/values.yml` into a local file like `values-local.yml` and use that to provide the variable to the playbooks.

```
ansible-playbook -i inventory/values-local.yml [desired playbook]
```