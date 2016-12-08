# PlusOne Demo

***
## Prerequisites
- **Linux**
	- This demo was created and tested using Fedora 24 but should work with any distrobution as long as the following prerequisites are met.
- **Java Runtime**
	- version >= 1.8
- **Docker**
	- version >= 10
	<https://docs.docker.com/engine/installation/>
- **Ansible**
	- version >= 2.3
	*At time of writing (2016/11/28), some Linux distro's had version 2.2 in their repositories and in order to get 2.3 you have to run from source* <http://docs.ansible.com/ansible/intro_installation.html#running-from-source>.
	- The host running ansible must be able to remotely connect to both the server running a standalone 'legacy' web application in wildfly and the server that will be running OpenShift.  Please read the following for more information <http://docs.ansible.com/ansible/intro_getting_started.html#id5>
- **Git**
	- version >= 2.7

## Download the Demo
Clone the github repository
	
	$ git clone https://github.com/rduncan506/plusone.git
	
## Option 1 - From Binaries
To make it easier and remove dependencies on build tools, all source has been compiled/packaged and has been downloaded when cloning the github repository in the previous step.

### Step 2 - Configure Installation
Edit <plusoneROOT\>/ansible/plusonedemo/hosts

Edit <plusoneROOT\>/ansible/plusonedemo/site.yaml

### Step 3 - Run Ansible
	$ cd <plusoneROOT\>/ansible/plusonedemo
	$ ansible-playbook -i hosts site.yml

## Option 2 - From Source
###Additional Prerequisites
In addition to the main prerequisites above, the following are required to compile and deploy the source in the following sections.


	$ kill -9 `fuser -f nohup.out`
	$ docker stop origin `docker ps -q`

- **Maven**
	- version >= 3.3
- **NPM**
	- version >= 2.15

