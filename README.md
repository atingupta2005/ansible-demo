# Installation:
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

# Validate and obtain information about your Ansible inventory
 - ansible-inventory -i hosts --list

# Deploy Public Key to host
 - ssh-copy-id -i ~/.ssh/demo_id_rsa.pub demouser@138.91.140.75
 - ssh-copy-id -i ~/.ssh/demo_id_rsa.pub demouser@40.83.249.79

# Test the key
 - ssh -i ~/.ssh/demo_id_rsa demouser@host1

# Test Ansible is able to conenct to all hosts
 - ansible all -i hosts -m ping

# Running ad hoc commands
- ansible all -a uptime
- ansible all -a "free -m"
- ansible all -a "df -h"

# Running Playbook
- vim first_playbook.yml
- ansible-playbook -i hosts first_playbook.yml

# Confirm content of the file in all hosts
- ansible all -a "cat /tmp/testfile.txt"
