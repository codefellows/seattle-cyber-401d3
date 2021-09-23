# Interview 01

## Interview Question

- What is threat hunting?
  - What are the stages of a hunt?
- How can threat hunters keep up with the latest security threats?
- What tools and techniques are used in signature-based threat detection?
  - What about behavioral threat detection, particularly covert data transmissions?

## Interviewer Notes

- **Threat hunting** is the act of proactively searching for threats in the network. Hunters will seek to obtain indicators of compromise (IOCs) that suggest nefarious activity is taking place, and investigate more deeply using forensics tools in order to determine if the observed traffic is in fact malicious.
- The **threat hunting loop** depicts the stages of a hunt.

  ![huntloop](../assets/huntloop.png)

- Threat hunters use **intelligence feeds** like [VirusTotal](https://www.virustotal.com/gui/home/upload) and [Spamhaus](https://www.spamhaus.org/) to keep up with current information about what IOCs they should be looking for.
- In signature-based threat detection, malware hashes from resources like VirusTotal are compared to file hashes that are being scanned by the antimalware solution. Commercial software can do this, or one might combine YARA rules with ClamAV for an effective email scanner. The downside to this technique is that if the malware author deviates a little from the known signature, it can go undetected by scanners since the hash will differ.
- In behavioral threat detection, anomalous activities are detected rather than file signatures. An example of behavioral detection is when RITA analyzes a PCAP for beaconing.
