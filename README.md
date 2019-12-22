## Ansible

```bash
brew install ansible
ansible all --user root -i hosts -m ping
```

## Playbook

```
ansible webservers -m apt -a "name=mysql-server state=present"
ansible webservers -m apt -a "name=python3 state=present"

ansible-playbook server.yml
ansible-playbook postgres.yml -e "postgresql_version=9.3"
ansible-playbook hello.yml
```

## Shell

```
ansible -m shell -a hostname all
ansible -m shell -a 'df -h' all
ansible -m shell -a 'whoami' all
```

## Role

```bash
ansible-playbook playbooks.yml
```