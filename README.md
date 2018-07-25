[![Build Status](https://travis-ci.org/while-true-do/ansible-role-repo-jenkins.svg?branch=master)](https://travis-ci.org/while-true-do/ansible-role-repo-jenkins)

# Ansible Role: repo-jenkins
| A role that configures the yum repository for Jenkins continuous integration and continuous delivery application.

## Motivation

This role is needed to provide the Jenkins packages.

## Installation

Install from [Ansible Galaxy](https://galaxy.ansible.com/while_true_do/repo_jenkins)

```
ansible-galaxy install while_true_do.repo_jenkins
```

Install from [Github](https://github.com/while-true-do/ansible-role-repo-jenkins)

```
git clone https://github.com/while-true-do/ansible-role-repo-jenkins.git while_true_do.repo_jenkins
```

## Requirements

Used Modules:

-   [command_module](https://docs.ansible.com/ansible/latest/modules/command_module.html)
-   [include_tasks_module](https://docs.ansible.com/ansible/latest/modules/include_tasks_module.html)
-   [rpm_key_module](https://docs.ansible.com/ansible/latest/modules/rpm_key_module.html)
-   [yum_repository_module](https://docs.ansible.com/ansible/latest/modules/yum_repository_module.html)

## Dependencies

This role has the below dependencies:

-   <https://galaxy.ansible.com/while_true_do/yum>

You can install them with:

```
ansible-galaxy install -r requirements.yml
```

## Role Variables

```yaml
# defaults/main.yml for repo_jenkins

# repository state can be set to "present" / "absent"
wtd_repo_jenkins_state: "present"
```

## Example Playbook

Simple Example:

```yaml
- hosts: servers
  roles:
    - { role: while_true_do.repo_jenkins }
```

Advanced Example:

```yaml
- hosts: servers
  roles:
    - { role: while_true_do.repo_jenkins, wtd_repo_jenkins_state: "absent" }
```

## Testing

All tests are located in [test directory](./tests/).

Basic testing:

```
bash ./tests/test-ansible.sh
bash ./tests/test-spelling.sh
bash ./tests/test-whitespace.sh
```

## Contribute / Bugs

Thank you so much for considering to contribute. Every contribution helps us.
We are really happy, when somebody is joining the hard work. Please have a look
at the links first.

-   [Code of Conduct](./docs/CODE_OF_CONDUCT.md)
-   [Contribution Guidelines](./docs/CONTRIBUTING.md)
-   [Create an issue or Request](https://github.com/while-true-do/ansible-role-repo-jenkins/issues)
-   [See who was contributing already](https://github.com/while-true-do/ansible-role-repo-jenkins/graphs/contributors)

## License

This work is licensed under a [BSD License](https://opensource.org/licenses/BSD-3-Clause).

## Author Information

Site: [while-true-do.org](https://while-true-do.org)

Mail: [hello@while-true-do.org](mailto:hello@while-true-do.org)
