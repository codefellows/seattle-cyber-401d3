# Ops Challenge - Network Scanning with Scapy Part 1 of 3

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

This first example takes an IP or a name as first parameter, send an ICMP echo request packet and display the completely dissected return packet:

```python

#! /usr/bin/env python

import sys
from scapy.all import sr1,IP,ICMP

p=sr1(IP(dst=sys.argv[1])/ICMP())
if p:
    p.show()

```

The second example scans a specific port on a given host IP, then returns the response.

```python

#! /usr/bin/env python3

# Run this with sudo

from scapy.all import ICMP, IP, sr1, TCP

# Define target host and TCP port to scan
host = "scanme.nmap.org"
port_range = 22
src_port = 22
dst_port = 22

response = sr1(IP(dst=host)/TCP(sport=src_port,dport=dst_port,flags="S"),timeout=1,verbose=0)

print(response)

```
