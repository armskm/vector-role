Vector
=========

Эта роль устанавливает и настраивает Vector на Debian 12.

Requirements
------------

ansible_version: 2.12

Role Variables
--------------

| vars | Description | Value | Location |
|------|------------|---|---|
| vector_version | Версия Vector | "0.44.0" | defaults/main.yml |
| vector_config_path | Путь до файла конфигурации Vector | "/etc/vector/vector.yaml" | defaults/main.yml |
| clickhouse_host | Local ip сервера clickhouse | <Обязательно указать> | defaults/main.yml |

Example Playbook
----------------

```yml
---
- name: Install Clickhouse
  hosts: clickhouse
  roles:
    - clickhouse
- name: Install Vector
  hosts: vector
  roles:
    - vector
- name: Install lighthouse
  hosts: lighthouse
  roles:
    - lighthouse
```

License
-------

MIT
