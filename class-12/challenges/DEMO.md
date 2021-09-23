# Ops Challenge - Network Scanning with Scapy Part 2 of 3

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

```python

#! /usr/bin/env python3

import ipaddress
from scapy.all import ICMP, IP, sr1, TCP

# Define end host and TCP port range. Take care not to populate the host bits here.

network = "10.0.2.0/24"
ip_list = ipaddress.ip_network(network)
hosts_count = 0

for host in ip_list:
    print("Pinging ",host,", please wait...")
    response = sr1(
        IP(dst=str(host))/ICMP(),
        timeout=2,
        verbose=0
    )

print(response)

```
