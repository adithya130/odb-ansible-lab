## Prepare Environment
```
git config --global user.email "adithya@sapphirehealth.org"
git config --global user.name "Adithya Pugazhendhi"
export ANSIBLE_CONFIG=$(pwd)/ansible.cfg
```

## List Inventory
```
ansible-inventory --list --yaml | more
```

## Prepare Environment
```
source ~/venv/azure/bin/activate
. .env
```

## Ping Linux Host
```
ansible -m ping all --limit azure_rm_linux
```

## Ping Windows Host
```
ansible -m win_ping all --limit azure_rm_windows
```

## Run Ansible variables Playbook
```
ansible-playbook ansible-vars.yml
```

## Read file content using ad-hoc ansible command
```
ansible -m ansible.builtin.command -a "cat /tmp/ip.txt" all
```

## Run public IP Playbook
```
ansible-playbook --limit ODBTST public-ip.yml
```