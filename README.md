# Ansible-lab  
  1) root@:~/Ansible-lab# git clone https://github.com/omriv88/Ansible-lab.git
  2) root@:~/Ansible-lab# ./setup-ubuntu.sh
     Error: No such container: ansible_node1
     Error: No such container: ansible_node2
     b80c0eae4efa95503b70110d44ba4d620b7e562dce7a9d9fd6e0e6198782e9fd
     e6c09d5d4dcfc50835a9d08030a5e77dd4660cf1c24fff89a2555eaba7e7a31c
     Hit:1 http://archive.ubuntu.com/ubuntu bionic InRelease
     Get:2 http://archive.ubuntu.com/ubuntu bionic-updates InRelease [88.7 kB]
     Get:3 http://archive.ubuntu.com/ubuntu bionic-backports InRelease [83.3 kB]
     Get:4 http://security.ubuntu.com/ubuntu bionic-security InRelease [88.7 kB]
     Fetched 261 kB in 3s (95.8 kB/s)
     Reading package lists... Done
     Reading package lists... Done
     Building dependency tree
     Reading state information... Done
     vim is already the newest version (2:8.0.1453-1ubuntu1.9).
     ansible is already the newest version (2.5.1+dfsg-1ubuntu0.1).
     0 upgraded, 0 newly installed, 0 to remove and 264 not upgraded.
     /root/ansible-lab
    ----------------------------
    - Ansible Port is
    - Node 1 Port is 49157
    - Node 2 Port is 49158
    ----------------------------
 3) root@:~/Ansible-lab# ssh-keygen
 4) root@:~/Ansible-lab# ssh-copy-id -p 49157 localhost
 5) root@:~/Ansible-lab# ssh-copy-id -p 49158 localhost
 6) ansible servers -m ping:
          node1 | SUCCESS => {
          "changed": false,
          "ping": "pong"
      }
      node2 | SUCCESS => {
          "changed": false,
          "ping": "pong"
      }
      root@vagrant:~/ansible-lab# ansible servers -m ping
      node2 | SUCCESS => {
          "changed": false,
          "ping": "pong"
      }
      node1 | SUCCESS => {
          "changed": false,
          "ping": "pong"
      }
