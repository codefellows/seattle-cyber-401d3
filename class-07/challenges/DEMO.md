# Ops Challenge - File Encryption Script Part 2 of 3

## Demo Code

The demo code below introduces concepts necessary to complete the challenge.

```python
#!/usr/bin/env python3

# Purpose: In this demo, we'll recursively dig a folder for its contents, then return each path. 
# This will allow us to perform operations en-masse, such as encryption.

# Import libraries
import os

# Begin recursive directory crawl
for root, dirs, files in os.walk(".", topdown=False):
# For each hit, concatenate the current directory pathing to left of result
   for name in files:
      print(os.path.join(root, name))
   for name in dirs:
      print(os.path.join(root, name))
```
