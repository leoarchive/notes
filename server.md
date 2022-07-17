# SSH key
```
ssh-keygen // generate my_ssh_key and my_ssh_key.pub
ssh -i my_ssh_key <user>@<ip>
```

# enable HTTP Connections
```
sudo iptables -I INPUT 6 -m state --state NEW -p tcp --dport 80 -j ACCEPT
sudo netfilter-persistent save
```