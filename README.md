# CarOS

CarOS is a Linux-based OS distribution targeting carriers (thus the name). It provides modern infrastructure for monitoring and logging, providing both, a run-time environment for distributed applications as well as virtualization and containerization.

CarOS release is rolling and has one announcement per month with release drop (image etc.)

https://github.com/carosio/caros-release/releases/latest


## caros-release repository
CarOS release redomat declarations

Use [redomat](https://github.com/carosio/redomat) to build CarOS based on declarations found in this repository

### Build 

System base:
 Ubuntu Server 15.10 only with SSH-Server 
 
Install Docker:
 (https://docs.docker.com/installation/ubuntulinux/)
 
 ~~~
 sudo apt-key adv --keyserver hkp://pgp.mit.edu:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
 sudo echo "deb https://apt.dockerproject.org/repo ubuntu-wily main" >> /etc/apt/sources.list.d/docker.list
 sudo apt-get update
 sudo apt-get install docker-engine 
 ~~~
 
Install python libs and bulidtools 

~~~
 sudo apt-get install build-essential python3-venv python-pip python-docker
~~~

Checkout redomat

~~~
 git clone https://github.com/carosio/redomat.git
 cd redomat/
 make
 cd ..
~~~

Checkout caros redomat xml files

~~~
 git clone https://github.com/carosio/caros-release.git
~~~

Build vmware images

~~~
 redomat.py caros-release/caros-15.12-vmware.xml
 redomat.py caros-release/caros-15.12-lamobo-r1.xml
~~~

Get the file

~~~
 docker images
 docker run --rm -ti -p <free_local_port>:80 <last built image ID> /REDO/results/serve.sh
~~~
 
 Use webbrowser for download
 
## Acknowledgement

CarOS research, development and evaluation has been partially supported by [FP7 UNIFY](http://www.fp7-unify.eu), a research project partially funded by the European Community under the Seventh Framework Program (grant agreement no. 619609).  The European Commission is not liable for any use that may be made of this code repository.

The UNIFY consortium researches, develops and evaluates means to orchestrate, verify and observe end-to-end service delivery from home and enterprise networks through aggregation and core networks to data centres. The challanges addressed are under discussion also in the IRTF NFV RG; see [draft-unify-nfvrg-challenges](https://datatracker.ietf.org/doc/draft-unify-nfvrg-challenges/) for a summary.
