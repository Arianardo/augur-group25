
Augur
branch	status
master	Build Status
dev	Build Status
About Augur
Augur is focused on prototyping open source software metrics.

Functionally, Augur is a prototyped implementation of the Linux Foundation's CHAOSS Project on open source software metrics. Technically, Augur is a Flask web application, Python library and REST server that presents metrics on open source software development project health and sustainability.

Getting Started
Vagrant
The quickest way to get started working on Augur is by using Vagrant to spin up a virtual machine (VM) that comes with Augur already installed. We'll do all the work of setting up and installing dependencies, leaving you free to jump right into making something awesome.

Caveat: if you’re a super nerd who likes to have total control over your development environment, there’s a local installation link at the bottom of this page. For the rest of you, Vagrant is the way to go, especially if you've had trouble getting all the dependcies installed locally, are not comfortable installing them yourself, or are using an OS for which we don't currently support local installation. We currently only support local installation for macOS and most flavors of Linux.

Windows installation instructions using Vagrant can be found here.

Dependencies
Git client
Vagrant
Virtualbox
GitHub Access Token (no write access required)
Clone the repository and boot up the VM.
# on your local machine
git clone https://github.com/chaoss/augur.git
cd augur
make vagrant
Note: you'll probably see a fair bit of errors during this provisioning process as Augur is getting installed. Don't worry about them, most of them are harmless. Probably.

Log in as root and navigate to /vagrant/augur. This folder is synced with your local clone of augur, meaning you'll be able to use your preferred local editor and just use the VM to run augur.
# inside the vagrant VM
sudo su -
cd /vagrant/augur

# due to vagrant weirdness, we have to manually install the python packagew (this might take a while)
$AUGUR_PIP install --upgrade .
Add your GitHub API key to the augur.config.json file under the section GitHub.

Start both the backend and frontend servers with make dev.

make dev
When you're done working in the VM, type exit twice: once to log out of root, and another to log out of the VM. Don't forget to shut down the VM with vagrant halt.
If you're interested in adding a new plugin, data source, or metric, check out the backend development guide. If new visualizations are more your speed, you'll want the [frontend development guide](http://augur.augurlabs.io/static/docs/dev-guide/4-frontend.html\).

TL;DR
# on your local machine

# using your Git client: 
git clone https://github.com/chaoss/augur.git

# using Command Prompt
cd augur
vagrant up
vagrant ssh

# inside the vagrant VM
sudo su -
cd /vagrant/augur

# due to vagrant weirdness, we have to manually install the python packages
$AUGUR_PIP install --upgrade .

# add your GitHub personal access token to augur.config.json

# start the frontend and backend servers
make dev
# full steam ahead!
Local Installation
To contribute to our code base routinely, we recommended that developers configure Augur on their local workstations. Start here to get a primer on the project, or jump straight into our local installation instructions for developers.

Guidelines
To contribute to Augur, please check out our development guide and notes on making contributions. Also, please note our code of conduct. We want Augur to be a welcoming development community that is open to everyone.

Roadmap
Our technical, outreach, and academic goals roadmap.

License and Copyright
Copyright © 2018 University of Nebraska at Omaha, University of Missouri and CHAOSS Project at the Linux Foundation

Augur is free software: you can redistribute it and/or modify it under the terms of the MIT License as published by the Open Source Initiative. See the file LICENSE for more details.

(This work has been funded through the Alfred P. Sloan Foundation)
