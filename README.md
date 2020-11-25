# ansible scripts for auto deploying some tools.
### What you should do first
* You must install ansible first, https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html
* You must setup passwordless SSH login for the servers, https://linuxize.com/post/how-to-setup-passwordless-ssh-login/
* You need to edit the file ```templates/hosts``` to replace with your servers' ips.

### About deploy-rocketmq.yaml 
* It is for deploying RocketMQ Broker and NameServer cluster with a gui console, then run the playbook, like this:
        ``` ansible-playbook -i templates/hosts deploy-rocketmq.yaml -e "env=dev" ```
* use the ``` -e "env=dev" ``` argument to setup a RocketMQ cluster with lower jvm heap memory(512M) for developping or testing.

### About deploy-zk.yaml 
* It is for deploying ZooKeeper, run the playbook, like this: 
        ``` ansible-playbook -i templates/hosts deploy-zk.yaml ```.
