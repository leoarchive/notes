## NPM package cannot be used as a JSX Component - Type errors
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
