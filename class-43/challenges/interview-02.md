# Interview 02: Windows Attack Techniques

## Interview Question

This interview will test the candidate's comprehension of attack techniques used against the Windows OS.

Begin the interview with some warmup questions.

- "Windows is a common attack surface, given its ubiquitous adoption in the desktop and enterprise marketplace. For this interview, I'll be asking you some questions about various attack techniques targeting Windows OS. How does Windows manage user identities and authentication? In your response, please address the terms 'Kerberos,' 'Active Directory,' and 'Domain.'"

- "What are some obsolete features in Windows 10 that, if activated, will cause known security vulnerabilities?"

Share this piece of code with the candidate. When they are ready, proceed.

```unknown
meterpreter > getsystem -h
Usage: getsystem [options]

Attempt to elevate your privilege to that of local system.

OPTIONS:

  -h        Help Banner.
  -t   The technique to use. (Default to '0').
  0 : All techniques available
  1 : Service - Named Pipe Impersonation (In Memory/Admin)
  2 : Service - Named Pipe Impersonation (Dropper/Admin)
  3 : Service - Token Duplication (In Memory/Admin)

meterpreter >
```

- "This is a sample console from a penetration tester executing Meterpreter. What is the general term for the type of exploit demonstrated here, and why would an attacker use this technique on a targeted system?"
  - Candidate should name the appropriate type of attack this is, and describe how it fits into an overall pentest or cyber attack effort.

Share this [terminal screenshot](https://pentestlab.files.wordpress.com/2018/04/golden-ticket-shell-with-psexec-as-invalid-user.png?w=760){:target="_blank"} with the candidate and proceed when they are ready.

- "This image depicts a malicious attack taking place against another Windows computer. What is the victim computer's domain, username, and system name? Please also explain how this attack is executed."
  - Candidate should identify the appropriate pieces of information, then go on to descibe the stages of a remote code execution or pass the hash attack.

Evaluate how well the candidate explained Windows OS security and related attack techniques.

## Interviewer Notes

- By default, Windows machines utilize NTLM to authenticate users.
- Kerberos is an authentication system that can be activated in a domained environment on the domain controller. If a Windows system detects Kerberos is available, it will use it instead of NTLM.
- Kerberos works with Active Directory (AD) to help more securely authenticate users using a ticket-granting system.
- **Privilege escalation** is a tactic where an attacker attempts to gain administrator rights from a non-administrator profile.
- **Pass the hash** is an offensive security technique belonging to the tactical family of **lateral movement**, which involves the nefarious use of hash values to authenticate as administrator over other systems on the network without knowing the plaintext password. 
