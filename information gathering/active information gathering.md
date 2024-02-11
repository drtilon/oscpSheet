# DNS Enumarion

DNS is a database that transforms a numerical ip to a name 

### host command
host www.megacorpone.com
www.www.megacorpone.com has address 149.56.244.87
host -t mx/txt www.megacorpone.com searcheds in other files as MX or TXT

one liner to attempt finding a server for www.megacorpone.com
```for ip in $(cat list.txt); do host $ip.megacorpone.com; done```
more advanced /usr/share/seclists

DNS-forward brute-force enumeration

```for ip in $(seq 200 254); do host 51.222.169.$ip; done | grep -v "not found" ```

# NMAP