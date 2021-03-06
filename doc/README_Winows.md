#Windows Installation Instructions

###Required Software

**Download and Install Vagrant**<br>
	https://releases.hashicorp.com/vagrant/1.8.1/vagrant_1.8.1.msi

**Download and Install Virtualbox**<br>
	http://download.virtualbox.org/virtualbox/5.0.14/VirtualBox-5.0.14-105127-Win.exe

**Download and Install Mysysgit**<br>
https://github.com/git-for-windows/git/releases/download/v2.7.0.windows.1/Git-2.7.0-64-bit.exe

**Download and Install Atom**<br>
	https://atom.io/download/windows

**Install Vagrant Plugins**<br>

Install each product according to its instructions.  When complete, install the required plugins into Vagrant via Vagrant's plugin manager:

    vagrant plugin install vagrant-hosts
    vagrant plugin install vagrant-pe_build

**Windows PE Download Notes**<br>

In previous releases, vagrant-pe_build had issues with downloading Puppet Enterprise for installation onto the VMs.  In recent documentation, the project has stated that this bug is fixed, but I have as of yet not had the opportunity to test it.  If your instance comes up without further assistance, then your instalation will be complete at this point.

In the past, you would need to download the PE Package manually here:

	https://s3.amazonaws.com/pe-builds/released/3.7.1/puppet-enterprise-3.7.1-el-6-x86_64.tar.gz

Move it to the C:\Users\<username>\.vagrant.d\.pe_builds directory.

**Create a Workspace and Clone this Repository**<br>

In Windows Explorer, navigate to a location within which to create your project.  From there, clone the git repository.

	git clone https://github.com/cvquesty/centos65-pe2015.2.git

**Change to the Directory and Launch Vagrant**<br>

    cd centos65-pe2015.2
    vagrant up

**Notes:**<br>

* This environment requires your machine to have at least 8GB of RAM.
* This has been tested to work in Windows 8.1.
