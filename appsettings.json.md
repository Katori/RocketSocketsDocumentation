---
layout: default
title: appsettings.json
permalink: /appsettings
nav_order: 3
---

# appsettings.json

The following parameters are available in `appsettings.json`, listed with their default settings:

```json
{
  "RocketSocketsConfig": {
    "unityBinaryConnectionPort": 1337,
    "unityConnectionTickRate": 33,
    "defaultWebSocketsConnectionPort": 7779,
    "useSecureWebSockets": false,
    "webSocketsCertificatePath": "",
    "webSocketsCertificatePassword": ""
  }
}
```

The following is a list of them with short descriptions:

- `unityBinaryConnectionPort` - The port to connect with Unity. **Must be set the same as in the RocketSockets Transport inside Unity.**
- `unityConnectionTickRate` - The rate to poll Unity for updates. Set to 16hz for "60fps".
- `defaultWebSocketsConnectionPort` - The port of the default server that will start when RocketSockets starts.
- `useSecureWebSockets` - Whether or not to enable WSS.
- `webSocketsCertificatePath` - The path to the certificate, relative to the RocketSockets binary. Must be in PFX format and **must be configured to enable WSS.**
- `webSocketsCertificatePassword` - The password to the certificate from `webSocketsCertificatePath`.
