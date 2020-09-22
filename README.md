# ansible scripts for auto deploying some services.
### What you should do first
* You must setup passwordless SSH login for you servers, https://linuxize.com/post/how-to-setup-passwordless-ssh-login/
* You need to edit the file templates/hosts to use you server ips.

### deploy-rocketmq.yaml 
* It is for deploying RocketMQ, sample command is ``` ansible-playbook -i templates/hosts deploy-rocketmq.yaml -e "env=dev" ```.
* use the ``` -e "env=dev" ``` argument can setup a RocketMQ cluster of lower jvm heap memory(512M) for developping or testing.

### deploy-zk.yaml 
* It is for deploying ZooKeeper, sample command is ``` ansible-playbook -i templates/hosts deploy-zk.yaml ```.
