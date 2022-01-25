### Linux

##### Linux Distribution families

* Debian : ubuntu, mint, and kali Linux
* Red Hat Enterprise Linux: CentOS and Fedora
* SUSE: OpenSUSE
* Arch Linux: LinHES and Manjaro

##### Linux Distributions: 

* Android (mobile)

* Red Hat Enterprise Linux: CentOS 

* SUSE: OpenmSUSE

* Scientific Linux (Science and math)

* Kali Linux (security)

* Raspbian (mini architectures)

* Ubuntu (all-around)

* Mint (consumer-friendly)

* Virtual machines

* Cloud computing

  

### Commands

##### Basic 

* `locate [filename]` : if doesn't show update index with **sudo updatedb**
* `grep` : search plain text data set for lines that match regex. Can be used with pipeline **|** 
* `wc [file path]` : word count 
* `wget` [URL] : retrieves content from web servers
* `cut -d: -f3 /etc/group | sort -n`: *cut* means extract sections from each line of input and sort command sorts the output.
* `type [command]` : information 
* `which [command]` : locate command
* `whereis [command]` : which package it exists  
*  `| tee -a [file name ]`: print and add to file pipeline 
*  `/etc/skal/.bashrc_aliases` : runs once terminal opened, add alias to make them public 
*  `uname` : determine the processor architecture, the system hostname and the version of the kernel running on the system

##### Archive 

* `tar xzf [file name]` : unpack archive, x: extract, z: compress or zipped, f: file name follows.

* `tar  czf [zip file name] [directory to archive]` : c: create.
* `unzip [file name]` : unzip .zip
* `zip [zip name] [directory to zip or all ""*""]` : zip into .zip 

##### Standard Streams 

* 0> : standard input 
* 1> : standard output 
* 2>  : standard error 

##### Linux Scripting 

* `nano [filename].sh` : create script
* `chmod +x [filename]` : change mode to be executable

##### **Task Schedule** 

* Minutes(0-59) Hour(0-24) Day of the month (1-31) Month (1-12) Day of week (0-6 Sunday = 0) 
* `cronetab -l` : list all scheduled tasks 
* `cronetab -e` : create and select editor
* Example : `23 20 * * * /bin/sh /home/user...`

##### Users and Groups 

* `/etc/passwd`: account and system data 
* `/etc/group` : groups data
* `who` : who logged in
* `w` : who is doing what 
* `last` : system logs
* `id [name of user]`: list all groups for user
* `su [username]` : switch users
* `sudo ln -s [path of script] [group to link]`:symbolic link
* `sudo usermod -aG [group name] [username]` : add user to group
* `sudo deluser [username] [group name]` : delete user from group

##### Network Connectivity

* `ap-get install net-tools` : get tools for networking
* `route -n` : routing table on machine with numbers
  * `route del default gw [IP addr of gateway]` : delete default gateway 
  * `route add default gw [IP addr of gateway]` : add default gateway

* `ip` : ip commands
  * `ip addr`  : show ip addresses 
  * `ip route show` : check network access
  * `sudo ip addr add/del 172.31.1.1/255.255.0.0 dev eth0`: add or delete IP address
  * `sudo ip addr flush dev eth0` : delete all ip address for device
  * `sudo ip link set eth0 down` : deactivate interface
  * `sudo ip route add/delete default via 10.0.2.2` : add or delete default gateway

* `ifconfig` : show ip address (easier to read) works with interfaces
  * `ifconfig [net name] [ip addr] netmask [netmask]`: add IP address
  * `ifconfig eth0 del [IP Addr]` : remove IP address
  * `ifconfig [interface name] down` : deactivate interface 
  * `ifconfig [interface name] up` : activate interface

* `netstat -i` : interfaces statistics 
* `netstat -l` : open and listening ports 
* `host [url]` : find dns for site name
* `ping [address]` : send short massage with echo
* `/etc/hosts` : contains local dns 
* access remote server using SSH:
* `ssh [username]@[server ip address]` : connect to ssh server
* ![](/images/ssh.PNG)

##### System Performance Metrics

* `cd /proc` : system info virtual files. created dynamically with system events.
* `maminfo` : memory Info 
* `cpuinfo` : CPU information
* `top` : manager for proccesses
* `free -h` : memory info
* `df -ht ext4`
* `sudo iftop -i [network name]` : network montior
* `ps` : current processes 
* `nice -19` : how much resources show process grab. 
* `kill [process number ]` : kill process
* `[process name] &` : run process in the background
* `sudo systemctl status apache2` : check status of apache server.

##### Docker

* `docker run hello-world`: run hello world example

  `-i` : interactive mode 

  `-t` : allocate shell to work with it 

* `docker ps or docker container ls`: current running containers

* `docker ps -a` : all running with history

* `docker images`: list of docker images

* `docker run -it ubuntu bash` : run docker container with ubuntu distro and bash command

* `docker start [container ID or name ]` : start container already created

* `docker exec -it [container ID or name ] [command]` : interact with running container

* `docker stats` : display stats for containers live

* `docker inspect [name of container]` : show details about container, can be used with `grep` to filter results 

* `docker container prune` : delete all containers

Build image: 

* `docker build -t [image name] [path of Dockerfile]` : create image

Run container 

* `docker run [image name]` : run container

Push image 

* `docker push [user name]/[name of image]:[version tag]` : add image to docker hub repo

Issues with docker : 

* `sudo usermod -aG docker ${USER}` : restart to make effect

Docker pass file as parameter for container 

* `docker run -p 8080:8080 --mount type=bind,source=$(pwd)/application.properties,target=/application.properties oabuoun/sakilarestapi`

##### **Certificates and Keys**

* Generate key: 
  `openssl genrsa -out intermediate/private/plc1.example.com.key.pem 2048`
* Change permission:
  `chmod 400 intermediate/private/plc1.example.com.key.pem`
* Certificate signing request 
  `openssl req -config intermediate/openssl.cnf `
  `-key intermediate/private/plc1.example.com.key.pem `
  `-subj ’/CN=plc1.example.com/O=Example./C=US/ST=CA’ `
  `-new -sha256 -out intermediate/csr/plc1.example.com.csr.pem`
* Sign certificate 
  `openssl ca -batch -config intermediate/openssl.cnf `
  `-extensions server_cert -days 375 -notext -md sha256 `
  `-in intermediate/csr/plc1.example.com.csr.pem `
  `-out intermediate/certs/plc1.example.com.cert.pem`
* Self-sign certificate :  
* `openssl req -x509 -newkey rsa:4096 -nodes -out cert.pem -keyout key.pem -days 365`

##### Firewall Configuration

* List all rules 

  * `sudo iptables -L` 
  * `sudo iptables -S` : with specification
  * `sudo iptables -L --line-numbers`

* Drop all rules 

  * `sudo iptables -F`
  * `sudo iptables -t nat -F`
  * `sudo iptables -X`

* Delete rules eg. 2

  * `sudo iptables -D FORWARD 2`

* Drop all packets by default

  * `sudo iptables -P FORWARD DROP`
  * `sudo iptables -P INPUT DROP`
  * `sudo iptables -P OUTPUT DROP`

* Allow forwarding traffic **on firewall** that matches the rules: 

  ​	Source IP: 10.1.1.2
  ​	Destination IP: 10.1.2.1
  ​	Protocol: TCP
  ​	Port: 80 (HTTP)

  * `sudo iptables -A FORWARD -p tcp --dport 80 -s 10.1.1.2 -d 10.1.2.1 -j ACCEPT`

* Allow traffic that is part of connection to **pass through the firewall**. It allows established sessions, as well as new connections that are related to established sessions to pass.

  * `sudo iptables -A FORWARD -m conntrack --ctstate ESTABLISHED,RELATED -j ACCEPT`

##### Proxy

* install nginx 

  * `sudo apt install nginx`

* start nginx 

  * `sudo systemctl start nginx`
  * `sudo sysemctl enable nginx` : start with os boot

* Create custom link

  * `sudo nano /etc/nginx/sites-available/default`

    ```nginx
    server {
            listen 80;
            server_name _;
            location / {
                    proxy_pass http://127.0.0.1:8080;
            }
    }
    ```

  * load balancer :

    ```nginx
    upstream simplerest_servers {
            server 127.0.0.1:8080;
            server 127.0.0.1:8081;
    }
    server {
            listen 80;
            server_name _;
            location / {
                    proxy_set_header Host $host;
                    proxy_pass http://simplerest_servers;
            }
    }
    ```

  * With certificate : 

    ```nginx
    upstream simplerest_servers {
            server 127.0.0.1:8080;
            server 127.0.0.1:8081;
    }
    
    server {
            listen 443 ssl;
            server_name _;
    
            location / {
                    proxy_set_header Host $host;
                    proxy_pass http://simplerest_servers;
            }
    
            ssl_certificate /home/vagrant/cert/cert.pem;
            ssl_certificate_key /home/vagrant/cert/key.pem;
    
    }
    ```

    

* Create soft link to sites available 

  * `sudo ln -s /etc/nginx/sites-available/default /etc/nginx/sites-enabled/default`



##### SSH 

Forward shh key, share on the session that was created

* `eval 'ssh-agent'` : start ssh agent
* `ssh-add [key name]` : add key to session
* `ssh -A [destination IP]` : share key in session

Secure copy file 

* `scp application.properties ubuntu@54.170.152.163:/home/ubuntu`



##### MySQL 

Install client 

* `sudo apt install mysql-client-core-8.0`

Connect to server

* `mysql --host=[IP address] --user=root --password=root`

Run script on MySQL

* `source [source of script]` eg: `source /sakila-data.sql`

Access mysql server on server

* `docker exec -it mysql_dbms mysql -u root -p`

Change password 

* `ALTER USER 'root' IDENTIFIED WITH mysql_native_password BY 'new_password';`



##### Terraform

Show all commands

* `terraform`

Check if configuration valid 

* `terraform validate`

Show changes required to apply configuration provided 

* `terraform plan`

Destroy only one resource 

* `terraform destroy -target="aws_instane.java10x_sakila_konrad_app_tf"`



**Create infrastructure as code using Terraform** :

1. Create directory for infrastructure. 

2. Create file .tf
   1. Add provider with region
   
3. Initialize project 
   * `terraform init` 
   
4. In .tf file 
   * provider 
   * vpc
   * route53_zone, if using DNS
   * internet gateway 
   * route table
   * subnets
   * route table associations with subnets
   * network acl
   * security groups 
   * instances
   * route53_record, for each instance
   
5. Store key 4 methods :

   1. Store it in .tf file 

   2. Store it in environment viable 

      Environment variable for access key and secret key

      * `export AWS_ACCESS_KEY_ID="key"`
      * `export AWS_SECRET_ACCESS_KEY="key"`

   3. Store it in aws - not secure as it's not encrypted 

   4. Best choice, store it in aws-vault

      * `aws-vault add [name]`

      Run terraform with aws-vault

      * `aws-vault exec [name] -- terraform plan`



**Create configuration as code using Terraform :**

1. Add to .tf file inside resource instance: 
   1. connection including type, host, user, private key
   2. provisioner file if using scripts 
   3. provisioner `remote-exec` 



##### Ansible 

Inventory containing IP addresses which can be configured at the same time

Check default inventory : 

* `ansible all -m ping -u root`

Create list of servers 

* `nano ansible_hosts`

* ```ansible
  [servers]
  
  server1 ansible_host=52.18.232.37
  ```

Example of how to write inventory

* `cat /etc/ansible/hosts`

List inventory of file 

* `ansible-inventory -i ansible_hosts --list -y`

Go trough inventory and ping servers

* `ansible all -i [file of list of servers] -m ping -u [user of server, eg ubuntu]`

Send command to all servers

* `ansible all -i ansible_hosts -a "command to send" -u ubuntu`

Create playbook 

* `nano playbook.yml`

Play playbook 

* `ansible-playbook playbook.yml -i ansible_hosts -u ubuntu`
* `ansible-playbook playbook.yml -i [IP address], -u ubuntu`

Bypass ssh yes/no 

* `export ANSIBLE_CONFIG=$(pwd)`

Install docker ansible .yml 

* ```yaml
  ---
  - hosts: all
    become: true
    vars_files:
      - vars/default.yml
  
    tasks:
      - name: Install aptitude using apt
        apt: name=aptitude state=latest update_cache=yes force_apt_get=yes
  
      - name: Install required system packages
        apt: name={{ item }} state=latest update_cache=yes
        loop: [ 'apt-transport-https', 'ca-certificates', 'curl', 'software-properties-common', 'python3-pip', 'virtualenv', 'python3-setuptools']
  
      - name: Add Docker GPG apt Key
        apt_key:
          url: https://download.docker.com/linux/ubuntu/gpg
          state: present
  
      - name: Add Docker Repository
        apt_repository:
          repo: deb https://download.docker.com/linux/ubuntu bionic stable
          state: present
  
      - name: Update apt and install docker-ce
        apt: update_cache=yes name=docker-ce state=latest
  
      - name: Install Docker Module for Python
        pip:
          name: docker
  
      - name: Pull default Docker image
        docker_image:
          name: "{{ default_container_image }}"
          source: pull
  
      # Creates the number of containers defined by the variable create_containers, using values from vars file
      - name: Create default containers
        docker_container:
          name: "{{ default_container_name }}{{ item }}"
          image: "{{ default_container_image }}"
          command: "{{ default_container_command }}"
          state: present
        with_sequence: count={{ create_containers }}
  ```

  
