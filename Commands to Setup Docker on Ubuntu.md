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
sudo apt install docker-ce
```

### Check Docker Status
```
sudo systemctl status docker
```
Output should be something like this
`
● docker.service - Docker Application Container Engine
     Loaded: loaded (/lib/systemd/system/docker.service; enabled; vendor preset: enabled)
     Active: active (running) since Fri 2022-04-01 21:30:25 UTC; 22s ago
TriggeredBy: ● docker.socket
       Docs: https://docs.docker.com
   Main PID: 7854 (dockerd)
      Tasks: 7
     Memory: 38.3M
        CPU: 340ms
     CGroup: /system.slice/docker.service
             └─7854 /usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.sock
`


### Test Docker it setup properly and working
```
docker run hello-world
```
