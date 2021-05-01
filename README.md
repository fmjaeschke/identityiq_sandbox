# identityiq_sandbox


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
