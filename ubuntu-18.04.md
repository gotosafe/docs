# Create an empty file to prevent the service from starting
```
sudo touch /etc/cloud/cloud-init.disabled
```
# Disable all services (uncheck everything except "None"):
```
sudo dpkg-reconfigure cloud-init
```
# Uninstall the package and delete the folders
```
sudo dpkg-reconfigure cloud-init
sudo apt-get purge cloud-init
sudo rm -rf /etc/cloud/ && sudo rm -rf /var/lib/cloud/
```
# Restart the computer
```
sudo reboot
```

# If error: aufs aufs_fill_super:918mount[6090]: no arg overlayfs: missing 'lowerdir'
```
sudo apt-get remove snapd
```
