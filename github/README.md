## This playbook was created to sample how we can interact with the GitHub API

You can fin the [GitHub API here](https://docs.github.com/en/rest/repos/webhooks?apiVersion=2022-11-28)


#### Available playbooks
* [List repository for a user](list_user_repositories.yml)
* [Create webhook on repository](create_webhook_for_repo.yml)
* [Delete webhook on repository](delete_webhook_on_repository.yml)

#### Required

This playbook requires the jmespath to be install.
```
pip3 install jmespath
```

#### Execute

:warning: Before you try to execute this you need to make sure you have made a copy of the file `inventory/github_values` to a file call `inventory/github_values-local.yaml` with you own values.

```
ansible-playbook -i inventory/github_values-local.yml [desired playbook]
```