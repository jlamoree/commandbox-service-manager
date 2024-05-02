# Installation

Once you have been granted access to the package on ForgeBox, you will be able to install the module from your CommandBox CLI.  Check and make sure you are logged into the CLI with your ForgeBox account.

```text
forgebox whoami
```

If you're not logged in, you can authenticate like so:

```text
forgebox login
```

Now you're ready to install the Service Manager module!

```bash
install commandbox-service-manager@ortus
```

The module will be installed as a global/system CommandBox module.  You can update all your system modules or just the service manager like so:

```bash
# Check and update all system dependencies
update --system
# Update only the service manager
update commandbox-service-manager@ortus --system

# List all system dependencies
list --system
# Check for oudated dependencies
outdated --system
```

## CommandBox Home Directory

The recommendation for specifying a CommandBox home directory using `commandbox.properties` will make service creation using CommandBox Service Manager straightforward. See the [CommandBox Installation](https://commandbox.ortusbooks.com/setup/installation) documentation for instructions on defining the CommandBox home directory.

The service creation must be performed as an administrator user. In a secured server environment, the administrator is not the user that will be running the CFML application. By specifying a pinned CommandBox home directory, the discrepancy between the administrator user's home directory and the CFML application user's home directory will be irrelevant. This configuration also allows the correct permissions to be applied to the CommandBox working files for all users executing CommandBox.
