[README](README.md) | [中文文檔](README_zh.md)

# Google IP Range hosts.allow

# What is it?

This is a Google IP range, and we organize it into a host.allow file.

If you’re a GCP (Google Cloud Platform) service user, this is for you!

We use the commands below  to collect the IP range:

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
