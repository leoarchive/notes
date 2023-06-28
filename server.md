# certbot
```
certbot certonly --standalone --preferred-challenges http -d exemplo.com.br
```
# ssl
```
openssl s_client -showcerts -connect irc.leonardo.moe:6697
```
# firewalld
```
sudo firewall-cmd --zone=public --add-port=<PORT>/tcp --permanent
sudo firewall-cmd --reload
```

# ORACLE HTTPS:
```
TCP 443 Allow HTTPS connections
```

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
