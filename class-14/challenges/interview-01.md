# Interview 01

## Interview Question

Ask the candidate: 
- What are some examples of security teams that an organization might assemble?
  - What are threat hunters, what do they do, and how is this role different from IR?
- What tools can a SOC use to detect threats?
  - Why do security teams use SIEMs?
  - How do SIEMs work? Be sure to highlight the key infrastructure components for Splunk Enterprise by drawing them in a diagram depicting a small enterprise deployment.
  - If my SIEM is aggregating logs from multiple systems that all have different time zones, what aspect of the CIA triad is violated and why?

## Interviewer Notes

Key areas to explore and discuss:
- Types of security teams
  - **Computer Security Incident Response Team (CSIRT)**
  - **Security Operations Center (SOC)**

- Proactively searching for threats in the environment is known as **threat hunting**.
  - Threat hunters proactively search for security threats in the environment, but they do not perform the full incident management lifecycle. Threat hunters stick to detection and identification duties.
- A **SIEM** aggregates systems logs from devices throughout the environment.
  - Endpoints
  - Servers
  - Network appliances
- Splunk Enterprise is an example of a SIEM. It uses the following key elements to collect data:
  - Search head
  - Indexer
  - Forwarder

![splunk.png](../assets/splunk.png)

- **Sysmon** is often deployed to Windows systems to improve the quality of event log data that gets sent to the SIEM.
- SIEMs can be configured to parse data in a desired configuration, and also display data in visual dashboards.
- If SIEM data sources have conflicting times, the integrity aspect of the CIA triad is violated because the data has poor **integrity**.
