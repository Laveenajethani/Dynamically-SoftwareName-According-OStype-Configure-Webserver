# Dynamically SoftwareName Take According OStype and Configure Webserver

#### I have two traget nodes one traget node is running in my local VM which is redhat8 and another trarget node in running in the AWS cloud service ec2 this traget node is Ubuntu OS .

## This target node 1 : Redhat OS
<img src="Screenshots/local_target_node.png">

## This target node 2 : Ubuntu OS : ec2 instance
<img src="Screenshots/traget_node_ubuntu_ec2.PNG" >

## In controller node I have inventory file in which I have mentioned the target node IP and other information

<img src="Screenshots/inventory.PNG" >

## This is ansible.cfg file

<img src="Screenshots/ansible_cfg.PNG">

In my second target node ansible login using SSH with the ubuntu user power but some task will perform using root power so in my inventory file I have mentioned the keyword [privilege_escalation] .

#### In my target node I want to configure the webserver so target nodes are redhat and ubuntu OS so apache webserver software name is different for both the OS so  my ansible playbook will dynamically take software name according to OS type for this I have created two files RedHat.yml & Debian.yml .

## Debian.yml (for ubuntu OS)
<img src="Screenshots/Debian.yml.png">

## RedHat.yml (for RedHat OS)
<img src="Screenshots/RedHat.yml.png">
