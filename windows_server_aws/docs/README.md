## AWS Execution environment, Playbook and Roles

Here is an example how to create with ansible-playbool a AWS environment that will host a VM with a windows server install in it.


#### Available playbooks
* [Create Window Server Demo](create_window_servers_demo.yml)
* [Delete Window Server Demo](delete_window_server_demo.yml)

#### Required

1. An AWS enviroment and credentials.
1. Different element for python and ansible need to be added in order to execute this outside of an execution environment.

    Ansible collection:
    * Amazon Community.
    ``` ansible-galaxy collection install community.aws```
    * Amazon Certify 
    ``` ansible-galaxy collection install amazon.aws ```

    Python libraries:
    * None

1. Create a Key Pairs in AWS and download the .pem file. Use that name for variable in the value-local.yml file.
![key_pair](images/key_pair.png)

1. Select which AMI to install. Currently this demo uses that one for windows.
![window_ami](images/window-ami.png)

1. Define the values-local.yml file.
:exclamation: __COPY__ the file `inventory/values.yml` into a local file like `values-local.yml` and use that to provide the variable to the playbooks. The following variable absolutely needs to be overwritten.
    * AWS_ACCESS_KEY_ID
    * AWS_SECRET_KEY
    * key_name
    * key_file



#### Execute

:warning: Lot's of var have been externalize to represent running in a real environment, they must be provider to the playbook in order to work. Make sure you have done the requirment step before.

```
ansible-playbook -i inventory/values-local.yml [desired playbook]
```