Run these commands to start vpn server
```
docker-compose run --rm openvpn ovpn_genconfig -u udp://<server ip>
docker-compose run --rm openvpn ovpn_initpki
docker-compose up -d
```

Run these commands to add user 
```
export CLIENTNAME="your_client_name"
# with a passphrase (recommended)
docker-compose run --rm openvpn easyrsa build-client-full $CLIENTNAME
# without a passphrase (not recommended)
docker-compose run --rm openvpn easyrsa build-client-full $CLIENTNAME nopass
```


Revoke a user

```
# Keep the corresponding crt, key and req files.
docker-compose run --rm openvpn ovpn_revokeclient $CLIENTNAME
# Remove the corresponding crt, key and req files.
docker-compose run --rm openvpn ovpn_revokeclient $CLIENTNAME remove
```