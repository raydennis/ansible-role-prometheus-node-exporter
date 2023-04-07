# Ansible role to install a Prometheus node_exporter service on RHEL based hosts

## Example playbook

```yaml

# run: ansible-playbook -i ./inv/${CLUSTER}/hosts ./pb_prometheus-node-exporter.yml --extra-vars="target=all:h!reservable_hosts" -u root
---
- name: Install Prometheus Node Exporter service
  hosts: '{{ target | default("noname.example.com") }}'

  roles:
    - ansible-prometheus-node-exporter 
```
