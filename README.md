# Ansible-lab  
  - 1) root@:~/Ansible-lab# git clone https://github.com/omriv88/Ansible-lab.git
  - 2) root@:~/Ansible-lab# ./setup-ubuntu.sh
     
    ----------------------------
    - Ansible Port is
    - Node 1 Port is 49157
    - Node 2 Port is 49158
    ----------------------------
 - 3) root@:~/Ansible-lab# ssh-keygen
 - 4) root@:~/Ansible-lab# ssh-copy-id -p 49157 localhost
 - 5) root@:~/Ansible-lab# ssh-copy-id -p 49158 localhost
 - 6) root@:~/Ansible-lab# ansible servers -m ping
 
    - node1 | SUCCESS => {"changed": false,"ping": "pong"} 
    - node2 | SUCCESS => {"changed": false,"ping": "pong"}
