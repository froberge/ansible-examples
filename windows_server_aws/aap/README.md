## AWS Execution environment, Playbook and Roles

Here is an example how to create with ansible-playbool a AWS environment that will host a VM with a windows server install in it.


#### Available playbooks
* [Create Window Server](create_window_server.yml)
* [Delete Window Server](delete_window_server.yml)

#### Required

Different element for python and ansible need to be added in order to execute this outside of an execution environment.

The Ansible collection:
* Amazon Community.
 ``` ansible-galaxy collection install community.aws```
* Amazon Certify 
``` ansible-galaxy collection install amazon.aws ```

The python libraries:
* None

#### Execute

:warning: Lot's of var have been externalize to represent running in a real environment, they must be provider to the playbook in order to work.

:exclamation: __COPY__ the file `inventory/values.yml` into a local file like `values-local.yml` and use that to provide the variable to the playbooks.

```
ansible-playbook -i inventory/values-local.yml [desired playbook]
```