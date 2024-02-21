# ansible
# This the command to connect to the specified servers IP address
ansible -i 184.72.173.207, all -e ansible_user=centos -e ansible_password=DevOps321 -m ping
# Ansible adhco commands
ansible -i node.jiondevops.site, all --become -e ansible_user=centos -e ansible_password=DevOps321 -m ansible.builtin.yum -a "name=nginx state=present"

ansible -i node.jiondevops.site, all --become -e ansible_user=centos -e ansible_password=DevOps321 -m ansible.builtin.service -a "name=nginx state=started"
