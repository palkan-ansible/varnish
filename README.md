Varnish
========

Installs Varnish.

Installation
--------------

`ansible-galaxy install palkan.varnish`

Role Variables
--------------

`defaults/main.yml`

| Name                        | Default Value |  Description    |
|-----------------------------|---------------|-----------------|
| varnish_vcl_tpl              | "default.vcl.j2"        | Path to VCL config |
| varnish_ulimit                 | 131072 | Open files | 
| varnish_memlock                 | 82000 | Maxiumum locked memory size for shared memory log |
| varnish_listen_port             | 80 | |
| varnish_admin_port              | 6082 | |
| varnish_malloc_size             | 1G | | 
| varnish_backend_host            | "127.0.0.1" | _For default VCL_ |
| varnish_backend_port            | "8080" | _For default VCL_ |
| varnish_backend_max_connections | 300 | _For default VCL_ |

Example Playbook
-------------------------
```yml
  - hosts: servers
    roles:
       - palkan.varnish
```
