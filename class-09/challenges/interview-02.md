# Interview 02

## Interview Question

- Ask the candidate: 
  - What is PKI?
    - Is PKI symmetric or asymmetric and why?
    - Provide an example of PKI in action, and compose a drawing or diagram using draw.io or Zoom whiteboard.
  - What’s the difference between symmetric and public-key cryptography?

## Interviewer Notes

- **PKI** stands for public key infrastructure, a system that utilizes public keys, private keys, and digital certificates to protect data, vouch for user identities/devices/applications, and secure communications end-to-end.
  - PKI is a form of **asymmetric key cryptography** because it uses two different keys, a public and private key. The sender never knows/possesses the private key.
  - One example use of PKI is to encrypt a message using the recipient's public key. After the message is encrypted, only the recipient can decrypt it by using the private/secret key. Here is how this would look in a diagram:
    
    ![pki.jpg](../assets/pki.jpg)

  - Another example is when you visit a website with an SSL certificate installed via HTTPS protocol. The SSL certificate helps create a secure connection between a website’s server and a client (visitor) browser. Data sent over this connection is encrypted, which means that regular plaintext is turned into ciphertext, rendering it unreadable. 

- **Symmetric key cryptography** uses the same secret key for both encryption and decryption of the data. This secret key is shared by the recipient and the sender.
