# Interview 02

## Interview Question

Ask the candidate "What does the acronoym **APT** stand for, and how would you define it?"

- I have traditional security defenses, including antimalware agents and firewalls. Should I be concerned with APTs, and why?
- What is a threat actor, and what are some examples of different types?
- Give an example of a state-sponsored cyber attack.
- What threat modeling framework would you recommend for studying an APT?
- What is a C2 server?
- What is an attack payload?
- How can a threat actor automate a cyber attack against a system?

## Interviewer Notes

- **APT** stands for advanced persistent threat, and is "a covert cyber attack on a computer network where the attacker gains and maintains unauthorized access to the targeted network and remains undetected for a significant period. During the time between infection and remediation the hacker will often monitor, intercept, and relay information and sensitive data. The intention of an APT is to exfiltrate or steal data rather than cause a network outage, denial of service or infect systems with malware." -Cisco
- Traditional defense are inadequate in defending against APTs. Security controls like firewalls and antimalware agents are inadequate in defending against modern attack techniques such as lateral movement, privilege escalation, and more.
- A **threat actor** is a person or entity that has the ability or intent to impact the security of other individuals or companies. Types include:
  - Nation state or state-sponsored
  - Organized crime
  - Hacktivist
  - Inside actor
  - Script kiddies
- An example of a state-sponsored attack: "In December 2020, Facebook announced that its users had been targeted by two hacking campaigns, one originating from state-sponsored Vietnamese hackers focused on spreading malware, and the other from two non-profit groups in Bangladesh focused on compromising accounts and coordinating the reporting of accounts and pages for removal." -[CSIS](https://www.csis.org/programs/strategic-technologies-program/significant-cyber-incidents)
- Threat modeling frameworks:
  - STRIDE
  - OWASP Top 10 
  - MITRE ATT&CK
- A **C2 server** is a command and control system used to issue commands to remote malware.
- An **attack payload** is the attack component that harms the victim.
- A threat actor can automate a cyber attack by using shell scripting or other automated tools.
