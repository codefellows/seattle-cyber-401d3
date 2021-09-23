# Ops Challenge - Automated Brute Force Wordlist Attack Tool Part 2 of 3

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

```python
# Sample SSH authentication script

from pexpect import pxssh
import getpass

s = pxssh.pxssh()
host = ###
username = ###
pwd = ###

try:
    s.login(host, username, pwd)
    s.sendline('uptime')
    s.prompt()
    print(s.before)        # print everything before the prompt.
    s.sendline('ls -l')
    s.prompt()
    print(s.before)
    s.sendline('df')
    s.prompt()
    print(s.before)
    s.logout()

except pxssh.ExceptionPxssh as e:
    print("pxssh failed on login.")
    print(e)

```
