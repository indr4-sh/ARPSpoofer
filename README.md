# ARP Spoofer

## Table of Contents
- [Usage](#usage)

### Prerequisites

What things you need to run

```bash
sudo iptables --policy FORWARD ACCEPT
sudo echo 1 > /proc/sys/net/ipv4/ip_forward
sudo ifconfig down
sudo macchanger --mac "aa:bb:cc:44:55:66" eth0
sudo ifconfig up
```

## Usage <a name = "usage"></a>

--target(-t) ip_victim

```bash
sudo python3 arp_spoof.py -t 192.168.1.x
```

## wireshark

```bash
wireshark &>/dev/null
```
filter for DNS