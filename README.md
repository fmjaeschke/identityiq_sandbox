# IdentityIQ sandbox
vagrant + ansible scripts for creating a sandbox with Sailpoint IdentityIQ

## installed stack in sandbox
- Java 8
- Tomcat (TODO)
- Oracle 18c XE
- IdentityIQ (TODO)
- OpenLDAP (TODO)

## Requirements
- virtualbox
- vagrant
- vagrant-vbguest (version 0.21 is preferred)
- identityiq.war version 8.1
- at least 10 GB of disc space (~6 GB for Oracle docker image + 2.5 GB to build Oracle docker image)

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
