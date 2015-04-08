# atlassian-apps-vagrant-install

A project that uses Vagrant and Puppet to create and boot a VirtualBox VM with the following apps

* Stash
* JIRA
* Confluence
* Bamboo

## Notes

* This is intended as a proof of concept and is not intended to be a full provisioning solution for any of the installed applications. You will need to manually supply your own licenses and use the "Evaluation Installation" option for all four apps as the Puppet manifest does not install or configure a database.
* Because the resulting VM is expected to run 4 different applications, I've set the required RAM for the VM to 4GB.  Depending on your system you may want to increase or decrease this allocation.
* The provisioning process can take a *long* time (10+ minutes on a fast connection).  Between Bamboo, Confluence, JIRA and Stash you're going to be downloading about 500MB of data before the installation process starts.
* Credit where credit is due: This project is closely based off-of Nicola Paolucci's Stash provisioning example https://bitbucket.org/durdn/stash-vagrant-install.git. Check out https://blogs.atlassian.com/2013/03/instant-java-provisioning-with-vagrant-and-puppet-stash-one-click-install/ for more details

## Dependencies

1. [Vagrant](http://downloads.vagrantup.com/)
2. [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

## Usage

	$ git clone https://github.com/lwndev/atlassian-apps-vagrant-install.git && cd atlassian-apps-vagrant-install
	$ vagrant up

Once the VM boot and provisioning is complete, you can access the applications at the following locations:
* Bamboo: http://192.168.100.100:8085
* Confluence: http://192.168.100.100:8090
* JIRA: http://192.168.100.100:8080
* Stash: http://192.168.100.100:7990

## Reference URL's
## 
## cPrime scrubbed : https://lab.cprime.com/stash/users/sworley/repos/atlassian-stack-vagrant/
## sworley Forked : https://github.com/sworley/atlassian-apps-vagrant-install
## Original : https://github.com/lwndev/atlassian-apps-vagrant-install
