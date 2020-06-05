# GoogleIP Range hosts.allow

# What is it?

It is Google IP block list for hosts.allow(linux sshd hosts allow)

If you use GCP(Google Cloud Platform), this is for you!

We use these command to get these ip range.

```
nslookup -q=TXT _netblocks.google.com 8.8.8.8
nslookup -q=TXT _netblocks2.google.com 8.8.8.8
nslookup -q=TXT _netblocks3.google.com 8.8.8.8
```

# How to use it

Download hosts.allow and replace file to /etc/hosts.allow

Edit /etc/hosts.deny and add this content

```
sshd:ALL:deny
```
