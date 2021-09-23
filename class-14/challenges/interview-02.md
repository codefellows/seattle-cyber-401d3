# Interview 02

Ask the candidate: 
- Please diagram the implementation of a firewall. Include elements for the internet, firewall, cable modem, router, endpoint, and switch.
  - Do you prefer filtered ports or closed ports on your firewall, and why?
- What is Nmap, why is it important with regards to network security, and how does it work? 
- Please explain the concept of "security by obscurity."
  - If I move my well-known port to a random port number, am I secure against attack? Why?
- Now that we're on the topic of ports and protocols, let's talk about ICMP next. What is ICMP, what does the acronym stand for, 
what port number is ICMP, and how does it work compared to other protocols?

## Interviewer Notes

- The order of the diagram should flow as follows:
  1. Internet depicted as a cloud
  1. Cable modem
  1. Router combined with firewall, or depicted as separate
  1. Switch
  1. Endpoint
- A **closed port** indicates that no application or service is listening for connections on that port, although the port can open up if an application or service is started that uses it. A **filtered port**, however, indicates that a firewall, filter, or other network issue is blocking the port. 
- **Network Mapper (Nmap)** is an open source Linux command line tool used to scan network IP addresses and the ports on each host. Nmap can also attempt to detect useful information abouch each host, such as installed applications and OS.
  - Nmap is particularly useful during a penetration test, as it can help the attacker find vulnerabilities on target hosts.
  - Nmap can even be used to attack systems using existing scripts from the Nmap Scripting Engine (NSE).
  - Nmap is operated via command line or its separate GUI, Zenmap.
- Use the third question above to facilitate a discussion of "security by obscurity," exploring the pros and cons of being visible versus not.
  - **Security by obscurity** is a logical fallacy that asserts security can be achieved by "obscuring" (hiding) vulnerabilities, such as open ports. Proper computer security cannot be attained by merely concealing vulnerabilities. Security by obscurity is commonly assumed amongst untrained computer operators, but not well-trained security professionals. Therefore, reassigning an open port to a random number does not fully secure a computer against attack.
- Asking the port number for ICMP is a trick question. The **Internet Control Message Protocol (ICMP)**, colloquially known as ping, does not have a designated port number. While ICMP does belong to the application layer of the OSI model, it does not transmit data over the transport layer; instead, ICMP transmits over the IP layer. This is a common question to test a person's grasp of ports and protocols as they relate to the theoretical OSI model.
