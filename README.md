cloud3rsio.os_user
=========

Create os user.

Installation
------------

```bash
$ ansible-galaxy install cloud3rsio.os_user
```

Requirements
------------

Nothing.

Role Variables
--------------

| Key | Default Value | Type |
| ------------- | ------------- | ------------- |
| `os_user` | Reference to [defaults/main.yml](defaults/main.yml) | Hash |
| `os_user.name` | `admin` | String |
| `os_user.password` | `password` | String |
| `os_user.homedir` | `/home/admin` | String |
| `os_user.generate_ssh_key` | `yes` | String |
| `os_user.additional_ssh_keys` | `[]` | Array |

Dependencies
------------

Nothing.

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: cloud3rsio.os_user
      os_user:
        name: admin-xxxx
        password: Passw0rd
        homedir: /home/admin-xxxx
        generate_ssh_key: yes
        additional_ssh_keys:
          - ssh-rsa AAAAB3NzaCxxxx....
          - ssh-rsa AAAAB3NzaCyyyy....
```

License
-------

[MIT](LICENSE)

Author Information
------------------

- youyo
