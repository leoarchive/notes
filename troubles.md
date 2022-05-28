
## create a new xsession desktop

```
sudo vim /usr/share/xsessions/dwm.desktop
```

```
[Desktop Entry]
Encoding=UTF-8
Name=Dwm
Comment=the dynamic window manager
Exec=dwm
Icon=dwm
Type=XSession
```


## set dwm status
```
xsetroot -name "$(date)"
```
autostart patch
https://dwm.suckless.org/patches/autostart/


```
patch -i patch_name
```

## clean restart docker
```
docker rm -f $(docker ps -a -q)
docker volume rm $(docker volume ls -q)
```

## arch lightdm cannot open
``` 
rm /etc/X11/xorg.conf.d/10-evdev.conf
```

## NPM package cannot be used as a JSX Component - Type error
```
use yarn in dockerfile and in package.json:

"resolutions": {
  "@types/react": "17.0.2",
  "@types/react-dom": "17.0.2"
},

```
## auto focus reactstrap input
```
const emailInputRef = React.useRef<HTMLInputElement>(null);

React.useEffect(()=>{
    setTimeout(() => {
        emailInputRef.current?.focus();
    }, 1);
}, []);


<Input innerRef={emailInputRef} ...props />

```

## disable screensaver dconf-editor
```
gsettings set org.gnome.desktop.screensaver idle-activation-enabled false
```
## mount new hard drive

```
# create mount dir
sudo mkdir mnt/drive

# new file system
sudo mkfs.ext4 /dev/sdXY

# mount drive
sudo mount /dev/sdXY mnt/drive

# change ownership to specified user
sudo chown user mnt/drive/
```

## debian steam error: you are missing the following 32-bit libraries, and steam may not run: libgl.so.1

this is the only solution that worked

```
sudo apt install nvidia-driver-libs:i386
```

## docker not run npm install
if your Dockerfile have more than one CMD, docker only run the last

```
change RUN npm install
for CMD ["npm", "install"]
``` 

## set user and email repository git/config

```
[user]
	name=name
	email=email
[remote "origin"] 
	url=https://username:password@github.com/username/repo 


or clone with this url
```
