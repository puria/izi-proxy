# Fork of
https://github.com/Roslovets-Inc/greenlock-prox
https://github.com/ardencod3/greenlock-proxy

# Greenlock Proxy Wrapper

Automatically get free SSL certificates from [Let’s Encrypt](https://letsencrypt.org/) and serve your sites over HTTPS.

## Features

- Automatically get **free** SSL sertificate from Let's Encrypt
- Easily redirect requests for your domain to any internal address (like server on any port)
- Distribute incoming traffic across several servers with built-in balancer
- Support Web Socket connection

Based on [greenlock-express](https://github.com/coolaj86/greenlock-express).

## How to Install

```bash
pnpm add https://github.com/puria/izi-proxy
```

## Example

```js
import IziProxy from 'izi-proxy'

// Configure Let's Encrypt settings to get SSL certificate
var proxy = new IziProxy({
    maintainerEmail: "example@email.com", // your email
    staging: true // true for testing, false for production (only after testing!)
});

// Just bind your domain to internal address - common example
// with parameter boolean activeGreenLock for greenlock activation
proxy.register(["exxxample.com", "uptime.exxxample.com"], ["http://localhost:3001"], true);

proxy.start();
```
