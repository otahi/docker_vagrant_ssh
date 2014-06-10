docker_vagrant_ssh
==================

## provide ssh connectable docker image

### for users
```
sudo docker pull otahi/vagrant_ssh
sudo docker run -P -d --name sst_test otahi/vagrant_ssh 
```

### for creators
```
vagrant up 
vagrant ssh
sudo docker.io build -t otahi/vagrant_ssh /vagrant
sudo docker.io push otahi/vagrant_ssh
```


[see hub.docker.com otahi/vagrant_ssh](https://registry.hub.docker.com/u/otahi/vagrant_ssh/)
