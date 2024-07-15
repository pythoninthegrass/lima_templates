# lima_templates

## Requirements
* [lima](https://lima-vm.io/docs/installation/)

## Quickstart
```bash
# install
brew install lima

# install socket_vmnet
brew install socket_vmnet

# Set up the sudoers file for launching socket_vmnet from Lima
limactl sudoers >etc_sudoers.d_lima
sudo install -o root etc_sudoers.d_lima /etc/sudoers.d/lima

# create alias
echo "alias lc='limactl'" >> ~/.bashrc

# create a new instance
lc start ubuntu-2004.yml --tty=false

# stop the instance
lc stop ubuntu-2004

# start the instance
lc start ubuntu-2004

# remove the instance
lc rm ubuntu-2004

# list all instances
lc ls

# shell into the instance
lc shell ubuntu-2004
```
