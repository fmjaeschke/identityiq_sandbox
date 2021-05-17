# IdentityIQ sandbox
vagrant + ansible scripts for creating a sandbox with Sailpoint IdentityIQ

## installed stack in sandbox
- Java 8
- Tomcat
- Oracle 18c XE
- IdentityIQ (TODO)
- OpenLDAP (TODO)

## Requirements
- virtualbox
- vagrant
- vagrant-vbguest (version 0.21 is preferred)
- identityiq.war version 8.1
- at least 10 GB of disc space (~6 GB for Oracle docker image itself + ~3 GB to build Oracle docker image)

- plenty of time (on my AMD Ryzen5 2600 it takes 795 seconds alone to build the Oracle docker image)

## General usage
Start image with
```sh
vagrant up
```

If something was changed in Ansible scripts rerun provisioning the image with
```sh
vagrant provision
```

Image could be stopped with
```sh
vagrant halt
```

And complete removed, if something was messed up with
```sh
vagrant destroy --force
```

Reference for Vagrant CLI options (https://www.vagrantup.com/docs/cli)

## Troubleshooting
**Q: I get constantly errors like 'An error occurred during installation of VirtualBox Guest Additions' or version missmatch of installed VirtualBox guest extension and installed VirtualBox version.**

**A:** You may need to downgrade installed vagrant-vbguest plugin

Check which version is installed
```sh
vagrant plugin list
```

If it is newer than v0.21 uninstall vagrant-vbguest plugin and install v0.21
```sh
vagrant plugin uninstall vagrant-vbguest
vagrant plugin install vagrant-vbguest --plugin-version 0.21
```
