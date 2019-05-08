---
layout: default
title: Changelog
permalink: /changelog
nav_order: 2
---

# Changelog

## Version 1.1 - 05/08/2019

- RocketSockets now supports TLS1.2
- Start secure servers from the RS Command Line with the `--secure` switch and nonsecure servers with the `--nosecure` switch. [This requires you to configure WSS before starting RocketSockets.]({{ "/websocketssecure" | relative_url }})
- Fixed a (harmless) exception that was raised to the Unity level during each disconnect

## Version 1.0 - 05/02/2019

- Welcome to RocketSockets!
- `StartWebSockets` and `StopWebSockets` commands are available
- Configuration is available via JSON
