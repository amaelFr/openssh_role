amaelFr.openssh
=========

A role to manage openssh on linux

Requirements
------------

Role Variables
--------------

cf defaults main.yml

Dependencies
------------


Example Playbook
----------------


    - hosts: servers
      roles:
        - role: amaelFr.openssh
          openssh_global:
            PasswordAuthentication: true
            PermitRootLogin: true
            AuthenticationMethods:
              - password
              - publickey
          openssh_match:
            - Match:
                - type: User
                  value:
                    - ansible
              PasswordAuthentication: false
              AuthenticationMethods:
                - publickey

License
-------

BSD

Author Information
------------------
amaelFr
