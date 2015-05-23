## Whats the point
Installing Go inside of a VM for easy development on OS X.

##Why Vagrant over Docker
The goal of this is to be ran in OS X.
Inside of OS X docker needs to live in a VM whichis usally boot2docker. 
I say that the Vagrant setup on OS X is easier and cleaner. 

## Requirements
- VirtualBox
- Vagrant
- Anisble

## Setup Vagrant and VirtualBox
	$ brew tap phinze/homebrew-cask && brew install brew-cask
	$ brew cask install virtualbox
	$ brew cask install vagrant

## Ansible Setup
	$ sudo easy_install pip
	$ sudo pip install ansible

## Setup
Pull Down the repo then:
	$ cd repodir
	$ vagrant up
	$ vagrant ssh
	$ go version

## Useful Vagrant commands
	$ vagrant provision 
	is the best way to reload the box if any changes to the Vagrantfile
	or Ansible files are made

	$ vagrant halt
	is the best way to stop the box from running

	$ vagrant destroy 
	Is the best way to remove everything about the box. This will not delte any
	files in the src folder as they are shared with your machine. 
	EVERYTHING ELSE WILL GO.

## Choosing golang version

This repo is hardcoded to use 1.4.2.

### Contributing
Any contributions are welcome. Please just fork the repo and submit a pull
request when complete.

## Credit
Initial idea came from
https://github.com/dcoxall/vagrant-golang
