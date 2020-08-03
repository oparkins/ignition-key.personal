# ignition-key.personal
Ansible scripts to setup a user account the way I prefer it.

## Setup

Create an `inventory.yml` file that contains all of the hosts that you are able to connect to. Note that these scripts do not require superuser and shouldn't. This means these scripts should work on every server you have access to. 

An `inventory.yml` file would look like:
```
all:
  hosts:
    host0:
    host1:
		host2:
		...
```

Then edit the roles to suit yourself. I recommend adding a new role for each program you want to configure. The roles essentially need:
```
role_name
|- files
|- tasks
   |- main.yml
```

Then run `ansible-playbook site.yml` to have all the machines updated the way you want.


## Pull Requests Welcome

If you have what you believe is a superior setup or configuration file, pull requests are always welcome. Even if it is for a program I don't have here (like bash at the moment). The main thing is that these scripts need to work without superuser access. 
