Sysdig
=========
This role installs the [Sysdig](http://www.sysdig.org/) monitoring tool.


Requirements
------------
If installing as a Docker container then this roles assumes that Docker is running on the specified hosts. Apart from this no special requirements.


Variables
---------
``sysdig_install_type``: Specify what kind of installation do you want. By default sysdig will be installed as a traditional application on the host system. If you want sysdig to be running as a Docker container then provide this variable with 'container' as the value.


Example Playbook
----------------
If you want a traditional sysdig install:

    - hosts: servers
      roles:
         - { role: rsjethani.sysdig }

If you want to install sysdig as a Docker container:

    - hosts: servers
      roles:
         - { role: rsjethani.sysdig, sysdig_install_type: "container" }


License
-------
MIT


Author Information
------------------
Ravi Shekhar Jethani <rsjethani@gmail.com>
