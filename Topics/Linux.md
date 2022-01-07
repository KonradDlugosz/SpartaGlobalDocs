## Linux

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

  

## Commands

##### Basic: 

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

##### **Standard streams:** 

* 0> : standard input 

* 1> : standard output 

* 2>  : standard error 

##### Archive 

* `tar xzf [file name]` : unpack archive, x: extract, z: compress or zipped, f: file name follows.

* `tar  czf [zip file name] [directory to archive]` : c: create.
* `unzip [file name]` : unzip .zip
* `zip [zip name] [directory to zip or all ""*""]` : zip into .zip 

##### Network Connectivity

* `ip route show` : check network access
* `ip addr` : show ip address
* `ifconfig` : show ip address (easier to read)
* `netstat -i` : interfaces statistics 
* `netstat -l` : open and listening ports 
* `host [url]` : find dns for site name
* `ping [address]` : send short massage with echo
* `/etc/hosts` : contains local dns 
* access remote server using SSH:
* `ssh [username]@[server ip address]` : connect to ssh server
* ![](/images/ssh.PNG)

##### Linux Scripting 

* `nano [filename].sh` : create script
* `chmod +x [filename]` : change mode to be executable

##### System perfomrance metrics

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

##### Docker

* `docker run hello-world`: run hello world example

  `-i` : interactive mode 

  `-t` : allocate shell to work with it 

* `docker ps or docker container ls`: current running containers

* `docker ps -a` : all running with history

* `docker images`: list of docker images

* `docker build -t "webserver" .` : naming tag webserver

* `docker run -it ubuntu bash` : run docker container with ubuntu distro and bash command

* `docker start [container ID or name ]` : start container already created

* `docker exec -it [container ID or name ] [command]` : interact with running container

* `docker stats` : display stats for containers live

**Hashing password in shadow file**  

* $ID $SALT $HASHED_PASSWORD
  ID 1 : MD5 
  ID 5 : SHA256
  ID 6 : SHA512 
  SALT : Random value
  HASHED_VALUE = hash(algorithm, SALT, PASSWORD)

**Task Schedule to run scripts** 

* Minutes(0-59) Hour(0-24) Day of the month (1-31) Month (1-12) Day of week (0-6 Sunday = 0) 
* `cronetab -l` : list all scheduled tasks 
* `cronetab -e` : create and select editor
* Example : `23 20 * * * /bin/sh /home/user...`

