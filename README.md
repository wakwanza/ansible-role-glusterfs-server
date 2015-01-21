GlusterFS Server
================

Sets up a group of nodes with glusterfs.

Requirements
------------

epel and glusterfs repositories.will be installed by the play if not available

Role Variables
--------------

- data_dir : Data directory for the filesystem brick to mount (eg /data)
- dev_path: Path of the device to be formatted as the data brick (eg /dev/sdb)
- replica_set: how many replicas to keep

Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: ansible-role-glusterfs-server,  data_dir: /data ,  dev_path: /dev/sdb , replica_set: 2}

License
-------

BSD

Author Information
------------------

@wakwanza