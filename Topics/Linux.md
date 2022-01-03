## Linux

##### Linux Distribtuion familes

* Debian : ubuntu, mint, and kali linux
* Red Hat Enterprice linux: CentOS and Fedora
* SUSE: OpenSUSE
* Arch linux: LinHES and Manjaro

##### Linux Distribtuions: 

* Android (mobile)

* Red Hat Enterpirse linux: CentOS 

* SUSE: OpenmSUSE

* Scientific Linux (Science and math)

* Kali Linux (security)

* Raspbian (mini archtectures)

* Ubuntu (all-around)

* Mint (consumer-friendly)

* Virtual machines

* Clound computing

  

## Commands

##### Basic: 

* **locate [filename]** : if doesn't show update index with **sudo updatedb**

* **grep** : search plain text data set for lines that match regex. Can be used with pipeline **|** 

* **wc [file path] ** : word count 

* **wget** [URL] : retrieves content from web servers

* **cut -d: -f3 /etc/group | sort -n** : *cut* means extract sections from each line of input and sort command sorts the output.

##### **Standard streams:** 

* 0> : standard input 

* 1> : standard output 

* 2>  : standard error 

##### Archive 

* **tar xzf [file name]** : unpack archive, x: extract, z: comprest or zipped, f: file name follows.

* **tar  czf [zipfile name] [directory to archive]** : c: create.
* **unzip [file name]** : unzip .zip
* **zip [zip name] [directory to zip or all ""*""]** : zip into .zip 

##### Network Connectivity

* **ip route show** : check network access
* **ip addr** : show ip address
* **ifconfig** : show ip address (easier to read)
* **netstat -i** : interfaces statistics 
* **netstat -l** : open and listening ports 
* **host [url]** : find dns for site name
* **ping [address]** : send short massage with echo
* **/etc/hosts** : contains local dns 
* access remote server using SSH:
* **ssh [username]@[server ip address]** : connect to ssh server
* ![](images/ssh.PNG)

##### Linux Scripting 

* **nano [filename].sh** : create script
* **chmod +x [filename]** : change mode to be ececutable



##### System perfomrance metrics

* cd /proc : system info virtual files. created dinmacily with system events.
* maminfo : memeory infor 
* cpuinfo : cpu information
* **top** : manager for proccesses
* **free -h**: memory info
* **df -ht ext4**
* **sudo iftop -i [network name]** : network montior
* **ps**: current processes 
* **nice -19** : how much resources show process grab. 
* **kill [process number ]**: kill process
* **sudo systemctl status apache2** : check status of apache server.



##### Users and Groups 

* /etc/passwd: account and system data 
* /etc/group : groups data
* who : who logged in
* w : who is doing what 
* last : system logs
* id [name of user]: list all groups for user
* su [username] : switch users
* sudo ln -s [path of script] [group to link]:symbolic link



##### Docker

* docker run hello-world: run hello world example
* docker run -it ubuntu bash : run docker container with ubuntu distro and bash 
* docker ps: current running containers
* docker ps -a : all running with history
* docker images: list of docker images
* docker build -t "webserver" . : nameing tag webserver

