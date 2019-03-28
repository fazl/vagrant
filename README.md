# vagrant
Take a look at vagrant, as the docker experience has been less than 'wow!' 

Just need to install virtualbox (already done due to docker) and download the windows msi (about200mb) and install that.

Looks like it seems free.. and.. there is an oreilly book out for it already

Never heard of Hashicorp .. but what does that mean

Tips on how-to migrating to the how-to repo, to be a collection of useful cheatsheets.


Ooops, the very first attempt from https://www.vagrantup.com/intro/getting-started :

	$ vagrant up
	The version of powershell currently installed on this host is less than
	the required minimum version. Please upgrade the installed version of
	powershell to the minimum required version and run the command again.

Guess I need to figure out impact of upgrading powershell, which I never use directly.

So, after 90 mins of fiddling around installing stuff, I got powershell 4 and rebooted a few times.
Then completed the vagrant up command which downloaded lots of MB, and setup a linux vm for me.
Finally can log into it with:
vagrant ssh

There are warnings about : default network adapter being insecure in the vm, and also about problems syncing with files.

Vagrant is currently configured to create VirtualBox synced folders with
the `SharedFoldersEnableSymlinksCreate` option enabled. If the Vagrant
guest is not trusted, you may want to disable this option. For more
information on this option, please refer to the VirtualBox manual:

  https://www.virtualbox.org/manual/ch04.html#sharedfolders

  This option can be disabled globally with an environment variable:

    VAGRANT_DISABLE_VBOXSYMLINKCREATE=1

    or on a per folder basis within the Vagrantfile:

     config.vm.synced_folder '/host/path', '/guest/path', SharedFoldersEnableSymlinksCreate: false
     Vagrant has detected a configuration issue which exposes a
     vulnerability with the installed version of VirtualBox. The
     current guest is configured to use an E1000 NIC type for a
     network adapter which is vulnerable in this version of VirtualBox.
     Ensure the guest is trusted to use this configuration or update
     the NIC type using one of the methods below:

       https://www.vagrantup.com/docs/virtualbox/configuration.html#default-nic-type
       https://www.vagrantup.com/docs/virtualbox/networking.html#virtualbox-nic-type

     The guest additions on this VM do not match the installed version of
     VirtualBox! In most cases this is fine, but in rare cases it can
     prevent things such as shared folders from working properly. If you see
     shared folder errors, please make sure the guest additions within the
     virtual machine match the version of VirtualBox you have installed on
     your host and reload your VM.

     Guest Additions Version: 4.2.0
     VirtualBox Version: 5.2
