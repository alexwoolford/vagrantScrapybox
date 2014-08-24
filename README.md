vagrantScrapybox
================

It's convenient to use VM's for one-off data acquisition tasks. A vanilla Ubuntu scrapy box can be provisioned:

    git clone https://github.com/alexwoolford/vagrantScrapybox
    cd vagrantScrapybox
    vagrant up

This assumes that vagrant (with the hashicorp/precise64 box) and Ansible are setup on the host machine.

The configuration also sets up and starts VyprVPN. The username and password for the account are in the vyprvpn.pas file. If you're going to use VyprVPN, edit this file with your own credentials before you vagrant up.

You can confirm that the external IP of the VM is different by executing the following command from the host and the VM:

    curl -s checkip.dyndns.org|sed -e 's/.*Current IP Address: //' -e 's/<.*$//'

The should return different IP addresses.
