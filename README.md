# Xero Connector by Meridian

Connect supported AI agents to Xero through the free, hosted
[Xero Connector by Meridian](https://starter.meridian.pilot.com/help/xero).

The connector can work with multiple Xero organisations and supports both
read-only and read-and-write access. You choose the access level for each
organisation in Meridian.

## Install in Gemini CLI

```sh
gemini extensions install https://github.com/PilotHQ/xero-connector-by-meridian
```

Restart Gemini CLI, then authorize the connector:

```text
/mcp auth xero-connector-by-meridian
```

The browser flow lets you sign in to Meridian, connect Xero organisations, and
approve Gemini CLI's access. OAuth tokens are managed by Gemini CLI; this
repository contains no credentials or connector implementation code.

## Install in Grok Build

```sh
grok plugin install PilotHQ/xero-connector-by-meridian --trust
```

The plugin adds one hosted MCP connection. Grok opens the provider's OAuth
sign-in and consent flow when authentication is required. The package includes
no local executable, hooks, API keys, or credentials.

## Install in GitHub Copilot

```sh
copilot plugin install PilotHQ/xero-connector-by-meridian
```

The repository uses the portable Agent Plugins 1.0 format, so the same MCP
configuration is also supported by VS Code's Agent Plugins experience and other
compatible clients.

## Useful requests

- List the Xero organisations I have connected.
- Show this month's profit and loss statement.
- Find unpaid invoices for this organisation.
- Create a draft invoice after showing me exactly what will be created.

## Security and support

- [Setup and troubleshooting](https://starter.meridian.pilot.com/help/xero#limitations)
- MCP endpoint: `https://xero-connector.meridian.pilot.com/mcp`
- [Privacy policy](https://starter.meridian.pilot.com/privacy)
- [Terms of service](https://starter.meridian.pilot.com/terms)
- Support: `xero-connector@pilot.com`

The connector is operated by [Pilot](https://pilot.com/).

## Network access

The MCP connection and OAuth discovery use `https://xero-connector.meridian.pilot.com`.
Sign-in/consent may use `https://starter.meridian.pilot.com`; connecting or
refreshing the underlying accounting connection uses Xero's authorization service.
Users sign in to their own Meridian account and explicitly authorize access.
No accounting data is bundled in this repository.
