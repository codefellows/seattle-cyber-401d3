# Interview 01

## Interview Question

 Ask the candidate: 
  - "What is risk, and how do cyber security professionals interact with risk?"
    - "What is the CIA Triad, and how does it pertain to risk management?"
      - Ask for examples of each CIA Triad element.
      - Explore the technical elements of each example security control.
    - "What is non-repudiation?"
      - Ask for an example.
    - "How can risk levels be evaluated?"

## Interviewer Notes

Key areas to explore and discuss:
- Definition of risk
  - The candidate must provide a definition of risk in their own words. Below is one example definition.

  > "Cyber risk commonly refers to any risk of financial loss, disruption or damage to the reputation of an organization resulting from the failure of its information technology systems. Cyber risk could materialize in a variety of ways, such as: Deliberate and unauthorized breaches of security to gain access to information systems, unintentional or accidental breaches of security, or operational IT risks due to factors such as poor system integrity. Poorly managed cyber risks can leave you open to a variety of cybercrimes, with consequences ranging from data disruption to economic destitution. In many cases, businesses will also find themselves in the middle of a public relations nightmare as they struggle to recover lost assets and prevent further theft." -[Northbridge Insurance Blog](https://www.nbins.com/blog/cyber-risk/what-is-cyber-risk-2/)

- The candidate must explain the role that cyber security professionals play in interacting with risk
  - Cyber security professionals generally exist in order to evaluate cyber risk levels and then implement and operate security controls that mitigate cyber risk.
- CIA triad
  - Candidate must identify the three components and give an example security control belonging to each category. Explore in depth the proposed security controls, and how they work as a solution to mitigate risk.
    - Confidentiality
      - Keeping secret things a secret. Example: Joe used OpenVPN to establish a tunnel to his workplace before transmitting HR data.
    - Integrity
      - Maintaining the integrity of data and systems. Example: Logs indicate David accessed the DC at 5am Wednesday. The logs are trustworthy and free of tampering.
    - Availability
      - Maintaining the availability of important IT services. Example: Hans deployed a backup server just in case the primary server went down.
  - Non-repudiation, often an optional fourth element of the triad, means that the data at hand is reliable and cannot be refuted. An example of repudiation is "Logs indicate David accessed the DC at 5am Wednesday, but David says he did not."
  - Security controls generally fall into these categories and serve one or more purposes of the CIA Triad. 
- Risk can be evaluated two ways:
  - Qualitatively
    - Does not use numbers, but evaluates the qualities of each risk
  - Quantitatively
    - Uses numbers and assigns numeric scores to percieved risks
