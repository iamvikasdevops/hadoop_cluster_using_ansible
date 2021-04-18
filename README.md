# Configure Hadoop Cluster Using Ansible(Automation Tool)
## For Running in Your Local System, You have to Perform some simple tasks
1. In **hostfile** 
   - change ansible_user = root
   - remove *ansible_ssh_private_key=keyname* from [slave] group and write there ansible_ssh_password=passwrord , here you have to write the password of the machine or os in which you want to run playbook a
