# Liferay Sample .NET Client Extension

This is a **.NET client extension** that exposes secured APIs for **Liferay DXP** to consume using **OAuth 2.0**.  
It demonstrates how to:
- Protect API endpoints with JWT validation
- Use Liferay's OAuth 2.0 tokens to authorize API calls
- Dynamically retrieve and validate tokens against Liferay's JWKS endpoint

---

## Features

- Secured API endpoints accessible from Liferay DXP  
- OAuth 2.0 / JWT token validation using Liferay's JWKS  
- Middleware for token validation  
- Configurable via `appsettings.json`  

---

## Configuration

Example `appsettings.json`:

```json
"LiferaySettings": {
  "OAuth": {
    "ApplicationExternalReferenceCodes": "liferay-sample-etc-dot-net-oauth-application-user-agent",
    "Oauth2JWKSURI": "/o/oauth2/jwks",
    "UrlsExcludes": "/ready"
  },
  "LxcDXPMainDomain": "localhost:8080",
  "LxcDXPServerProtocol": "http"
}

