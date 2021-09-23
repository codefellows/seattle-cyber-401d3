# Interview 01

## Interview Question

Show the candidate this piece of code. Give the candidate a moment to read the code and let you know they're ready to discuss.

```html
<script type=”text/javascript”>
var test=’../example.php?cookie_data=’+escape(document.cookie);
</script>
```

Ask the candidate:

- What type of attack is taking place in this code?
- What is the attacker hoping to accomplish by injecting this code into a web app?
- How can this vulnerability be detected on a web app?

Send the candidate the link to [XSS Game Level 1](https://xss-game.appspot.com/level1){:target="_blank"}.

Ask the candidate:

- Please share your screen of the provided web site and demonstrate how a XSS attack is executed.
- Explain in your own words why this attack works.

> Being asked to demonstrate your proficiency in a technical skill is a common hoop you'll jump through as a cyber job applicant. Get ready to demonstrate your technical chops in both the interview as well as during any technical testing the organization subjects you to. You also may not always have the luxury of consulting outside resources.

Show the candidate this piece of code. Give the candidate a moment to read the code and let you know they're ready to discuss.

```php
$safe_data=filter_input(INPUT_GET, 'comment', FILTER_SANITIZE_SPECIAL_CHARS);
```

Ask the candidate:

- What technique is demonstrated in this code?
- How does this code help protect against the web application vulnerability we've discussed today?
- Finally, how are newly-discovered vulnerabilities documented by the security community at large?
  - What are the OWASP Top 10?

How well did the candidate demonstrate technical proficiency as well as communicate knowledge of the XSS attack technique?

## Interviewer Notes

- The first provided code is an example of cross-site scripting (XSS). This example is attempting to steal a cookie by way of executing Javascript. 
- XSS cookie thievery can be thwarted by means such as installing a SSL certificate, installing a security plugin, updating the website, and hardening the website.
- This second example code is a PHP function that demonstrates a technique called **input sanitization**, which is the process of checking user input strings for malicious code and preventing the execution of said code upon detection. 
- Input sanitization can be used to prevent the execution of Javascript on web application text input fields by only accepting non-Javascript text strings as valid input. Characters like tag brackets ( < > ) as well as entity ampersand ( & ) need to be filtered out by the web app so that they are not rendered by the client browser. The provided code is a PHP function that filters a single GET parameter at a time.
- Web application risks are well documented in the OWASP Top Ten Web Application Security Risks. The OWASP Top Ten 2017 edition includes the following:
  - Injection
  - Broken authentication
  - Sensitive data exposure
  - XML external entities (XXE)
  - Broken access control
  - Security misconfiguration
  - Cross-site scripting (XSS)
  - Insecure deserialization
  - Using vulnerable components
  - Insufficient logging & monitoring
