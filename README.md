ansible-playbook playbook.yml --ask-vault-pass

playbook.yml

The playbook's yml content and what each line does

Line 1: YAML documents start with ---

Line 2: Identifies the first play in the playbook

Line 3: Declare the hosts against which the playbook will run

Line 4: Activate privilege escalation

Lines 5-8: Specifies the set of roles that will be applied to the hosts 

Note
The content of the roles directory was automatically created

ansible-galaxy init disk_mgmt
ansible-galaxy init cpu_mgmt
ansible-galaxy init net_mgmt


Line 10: Introduce a list of tasks to be executed

Lines 11-13: Execute the lscpu command on the target 
and capture the output into a variable
Line 14 Suppress the change notification


Lines 16-22: Extract the lines from the output where 
indices are used to select specific lines in the lscpu output



inventory 

Line 1 Group name to organize hosts and apply tasks to multiple hosts 

Line 2 Define the host

Line 4 Define the group of hosts with specific variables

Line 5 Define the custom variable to be used in the disk_mgmt role




ansible.cfg

Line 1-3 Specifies the default location of the inventory file and path to store log output



group_vars/ubuntu_servers

Line 3 This defines the default user for all hosts in the group ubuntu_servers

Line 4 This defines the default private key for all hosts in the group ubuntu_servers


group_vars/all

Line 3 Disable the SSH host key verification globally

Line 4 Specify which Python interpreter to use