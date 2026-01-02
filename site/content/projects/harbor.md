+++
title = "Harbor"
description = "A desktop application framework as an Electron alternative. Harbor embeds the Servo browser engine to render web UIs, communicating with local backends exclusively over Unix Domain Sockets (Named Pipes on Windows)."
weight = 3
template = "project.html"

[extra]
category = "security"
status = "Experimental"
logo = "images/harbor_logo.png"
github = "https://github.com/marctjones/harbor"

[[extra.related]]
name = "Rigging"
url = "https://github.com/marctjones/rigging"
description = "Scaffold generator for Harbor applications. Creates project structure, configuration, and build tooling."

[[extra.related]]
name = "Compass"
url = "https://github.com/marctjones/compass"
description = "Developer tools for Harbor. Live reload, request inspection, and debugging utilities."

[[extra.related]]
name = "Corsair"
url = "https://github.com/marctjones/corsair"
description = "Packaging and distribution toolchain. Handles bundling, code signing, and platform-specific installers."
+++

## Overview

Electron solved a real problem—building cross-platform desktop apps with web technologies—but introduced new ones. Every Electron app bundles a full Chromium instance, consuming hundreds of megabytes of disk space and significant memory. Worse, Electron apps expose TCP ports for their internal communication, creating attack surface on every machine they run on.

Harbor takes a different approach: use the Servo browser engine (smaller, Rust-based) and communicate over Unix Domain Sockets instead of TCP.

## Features

- **Zero network exposure**—no TCP ports to scan or attack
- **Use any HTTP backend**: Flask, FastAPI, Node.js, gunicorn, nginx
- **Managed backend lifecycle**: start, health check, restart on crash, cleanup on exit
- **Lower memory usage and smaller bundles** than Electron

## Architecture

Harbor consists of three components:

1. **Shell**: The Servo-based browser window that renders your UI
2. **Backend**: Your HTTP server (any language/framework)
3. **Bridge**: Unix Domain Socket (or Named Pipe) connecting them

The bridge is the key innovation. By using filesystem-based sockets instead of TCP:

- No ports are opened on the network
- Communication is restricted to the local machine
- OS-level permissions control access
- No firewall configuration needed

## Security Model

Traditional Electron apps expose localhost ports that any process on the machine can connect to. Harbor's socket-based approach means:

- Only processes with filesystem access to the socket can connect
- Socket permissions can be restricted to the current user
- No network scanners can discover your app's internal API
