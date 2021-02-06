# TextSecureProtocol
Sabanci University CS 411-507 Cryptography Course Term Project

Develop a simplified version of the TextSecure protocol, which provides forward secrecy and deniability, a variant of which is used in different applications such as WhatsApp.

This project was implemented in 3 phases. At each phase we implemented different feature of the TextSecure protocol.

In the project we developed the client side of the TextSecure protocol. 
First, the client generates a long term private key and public key to use in Station-to-Station protocol to sign messages and verify signatures. In this project, we used Elliptic Curve Digital Signature Algorithm. 
Second, implemented the Station-to-Station protocol for mutual key and entity authentication.

The client generates ephemeral keys for sending and receiving messages from the other entities. After generating them, client signs these ephemeral keys and register them to the server. To send messages to other entites and receive messages from them, these two entites create a session key using the ephemeral public key of the other party and ephemeral private key of theirs. 

For encryption process, we used AES-CTR and compute HMAC-SHA256 of the message.

At the end of the project, we can send messages back and forth with my friend, these messages are secured with TextSecure protocol that we implemented. 
