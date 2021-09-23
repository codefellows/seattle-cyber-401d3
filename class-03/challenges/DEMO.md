# Ops Challenge - Uptime Sensor Tool Part 2 of 2

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

```python

# This script is optimized for Gmail. Yours may vary for this assignment. Replace values as indicated for the script to function.

import smtplib
server = smtplib.SMTP_SSL(MAILSERVER, PORTNUMBER) # Replace MAILSERVER and PORTNUMBER with the correct values
server.ehlo()

# Next, log in to the server
server.login(SENDEREMAILADDRESS, PASSWORD) # Replace SENDEREMAILADDRESS and PASSWORD with the correct values

# Send the mail
msg = "Hello!" # The /n separates the message from the headers
server.sendmail(SENDEREMAILADDRESS, DESTINATIONEMAILADDRESS, msg) # Replace SENDEREMAILADDRESS and DESTINATIONEMAILADDRESS with the correct values
server.quit()

```
