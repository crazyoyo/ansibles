# ansible scripts for auto deploying some services.
### What you should do first
* You must install ansible firstly, https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html
* You must setup passwordless SSH login for the servers, https://linuxize.com/post/how-to-setup-passwordless-ssh-login/
* You need to edit the file ```templates/hosts``` to replace with your servers' ips.

### deploy-rocketmq.yaml 
* It is for deploying RocketMQ Broker and NameServer cluster with a gui console, the sample command is ``` ansible-playbook -i templates/hosts deploy-rocketmq.yaml -e "env=dev" ```.
* use the ``` -e "env=dev" ``` argument can setup a RocketMQ cluster of lower jvm heap memory(512M) for developping or testing.

### deploy-zk.yaml 
* It is for deploying ZooKeeper, sample command is ``` ansible-playbook -i templates/hosts deploy-zk.yaml ```.
