# In short run below:
 - git clone https://github.com/atingupta2005/ansible-demo.git
 - cd ansible-demo
 - sudo apt -y install software-properties-common
 - sudo apt-add-repository ppa:ansible/ansible
 - sudo apt update
 - sudo apt install ansible

# ssh-keygen
 - ssh-keygen -f ~/.ssh/demo_id_rsa
 - chmod 0600 ~/.ssh/demo_id_rsa

# Update Hosts:
 - vim hosts

# Update SSH Key File Path:
 - vim hosts

# Deploy Public Key to host
 - ssh-copy-id -i ~/.ssh/demo_id_rsa.pub demouser@<ipaddress>
 - ssh-copy-id -i ~/.ssh/demo_id_rsa.pub demouser@<ipaddress>

# Test the key
 - ssh -i ~/.ssh/demo_id_rsa demouser@<ipaddress>

# Test Ansible is able to conenct to all hosts
 - ansible all  --module-name ping -u demouser

# Running ad hoc commands
- ansible all -a uptime
- ansible all -a "free -m"
- ansible all -a "df -h"



 
 
