### Edit Inventory file

	[keystone]
	controller		ansible_connection=ssh		ansible_user="{{ user | default('user') }}" ansible_become=true

Define appropriate host name instead of 'controller'

### Run playbook
	ansible-playbook -vvv -i hosts --extra-vars "user=username mysql_root_password=root mysql_keystone_password=keystone server_name=controller" install.yml

Specify appropriate user name (assuming that user can ssh to the host using public key authentication and do 'sudo' without password), password for MySQL root user and password for Keystone user (assuming that username is 'keystone').
