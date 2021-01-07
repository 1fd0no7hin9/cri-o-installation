. /etc/os-release

```
VERSION_CRIO=1.17
OS=Ubuntu_18.04

echo "deb http://download.opensuse.org/repositories/devel:/kubic:/libcontainers:/stable:/cri-o:/$VERSION_CRIO/x$OS/ /" > /etc/apt/sources.list.d/devel:kubic:libcontainers:stable:cri-o:$VERSION_CRIO.list
echo "deb https://download.opensuse.org/repositories/devel:/kubic:/libcontainers:/stable/x$OS/ /" > /etc/apt/sources.list.d/devel:kubic:libcontainers:stable.list

curl -L http://download.opensuse.org/repositories/devel:/kubic:/libcontainers:/stable:/cri-o:/$VERSION_CRIO/x$OS/Release.key | sudo apt-key add -
curl -L https://download.opensuse.org/repositories/devel:/kubic:/libcontainers:/stable/x$OS/Release.key | sudo apt-key add -

sudo apt update
sudo apt install cri-o cri-o-runc
```