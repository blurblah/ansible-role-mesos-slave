# ansible-role-mesos-slave
This role supports only for Ubuntu 14.04 and 16.04 and tested on Ansible version 2.4.2

## Playbook sample
This playbook installs mesos-slaves.
```yaml
- hosts: mesos-slaves
  become: yes
  roles:
    - role: mesos-slave
      mesos_masters:
        - { host: 192.168.0.10, zk_port: 2181 }
        - { host: 192.168.0.11, zk_port: 2181 }
        - { host: 192.168.0.12, zk_port: 2181 }
```
