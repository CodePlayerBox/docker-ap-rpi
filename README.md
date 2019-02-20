# docker-ap-rpi
配合scratch-link-node项目使用，用来将树莓当成一个AP使用。

## 构建运行

1. 在开发主机上，通过Ansible将代码同步到树莓派上
cd playbooks
ansible-playbook -i inventories/hosts deploy-to-rpi.yml

2. 在树莓派上，执行下面的命令进行构建
cd ~/CodePlayerBox/docker-ap-rpi
docker-compose build

3. 进入script目录下，然后执行下面的命令启动
cd script
sudo ./docker_ap start wlan0
