# vagrant
Take a look at vagrant, as the docker experience has been less than 'wow!' 

Just need to install virtualbox (already done due to docker) and download the windows msi (about200mb) and install that.

Looks like it seems free.. and.. there is an oreilly book out for it already

Never heard of Hashicorp .. but what does that mean

TIP: in a bash window export HISTCONTROL=erasedups

TIP: FAIL 
	to avoid always entering git creds can try this from stackover:
	git config credential.helper store        	
	git push https://github.com/owner/repo.git	
	git config --global credential.helper 'cache --timeout 7200'

This works on my win7+git-for-windows:	
	git config --global credential.helper 'cache --timeout 7200'

TIP: run GitBash as admin before trying to change git config if it complains about not being able to lock a gitconfig file
