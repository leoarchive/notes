[How to install software or upgrade from an old unsupported release?](https://askubuntu.com/questions/91815/how-to-install-software-or-upgrade-from-an-old-unsupported-release)

```
sudo sed -i -re 's/([a-z]{2}\.)?archive.ubuntu.com|security.ubuntu.com/old-releases.ubuntu.com/g' /etc/apt/sources.list
sudo apt-get update && sudo apt-get dist-upgrade
```
