# Interview 02

## Interview Question

Send the candidate the link to the [ZAP alerts image](https://www.randorisec.fr/img/blog/zap_alerts.png){:target="_blank"}. When the candidate confirms the link is working and has reviewed the image, proceed.

Ask the candidate:

- Why does ZAP consider this a high priority alert?
- Explain the technique used by ZAP to determine the target is vulnerable to SQL injection.
- How would you test for SQLi vulnerabilities using a tool outside of ZAP?

> Reading alerts and interpreting them is a vital skill to nurture as a junior security professional.

Send the candidate the link to the [ZAP spider output image](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fi.stack.imgur.com%2FREfnl.png&f=1&nofb=1){:target="_blank"}. When the candidate confirms the link is working and has reviewed the image, proceed.

Ask the candidate:

- This is a sample output from a ZAP scan. What ZAP component was used to generate this output, and what is depicted here?
- What does "OUT_OF_SCOPE" mean?
- Why do web app security testing tools like ZAP crawl directories?

Show the candidate this Python code sample. Give the candidate a moment to read over it, then proceed.

```python
def get_all_forms(url):
    soup = bs(s.get(url).content, "html.parser")
    return soup.find_all("form")
```

Ask the candidate:

- What is Beautiful Soup, and what does this function do?
- What kinds of web application vulnerabilities can this script potentially detect, if further developed?
- How can web application security tools be improved upon?

Evaluate the candidate's proficiency and comprehansion of web application security tooling.

## Interviewer Notes

### Part 1

- ZAP determined that the site was vulnerable to SQL injection attack technique by entering `query AND 1=1` in order to elicit an anomalous fresponse from the interpreter.
- Injection is among the OWASP Top 10 web application security risks and is a common way attackers will attempt to gain unauthorized access to a web application.
- SQL injection can be tested for by typing in the commands manually instead of using automated tooling.

### Part 2

- A spider tool was used to enumerate the files seen in the provided output.
- The `OUT_OF_SCOPE` message indicates the discovered object exists outside of the target domain.
- Directory enumeration is a useful capability for all offensive security engagements, allowing the attacker to view the structure of the directories.

### Part 3

- **Beautiful Soup** is a Python library for pulling data out of HTML and XML files.
- Because Beautiful Soup is able to evaluate HTML data, it can theoretically be used to detect for SQL injection vulnerabilities by inserting malicious code into the form field.
- Web application security tooling can be customized to suit the needs of a given engagement by using Python libraries for example.
