ansible
=======

This repo consists of an Ansible playbook that can be used to upgrade IOS-XR nodes like ASR9K.

It has 2 tasks which uses custom modules I prepared. 
1. First module 'SFTP_Tansfer" is used to transfer software files to the nodes.
2. Second module 'Install' is used to perform cli actions 'admin install add', 'admin install activate' and 'admin install commit'

Note that both modules use a custom Python module 'Connect' that I wrote to connect to devices using Paramiko. Nothing fancy here, really.

The modules are written to be idempotent i.e. if file is already present on the node, it does not transfer that particular file.
If the software is already installed, no need to re-install.

Warning: This are very basic modules due to my limited Python skills. So use it at your own risk (if you need to). If you have any suggestions, please let me know.
