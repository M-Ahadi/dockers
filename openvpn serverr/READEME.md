Run these commands to start vpn server
```
docker volume create --name openvpn
docker run -v openvpn:/etc/openvpn --log-driver=none --rm kylemanna/openvpn ovpn_genconfig -u udp://<server ip>
docker run -v openvpn:/etc/openvpn --log-driver=none --rm -it kylemanna/openvpn ovpn_initpki
docker run -v openvpn:/etc/openvpn -d --restart always -p 1194:1194/udp --cap-add=NET_ADMIN kylemanna/openvpn 
```

Run these commands to add user 
```
docker run -v openvpn:/etc/openvpn --log-driver=none --rm -it kylemanna/openvpn easyrsa build-client-full CLIENTNAME nopass
docker run -v openvpn:/etc/openvpn --log-driver=none --rm kylemanna/openvpn ovpn_getclient CLIENTNAME > CLIENTNAME.ovpn
```