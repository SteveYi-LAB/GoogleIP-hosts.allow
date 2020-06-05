[README](README.md) | [中文文檔](README_zh.md)

# Google IP 塊 hosts.allow

# 這是用來做什麼的

這是Google網路的IP塊，我們將其整理成 hosts.allow 文件

如果你使用GCP(Google Cloud Platform)的服務，這很適合你！

我們使用下方這些指令來取得這些IP塊

```
nslookup -q=TXT _netblocks.google.com 8.8.8.8
nslookup -q=TXT _netblocks2.google.com 8.8.8.8
nslookup -q=TXT _netblocks3.google.com 8.8.8.8
```

# 如何使用

將 hosts.allow 下載下來並替換到 /etc/hosts.allow

編輯 /etc/hosts.deny 並新增以下內容

```
sshd:ALL:deny
```
