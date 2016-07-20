# mc-scripts
Couple of minecraft scripts for working with minecraft API, etc.

## mc-whoami 
Return the minecraft uuid for a username

*usage:* mc-whoami \<yourname\>

## mc-jre-install
Installs JRE and Minecraft server; running the script assumes that you accept the Minecraft server EULA.

*usage:* mc-jre-install \<minecraft-version\>

## Vagrant setup
CAVEAT: Probably not a brilliant idea to run an unsecured vagrant dev environment with its ports open to the public, so use with great caution and only in firewalled environments. You mess up, it's your problem, mate.

Run it
```
vagrant up
```
You'll be prompted to state which interface you want to broadcast over (mine looks like this):

```
    ==> default: Available bridged network interfaces:
    1) en0: Wi-Fi (AirPort)
    2) en1: Thunderbolt 1
    3) en2: Thunderbolt 2
    4) bridge0
    5) p2p0
    ==> default: When choosing an interface, it is usually the one that is
    ==> default: being used to connect to the internet.
        default: Which interface should the network bridge to? 
```

Enter your choice (i.e. 1, 2, 3 or 4) and then you're running a server on your local network (see the caveat above!); should be discoverable, but if you need to know the IP-address of the server, do:
```
$ vagrant ssh
$ ifconfig eth1 | grep inet
```

Look for an ipv4-style address, e.g. 192.168.xx.xxx
