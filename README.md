# Ansible IPTABLES role

## What it does
Manages iptables rules

## Usage
Install in roles and call from playbook with:

```
- hosts: all
    - logstash
    - {
     role: iptables,
     action: ACCEPT,
     dports: [3000, 5671, 42022]
    }
```

## Notes
To persist the state of the firewall, the last action performed is always
an iptables-save to /etc/sysconfig/iptables
