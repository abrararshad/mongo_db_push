Anbiel Role
=========

Ansible role for pushing mongo database from the ansible controller to the remote machine
```
ansible-galaxy install abrararshad.mongo_db_push
```

Role Variables
--------------

```
mongo_db_push_remote_dump_path: '/tmp/mongo_dump'
mongo_db_push_data_path: ''
mongo_db_push_user_name: ''
mongo_db_push_user_pass: ''
```

Specify where the location of the data on local machine/ansible controller, it will zip before copying the database

```
mongo_db_push_data_path: '/tmp/data'
```

Example
----------------

```
---
- name: 'Mongo db push'
  hosts: "all"
  roles:
    - name: abrararshad.mongo_db_push
      vars:
        mongo_db_push_data_path: '/tmp/playbook/data/wefiq'
        mongo_db_push_user_name: admin
        mongo_db_push_user_pass: "{{ app_mongo_admin_pass }}"

```

License
-------

BSD
