---
layout: default
title: WebSocketsSecure (WSS) Configuration
permalink: /websocketssecure
nav_order: 4
---

# WebSocketsSecure (WSS) Configuration

## Prerequisites

- `certbot` and `openssl`
- [RocketSockets](https://rocketsockets.network)

## Instructions

1. Run `sudo certbot certonly` on your server that is hooked up to a domain name to generate a HTTPS certificate. Use the `standalone` option.
2. `cd` into the directory specified by `certbot` in its final stages (`etc/letsencrypt/`someOtherPath) and run the following command: `openssl pkcs12 -export -out certificate.pfx -inkey privkey.pem -in fullchain.pem`. Configure the certificate with a password and remember it.
3. Copy the generated `certificate.pfx` to the folder where `./RocketSockets` lives.
4. Configure RocketSocket's `appsettings.json` file with the following settings:

```json
{
  "RocketSocketsConfig": {
    // snip
    "useSecureWebSockets": true,
    "webSocketsCertificatePath": "certificate.pfx",
    "webSocketsCertificatePassword": "passwordYouSelected"
  }
}
```

You should be able to run WebSocketsSecure servers now! A secure server will start automatically, but you can start secure servers with the `--secure` switch and nonsecure servers with the `--nosecure` switch.