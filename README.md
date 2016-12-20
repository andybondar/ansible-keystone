### Edit Inventory file

	[keystone]
	controller		ansible_connection=ssh		ansible_user="{{ user | default('user') }}" ansible_become=true

Define appropriate host name instead of 'controller'

### Run playbook
	ansible-playbook -vvv -i hosts --extra-vars "user=username" install.yml

Specify appropriate user name (assuming that user can ssh to the host using public key authentication and do 'sudo' without password)
