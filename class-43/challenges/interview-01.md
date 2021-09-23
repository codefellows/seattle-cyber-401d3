# Interview 01: Target Intelligence & Reconnaissance

## Interview Question

This interview topic will test the candidate's comprehension of target intelligence, and the role it plays in a greater security team or pentesting effort.

Begin the interview with a couple warmups.

- "I first have some questions for you about penetration testing. What is the purpose of a penetration test? Please also describe the stages of a penetration test."
  - Candidate should know the seven stages of a penetration test according to PTES.

- "How do the Reconnaissance and Enumeration stages of penetration testing facilitate the execution of subsequent activities, such as vulnerability exploitation?"
  - Candidate should draw a connection between intelligence gathering and the process of actual computer exploitation.

Share this link to the [Maltego Transform Hub](https://www.maltego.com/transform-hub/){:target="_blank"} with the candidate. When they are ready to proceed, ask the following questions:

- "Thanks for explaining penetration testing. Let's talk about defending. My threat intelligence team wants to use Maltego to gather malware and IOC signatures as part of the company's overall defense effort. The team is new to the process of gathering threat intelligence using this particular tool, although they are well-versed in many securty tools and resources such as the MITRE ATT&CK® database, Atomic Red Team, Splunk, and Security Onion. Which one of these transform packages should we implement, why should we choose it, and how does it work?"
  - Candidate should address all three questions and demonstrate a grasp of how APIs, transforms, and TTPs are integrated via Maltego.

Share this link to the [FireEye APT List](https://www.fireeye.com/current-threats/apt-groups.html){:target="_blank"} and proceed when they are ready.

- "Feel free to reference the provided web resource for this question. My company supports a client in the US defense sector that has been infiltrated in the past by threat actors from APT40. This client has requested that we customize their cyber defenses against the TTPs of APT40. Given what you know about my threat intelligence team, what steps should we take in achieving this objective for the defense company, and how do we measure the success of this effort?"
  - Candidate should discuss in depth the process of identifying IOCs and TTPs associated with APT40 and describe KPIs that might be used to define if the changes yielded successful outcomes.

Evaluate how well the candidate seemse to grasp the purpose of penetration testing, intelligence gathering, and how threat intelligence efforts tie directly to an organization's desired measurable outcomes.

## Interviewer Notes

- Penetration test
    - Formalized hacking process where vulnerabilities are discovered and exploited
    - Simulate real-world attacks
    - Findings are documented and reported
  - PTES stages of pentesting:
    1. Pre-engagement Interactions
    1. Intelligence Gathering
    1. Threat Modeling
    1. Vulnerability Analysis
    1. Exploitation
    1. Post Exploitation
    1. Reporting
  - Pentesters perform reconnaissance against their target in order to gain more information about what they're about to attack.
    - Passive: OSINT, observing, and sniffing. Information Gathering.
    - Active: Interacting with target and probing network for weaknesses.
    - Maltego is used to perform target investigation, typically to learn more about a company and its web footprint.
    - "Maltego is an open source intelligence (OSINT) and graphical link analysis tool for gathering and connecting information for investigative tasks."
    - Desktop client
    - Supports data integration
  - What is a Maltego object/entity?
    - A person, company, domain, etc.
    - An artifact of online activity
  - What is a Maltego Transform?
    - Discover relationships to existing data entities
