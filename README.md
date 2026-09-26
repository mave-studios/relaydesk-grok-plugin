# RelayDesk for Grok

RelayDesk connects Grok Build to computers, servers, and VMs that a user owns or administers and has explicitly paired with their RelayDesk account.

## Hosted MCP

- Endpoint: `https://relay-desk-mjq6.vercel.app/mcp`
- Authentication: OAuth in the browser
- Transport: HTTP MCP
- Operator: Mave Studios LLP

This repository is only the public Grok integration package. The RelayDesk product, hosted control plane, dashboard, and deployment source are maintained separately in a private repository.

## What RelayDesk enables

After connecting RelayDesk and pairing a device, Grok can use the RelayDesk MCP tools to work with permitted files, run approved commands, inspect processes, troubleshoot systems, and search configured workspaces on that device.

RelayDesk is intended only for devices the signed-in user owns or is authorized to administer. Device-scoped remote execution requires explicit acknowledgement through the RelayDesk MCP interface.

## Network and credentials

The plugin connects to RelayDesk's hosted MCP service at `https://relay-desk-mjq6.vercel.app/mcp`. Browser OAuth is issued through RelayDesk's managed Supabase authorization server at `https://atuvyeoctkevglimkmka.supabase.co/auth/v1`. Users do not place API keys, passwords, SSH keys, or device secrets in this repository or in the Grok plugin configuration.

## Security boundaries

RelayDesk is designed to keep remote access scoped to explicitly paired devices and authenticated accounts. Sensitive credential locations and secret-bearing files are restricted by RelayDesk safety controls. The public Grok package contains no executable installer, post-install downloader, obfuscated payload, or vendored product backend.

## User-facing pages

- Product: `https://relay-desk-mjq6.vercel.app/`
- Support: `https://relay-desk-mjq6.vercel.app/support`
- Privacy: `https://relay-desk-mjq6.vercel.app/privacy`
- Terms: `https://relay-desk-mjq6.vercel.app/terms`

## Ownership and license

RelayDesk is operated by Mave Studios LLP. See `LICENSE` for the license covering this integration package.
