# env setup
## Step 1 Install Vagrant
Everything can be found on its website.

[The way to init vm](https://www.vagrantup.com/docs/getting-started/)

[The vm box list](https://atlas.hashicorp.com/boxes/search)

Since Ross said to use xubuntu. The most downloads one is  jhartman/xubuntu14.04.1

After the vm is initialized, edit the Vagrantfile. Add one line:
```python
config.vm.network "private_network", ip: "192.168.33.10"
```
Then we can use the ip address to access the vm

## Step 2 Install Jenkins
use apt-get
[jenkins wiki](https://wiki.jenkins-ci.org/display/JENKINS/Installing+Jenkins+on+Ubuntu)

## Step 3 Install git
apt-get 

## Step 4 Setup Jenkins
If wanna use ssh to connect the git repo, do the following three steps:

#### use this command to switch to jenkins user
```
sudo su -s /bin/bash jenkins
```
#### generate rsa key
```
ssh-keygen -t rsa
```
#### put the public key to the repo

After setup the public key, Open jenkins > Manage Jenkins > Manage Plugins , install the plugin: Git plugin

Establish a new item, set the repo address and the build script.

## Example
This project was established over one year ago.
So there's some problem about dependency and Jenkins version is different.
[Example](http://nomoon.me:8090/job/RestX/)
