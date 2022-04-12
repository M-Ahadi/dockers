## Smart DNS
This package helps you to change your IP for specific websites to bypass region restrictions

To use this, first edit dnsmasq/proxy.conf and replace your VPS ip address, then simply run this command:

```
docker-compose up -d
```

In order to config with websites you want to bypass region restriction edit the dnsmasq/proxy.conf file.

If you got error regarding port 53, you should stop local dns in your system. After running the service user your VPS ip as DNS.