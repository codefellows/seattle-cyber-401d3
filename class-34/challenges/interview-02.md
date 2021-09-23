# Interview 02

## Interview Question

This is an interactive skills assessment. First, have the candidate download <https://www.malware-traffic-analysis.net/2020/09/25/2020-09-25-traffic-analysis-exercise-alerts.zip> to their FLARE VM and unzip it with the password 'infected'. Let the candidate know this package does not contain malware. Wait until this is complete before proceeding, as these files are a part of today's technical interview.

When the candidate is ready, ask them these questions one at a time:

- Describe the security incident that occurred based on your observations of the alert logs provided.
- If 10.0.0.0/24 is the company's subnet, what IP is the origin of the malware?
- How did the malware enter the system?
- What does the Trojan do? Feel free to use all resources at your disposal to answer this question.

## Interviewer Notes

Here is the [source](https://www.malware-traffic-analysis.net/2020/09/25/) of this activity. There are many valuable exercises on this site, be sure to bookmark it as a resource.

- Executive summary:
  - On Thursday, 2020-09-24 at approximately 22:41 UTC, a Windows host used by Ronaldo Paccione was infected with Agent Tesla malware.

- Victim details:
  - IP address: 10.0.0.179
  - MAC address: 00:0c:6e:34:b2:d0 (ASUSTekC_34:b2:d0)
  - Host name: DESKTOP-M1JC4XX
  - User account name: ronaldo.paccione

- Indicators of compromise (IOCs):
  - SHA256 hash: 1e4b7d7868d25071db67da87392fd5dafab344a9fa6dc040f7af
b0699152fc13
  - File size: 326,080 bytes
  - File type: PE32 executable (GUI) Intel 80386 Mono/.Net assembly, for MS Windows
  - File location: http://198.12.66.108/jojo.exe
  - File description: EXE file for AgentTesla malware

- Malicious HTTP traffic:
  - 198.12.66.108 port 80 - 198.12.66.108 - GET /jojo.exe
  - 185.61.152.63 port 587 - mail.big3.icu - SMTP traffic with data stolen from the infected Windows host
Suspicious domains using HTTPS traffic:
  - 37.120.174.218 port 443 - paste.nrecom.net - HTTPS address check probably related to the infection
  - port 443 - api.ipify.org - probably IP address check by the infected Windows host

AgentTesla is an information stealer. There are two categories of AgentTesla:
• AgentTesla that uses SMTP to send stolen data
• AgentTesla that uses FTP to send stolen data
