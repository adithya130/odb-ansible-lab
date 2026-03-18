## Prepare Environment
```
git config --global user.email "adithya@sapphirehealth.org"
git config --global user.name "Adithya Pugazhendhi"
export ANSIBLE_CONFIG=$(pwd)/ansible.cfg
```

## List Static Inventory
```
ansible-inventory -i inventory.yml --list --yaml
```

## Prepare Environment
```
source ~/venv/azure/bin/activate
. .env
```

## Ping Linux Host
```
ansible -i inventory.yml -m ping all
```