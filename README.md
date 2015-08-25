README
======

This project aims to provide an agnostic monitoring network tool which can be accessed through REST-based Web Services.

Software Requirements
=====================

In order to run this code is necessary to have installed the following packages
* Python + Python Dev 
	* `sudo apt-get install python-setuptools python-dev build-essential`
	* `sudo easy_install pip`
* Flask (`sudo pip install flask`)

Resources
=========

At this time the following resources are available

* *GET* **/os** returns in JSON format the uname command's output. It is possible to ask for specific values
	* *GET* **/os/kernel**
	* *GET* **/os/release**
	* *GET* **/os/nodename**
	* *GET* **/os/kernelversion**
	* *GET* **/os/machine**
	* *GET* **/os/processor**
	* *GET* **/os/operatingsystem**
	* *GET* **/os/hardware**

* *GET* **/who** returns in JSON format the users connected at that time
	* *GET* **/who/<user>** returns if a specific `<user>` is connected

* *GET* **/cpu/<type>** returns in JSON format the CPU usage. Possible values for `<type>`:
	* **us** user
	* **sy** system
	* **id** idle
	* **wa** waiting 
	* **st** time stolen by virtual machines

* *GET* **/mem/<type>** returns in JSON format the RAM usage. Possible values for `<type>`:
	* **swpd** swap
	* **free** free
	* **buff** buffered
	* **cache** cached 

* *GET* **/swap/<type>** returns in JSON format the SWAP behaviour. Possible values for `<type>`:
	* **si** memory swapped in
	* **so** memory swapped out
	* **buff** buffered
	* **cache** cached 
	* **st** time stolen by virtual machines

Installation
============
Change permissions of `main.py` and run from command line `./main.py`.
