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

## git credencial problems 

```
*dont forgot change git user and email first 

in config file:

[user]
	name=name
	email=email
[remote "origin"] 
	url=https://username:password@github.com/username/repo 


or clone with this url
```
