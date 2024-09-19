## AWS Execution environment, Playbook and Roles

This repository contain different element to interact with AWS, from the creation of and Execution environment, These playbook or role are use to manage element inside and AWS environment.



#### Available playbooks
* 

#### Required

This playbook requires the jmespath to be install.
```
pip3 install jmespath
```

#### Execute

:warning: Lot's of var have been externalize to represent running in a real environment, they must be provider to the playbook in order to work.


:exclamation: You can copy the file `inventory/github_values` to a local file ex:`inventory/github_values-local.yaml` and use that to provide the variable to the playbooks.


```
ansible-playbook -i inventory/github_values-local.yml [desired playbook]
```