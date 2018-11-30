wrlc-mariadb
=========

DRAFT! Installs mariadb if not installed. DRAFT! 

Role Variables
--------------
| Variable | Default | Comments |
|----------|---------|----------|
| mariadb_datadir | /var/lib/mysql | change the data diretory for the mysql server if desired |
| mariadb_tempdir | /tmp | |
| mariadb_bind_address | 127.0.0.1 | |
| mariadb_port | 3306 | |
| mariadb_key_buffer_size | '16M' | |
| mariadb_max_allowed_packet | '16M' | |
| mariadb_thread_stack | '192K' | |
| mariadb_thread_cache_size | '8' | |
| mariadb_query_cache_limit | '1M' | |
| mariadb_query_cache_size | '16M' | |
| mariadb_root_password | none | mariadb root password set this in your host vars|

Dependencies
------------

None.

Example Playbook
----------------

    ---
    - name: wrlc-mariadb
      hosts: blank
      vars:
        mariadb_bind_address: '0.0.0.0'
      roles:
        - wrlc-mariadb
      become: true

License
-------

BSD
