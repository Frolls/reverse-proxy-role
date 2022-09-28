Reverse-proxy
==============

Reverse proxy с поддержкой TLS для обеспечения безопасного доступа к веб-сервисам по HTTPS

Role Variables
--------------

Необходим словарь со списком серверов:

```yml
---
web_servers:
  - name: <server_name>
    ip: <server_ip>
...
```

Example Playbook
----------------

Пример использования:

```yml
- name: Reverse-proxy
  hosts: proxy
  become: true
  vars_files:
    - group_vars/web_servers.yml
  roles:
    - role: reverse-proxy
...
```

License
-------

BSD

Author Information
------------------

Frolls