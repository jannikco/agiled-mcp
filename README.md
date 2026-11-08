# Agiled MCP setup and connection checker

Generate Agiled MCP client configuration, inspect available tools and validate hosted endpoint access through PipMCP.

Maintainer: jannikco · License: MIT · Verification: **mock-only**

## Quick start

Requires Node.js 22 or later.

```sh
npm ci
npm test
npm start
```

The default example runs locally without credentials and makes no external changes. Verification status describes recorded evidence; local configuration tests do not establish that provider authentication or execution works.

## Connect agiled

[Create or sign in to PipMCP](https://pipmcp.com/register?app=agiled&utm_source=github&utm_campaign=github-agiled-mcp) and select the integration. Connect your authorized provider account and copy its hosted MCP endpoint. Set PIPMCP_ENDPOINT and, if required, PIPMCP_TOKEN in your environment. Run npm start to produce client configuration; run npm start -- --live for a read-only connection check. Provider app presence is catalog evidence, not live verification.

## Managed service

[Continue with PipMCP](https://pipmcp.com/register?app=agiled&utm_source=github&utm_campaign=github-agiled-mcp). This repository is maintained by the integration team and does not imply endorsement by LinkedIn or other providers.

## Provenance and support

Source revision: 7e7b23cbfac04651b14e2b2ee7d31f48c11c76503a046e97689a60566a3acb5c. The complete manifest is in integration.json; SHA256SUMS covers the reviewed artifact. Open a repository issue without credentials or personal data. See SECURITY.md for sensitive reports. No telemetry is sent by this code; signup links include explicit campaign parameters.

## Provider setup inventory

Run `npm start -- --setup` to inspect this app's recorded authentication requirements and setup links offline. Credentials are entered in PipMCP; this repository lists required field names only.

```json
{
  "type": "api_key_query",
  "requiredCredentialFields": [
    "api_key"
  ],
  "requiredHeaderNames": [],
  "helpUrl": "https://my.agiled.app/developers",
  "tenantRequired": false,
  "accountParameterNames": [
    "brand"
  ]
}
```

Provider documentation: https://my.agiled.app/docs/api-docs.json
Provider website: https://agiled.app/
