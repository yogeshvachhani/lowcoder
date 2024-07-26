### Install Docker
```
sudo apt update
```


### Install prerequisite packages
```
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```


### Add the GPG key for the official Docker repository to system
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```


### Add the Docker repository to APT sources
```
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
```

### To install from the Docker repo
```
apt-cache policy docker-ce
```


You’ll see output like this, although the version number for Docker may be different:
```
docker-ce:
  Installed: (none)
  Candidate: 5:19.03.9~3-0~ubuntu-focal
  Version table:
     5:19.03.9~3-0~ubuntu-focal 500
        500 https://download.docker.com/linux/ubuntu focal/stable amd64 Packages
```			
				

### Install Docker
```
sudo systemctl status docker
```


### Test Docker it setup properly and working
```
docker run hello-world
```
