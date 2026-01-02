+++
title = "EDDI"
description = "A secure application launcher that exposes web applications exclusively as Tor hidden services. All inter-process communication uses Unix domain sockets, achieving zero TCP port exposure."
weight = 4
template = "project.html"

[extra]
category = "security"
status = "Experimental"
logo = "images/eddi_logo.png"
github = "https://github.com/marctjones/eddi"
+++

## Overview

EDDI (Encapsulated Distributed Desktop Interface) takes network isolation to its logical extreme. Instead of merely avoiding TCP ports on localhost, EDDI ensures your application is only accessible via Tor hidden services—providing both transport encryption and anonymity by default.

## Features

- **Applications accessible only via .onion addresses**
- **No local network ports** to discover or attack
- **Built-in Tor integration** and hidden service management
- **Unix domain sockets** for all local IPC

## Use Cases

EDDI is designed for scenarios where network exposure must be minimized:

- **Personal services** you want accessible from anywhere without exposing your home IP
- **Sensitive applications** that should never be discoverable via network scanning
- **Development environments** for Tor-based services

## How It Works

1. EDDI starts your application, configured to listen on a Unix domain socket
2. EDDI configures Tor to create a hidden service pointing to that socket
3. The application is now accessible only via its .onion address
4. No TCP ports are opened on any interface

## Architecture

```
[Tor Browser] <--onion--> [Tor Network] <--onion--> [EDDI]
                                                      |
                                              [Unix Socket]
                                                      |
                                              [Your Application]
```

The entire path from user to application is encrypted and anonymized, with no local network exposure.
