# Ops Challenge - Uptime Sensor Tool Part 1 of 2

## Formatting Your Scripts

All Python scripts should include the shebang `#!/usr/bin/env python3` and be named with a `.py` file extension.

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

> Note: You may use any or none of the code provided below to complete the challenge objectives.

### Python's datetime library

You may wish to utilize Python's datetime library for this challenge.

```python
#!/usr/bin/env python3

import datetime

now = datetime.datetime.now()
print("Current date and time: ")
print(str(now))
```

### Python's time library

Python also has a time library with a very useful `sleep` function that lets us pause the script execution for the specified amount of time.

```python
#!/usr/bin/env python3

import time

print "Start : %s" % time.ctime()
time.sleep( 5 )
print "End : %s" % time.ctime()

```

### Creating an infinite loop

We can use `while True:` to create an unending cycle of commands repeated in perpetuity.

```python

#!/usr/bin/env python3

import time

while True:
   print "Start : %s" % time.ctime()
   time.sleep( 5 )
   print "End : %s" % time.ctime()

```

### Pinging using the OS commands

There are a few ways to approach using ping. This first approach uses operating system commands and is probably the easiest to perform.

```python

#!/usr/bin/env python3

import os;

print(os.system("ping 127.0.0.1"))

```

### Pinging single targets using pythonping

Another approach is to use the `pythonping` library. First you'll need to install pip3. Run `apt install python3-pip` to load up pip for Python3.

Pip3 (PyPi for Python 3) is a library management tool for Python3. We'll use Python3 for most of Ops 401.

Load [pythonping 1.0.14](https://pypi.org/project/pythonping/) using `sudo pip3 install pythonping`.

Execute the below script with `sudo` to avoid permissions issues.

```python

#!/usr/bin/env python3

# The above shebang line is good convention for Python scripts in 401.

# Import Python libraries
from pythonping import ping

# Main
print(ping('8.8.8.8', verbose=True))

```

### Pinging multiple targets using multiping

Another tool you can use is multiping.

Install with `sudo pip3 install multiping`.

```python

#!/usr/bin/env python3

# A small demo, which demonstrates how to use MultiPing

from multiping import MultiPing
from multiping import multi_ping

if __name__ == "__main__":

    # A list of addresses and names, which should be pinged.
    addrs = ["8.8.8.8", "cnn.com", "127.0.0.1", "youtube.com",
             "2001:4860:4860::8888"]

    print("sending one round of pings and checking twice for responses")
    mp = MultiPing(addrs)
    mp.send()
    # First attempt: We probably will only have received response from
    # localhost so far. Note: 0.01 seconds is usually a very unrealistic
    # timeout value. 1 second, or so, may be more useful in a real world
    # example.
    responses, no_responses = mp.receive(0.01)

    print("   received responses:  %s" % list(responses.keys()))
    print("   no responses so far: %s" % no_responses)

    # By now we should have received responses from the others as well
    print("   --- trying another receive ---")
    responses, no_responses = mp.receive(0.1)
    print("   received responses:  %s" % list(responses.keys()))
    print("   still no responses:  %s" % no_responses)
    print("")

    # Sometimes ICMP packets can get lost. It's easy to retry (re-send the
    # ping) to those hosts that haven't responded, yet. Send can be called
    # multiple times and will result in pings to be resent to those addresses
    # from which we have not heard back, yet. Here we try three pings max.
    print("sending again, but waiting with retries if no response received")
    mp = MultiPing(addrs)
    for i in range(3):
        mp.send()
        responses, no_response = mp.receive(0.01)

        print("    received responses:     %s" % list(responses.keys()))
        if not no_response:
            print("    all done, received responses from everyone")
            break
        else:
            print("    %d. retry, resending to: %s" % (i + 1, no_response))
    if no_response:
        print("    no response received in time, even after 3 retries: %s" %
              no_response)
    print("")

    # Having control over your retries is powerful and gives you lots of
    # flexibility, but sometimes you don't want to deal with it manually and
    # just want 'the right thing' to be done for you.
    #
    # Fortunately, MultiPing provides a ready-made function to do the retry for
    # you, called multi_ping(). Specify the overall timeout and the number of
    # additional retries (which are attempted within this timeout). Omit the
    # 'retry' parameter or set to 0 and there will only be a single send.
    #
    # We are also adding an address we won't be able to resolve and set the
    # 'ignore_lookup_errors' flag, to show that those can be ignored if wanted.
    # They will just appear in the 'no response' return list. If the flag is
    # not set then an exception would be thrown.
    addrs.append("cannot.resolve.thiscom")
    print("sending again, waiting with retries via provided send_receive()")
    responses, no_response = multi_ping(addrs, timeout=0.5, retry=2,
                                        ignore_lookup_errors=True)
    print("    reponses: %s" % list(responses.keys()))
    if no_responses:
        print("    no response received in time, even after retries: %s" %
              no_response)

```

These code samples should help you complete today's Ops Challenge. Good luck
