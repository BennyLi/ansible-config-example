# Ansible Config Example

An example Ansible configuration to use with my [Ansible Playbook Skeleton](https://github.com/BennyLi/ansible-playbook-skeleton) scripts.

## How this works 🎓

This repo is meant to be used in conjunction with my scripts provided in my [Ansible Playbook Skeleton](https://github.com/BennyLi/ansible-playbook-skeleton) repository.
For a production ready setup you should create your own config repo by forking this repo and then modifing the files to your needs.
If you don't know what to do with the files in this repo, you should definitely take a look into the official Ansible documentation for like [Build Your Inventory](https://docs.ansible.com/ansible/latest/network/getting_started/first_inventory.html) and [Intro To Playbooks](https://docs.ansible.com/ansible/latest/user_guide/playbooks_intro.html) first.

## Vaults 🔐

For sensible data, I use the Ansible Vault.
To work with this data in a fluent way, I seperate my vault entries in an extra file and then reference the variables in my variables file.

In this repository you will find two `vault.yml` files, which are encrypted.
For example take a look into the `group_vars/servers` directory.

To see or edit them, use the `ansible-vault` tool and the password `password` _(for your vault, you should use a better password 🤷)_ like this:

```shell
ansible-vault edit group_vars/servers/vault.yml
```
