# Configure Hadoop Cluster Using Ansible(Automation Tool)
### I have setup hadoop cluster on aws ec2-instance(linux os) and **namenode** on ansible controller node that is also an ec2-instance and datanode on other two ec2-instance

## By Making Some Changes in hostfile you can setup in your own private systems

## For Running in Your Local System, You have to Perform some simple tasks
1. In **hostfile** 
   - change ansible_user = root
   - remove *ansible_ssh_private_key=keyname* from [slave] group and write there ansible_ssh_password=passwrord 
   - write ip of machines that you want to configure as datanode in [slave] group of hostfile
   - if you want to configire more datanode then add same line but with different node ip , password 
2. Download [jdk](https://drive.google.com/file/d/17UWQNVdBdGlyualwWX4Cc96KyZhD-lxz/view?usp=sharing) an [hadoop](https://drive.google.com/file/d/1541gbFeGZZJ5k9Qx65D04lpeNBw87rM5/view?usp=sharing)
   - copy both hadoop and jdk rpm file in hadoop_master/files/, hadoop_slaves/files/ folder
