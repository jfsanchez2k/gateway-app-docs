---
title: Implementation Types
deprecated: false
hidden: false
metadata:
  robots: index
---
IoT: In this implementation, commands are sent through our API for IoT connections (TerminalManager). This implementation requires a key (POS\_KEY) to be sent in the request header, which is used to connect to the device.

Production Host: Payment Device Terminal Manager

Sandbox Host: [https://sandbox-terminal-manager.azurewebsites.net/](https://sandbox-terminal-manager.azurewebsites.net/)

IP: In this implementation, commands are sent directly to the terminal's IP address on port 8080.

Example IP Host: [http://10.0.0.16:8080/](http://10.0.0.16:8080/)
