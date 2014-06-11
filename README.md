docker_vagrant_ssh
==================

## provide ssh connectable docker image

You can connect the container with the vagrant insecure ssh key ~/.vagrant.d/insecure_private_key

### usage

You can run the docker container with:
```
sudo docker pull otahi/vagrant_ssh
sudo docker run -P -d --name sst_test otahi/vagrant_ssh 
```

access to the container with like:
```
ssh root@172.17.42.1 -p 49153 -i /vagrant/insecure_private_key
```

[see hub.docker.com otahi/vagrant_ssh](https://registry.hub.docker.com/u/otahi/vagrant_ssh/)
