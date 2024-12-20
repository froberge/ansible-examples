## GitHub Playbooks

Theses playbooks were created to show how we can interact with the GitHub API

You can fin the [GitHub API here](https://docs.github.com/en/rest/repos/webhooks?apiVersion=2022-11-28)


#### Available playbooks
* [List repository for a user](list_user_repositories.yml)
* [Create webhook on repository](create_webhook_for_repo.yml)
* [Delete webhook on repository](delete_webhook_on_repository.yml)
* [Update webhook configs](update_config_webhooks.yml)

#### Required

Different element for python and ansible need to be added in order to execute this outside of an execution environment.

The Ansible collection:
* None

The python libraries:
* jmespath
``` pip install jmespath ```

#### Execute

:warning: Lot's of var have been externalize to represent running in a real environment, they must be provider to the playbook in order to work.

:exclamation: __COPY__ the file `inventory/github_values.yml` into a local file like `github_values-local.yml` and use that to provide the variable to the playbooks.

```
ansible-playbook -i inventory/github_values-local.yml [desired playbook]
```