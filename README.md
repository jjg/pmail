# pmail
Simple, secure, private messaging system

This project consists of a protocol for a private messaging system and example server and client software.

The Protocol

pmail is build around public key encryption.  Messages are encrypted by clients and routed to recipients using the recipients public key.  

A message is sent by encrypting the body of the message using the recipients public key and then POSTing the message to the server at a URI including the recipients public key:

  POST http://server.com/<public key>

