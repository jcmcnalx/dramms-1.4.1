#DRAMMS 1.4.1
-------
  - Deformable Registration via Attribute Matching and Mutual-Saliency Weighting (DRAMMS) [MedIA2011], is a software package designed for 2D-to-2D and 3D-to-3D image registration tasks.
  - http://www.cbica.upenn.edu/sbia/software/dramms/index.html
  - Current Version 1.4.1
  - Authors
    - http://www.cbica.upenn.edu/sbia/software/dramms/people.html

--------

The Dockerfile and indentity.sh script will create an Ubuntu 14.04 container for DRAMMS + ability to mount host storage.

Requirements
--------

- Linux server or workstation
  - [Docker](https://www.docker.com//) >= 1.5

Installation
-------
Download Git repository
- git clone https://github.com/jcmcnalx/dramms-1.4.1.git

Cd into downloaded repo
- cd dramms-1.4.1

Execute identity.sh in same directory as Dockerfile
- ./identity.sh

Build Docker container
  - docker build -t YOUR_CONTAINER_NAME .

Note: The container is built using Phusion's Ubuntu 14.04 baseimage
http://phusion.github.io/baseimage-docker/

Run container
--------
Once built run the container with options to mount your home directory
  - $ docker run -it -v /home/USERNAME:/home/USERNAME YOUR_CONTAINER_NAME /bin/bash
  - Replace USERNAME with your username

Run DRAMMS tools
  - Tools and libraries located in /opt/sbia/dramms-1.4.1

Loading and saving data can be achieved by downloading the sample data in addition to working with your own data accessible in your container mounted home directory.

DRAMMS official documentation  http://www.cbica.upenn.edu/sbia/software/dramms/manual.html

----------
Tested on Docker hosts:
  - Ubuntu 14.04
  - CentOS 6.x
  - RHEL 6.x
  - Boot2docker Windows
