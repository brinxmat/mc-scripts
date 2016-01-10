# mc-scripts
Couple of minecraft scripts for working with minecraft API, etc.

## mc-whoami 
Return the minecraft uuid for a username

*usage:* mc-whoami \<yourname\>

## mc-jre-install
Installs JRE and Minecraft server; running the script assumes that you accept the Minecraft server EULA.

## Vagrant setup
CAVEAT: Probably not a brilliant idea to run an unsecured vagrant dev environment with its ports open to the public, so use with great caution and only in firewalled environments. You mess up, it's your problem, mate.

Run it
```
vagrant up
```
and then you're running a server on your local network (see the caveat above!); should be discoverable, but if you need to know the IP-address of the server, do:
```
$ vagrant ssh
$ ifconfig eth1 | grep inet
```

Look for an ipv4-style address, e.g. 192.168.xx.xxx
