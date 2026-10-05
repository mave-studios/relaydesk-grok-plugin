# RelayDesk for Grok

[![M8ven Verified](https://m8ven.ai/badge/mcp/mave-studios-relaydesk-grok-plugin-1rmtkh?variant=verified)](https://m8ven.ai/mcp/mave-studios/relaydesk-grok-plugin?s=readme)

RelayDesk connects Grok Build to computers, servers, and VMs that a user owns or administers and has explicitly paired with their RelayDesk account.

## Hosted MCP

- Review-compatible endpoint: `https://relay-desk-mjq6.vercel.app/mcp`
- Public product: `https://getrelaydesk.space`
- Authentication: OAuth in the browser
- Transport: HTTP MCP
- Operator: Mave Studios LLP

The legacy Vercel MCP hostname remains intentionally pinned in this marketplace package so the submitted Grok integration keeps the same MCP identity. New manual/custom connections may use `https://getrelaydesk.space/mcp`. The public product, setup, support, and legal experience uses the branded RelayDesk domain.

This repository is only the public Grok integration package. The RelayDesk product, hosted control plane, dashboard, and deployment source are maintained separately.

## What RelayDesk enables

After connecting RelayDesk and pairing a device, Grok can use RelayDesk MCP tools to work with normal files, run permitted commands, inspect processes, troubleshoot systems, and search the paired device.

RelayDesk is intended only for devices the signed-in user owns or is authorized to administer. Device-scoped remote execution requires an explicitly paired device and authenticated RelayDesk account.

## Network and credentials

The marketplace package connects to RelayDesk's hosted MCP service at `https://relay-desk-mjq6.vercel.app/mcp`. Browser OAuth is issued through RelayDesk's managed Supabase authorization server at `https://atuvyeoctkevglimkmka.supabase.co/auth/v1`. Users do not place API keys, passwords, SSH keys, or device secrets in this repository or in the Grok plugin configuration.

## Security boundaries

Normal OS-user files are available by default on a paired device. RelayDesk separately blocks recognized credential stores, private keys, authentication-secret paths, protected browser credential locations, and high-risk machine operations. Users may locally narrow filesystem access, and a remote AI session cannot silently widen that boundary. The public Grok package contains no executable installer, post-install downloader, obfuscated payload, or vendored product backend.

## User-facing pages

- Product: `https://getrelaydesk.space/`
- How it works: `https://getrelaydesk.space/how-it-works`
- Support: `https://getrelaydesk.space/support`
- Privacy: `https://getrelaydesk.space/privacy`
- Terms: `https://getrelaydesk.space/terms`

## Ownership and license

RelayDesk is operated by Mave Studios LLP. See `LICENSE` for the license covering this integration package.
