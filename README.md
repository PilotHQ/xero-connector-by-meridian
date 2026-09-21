# AI Agent Connector by Meridian

Connect supported AI agents to Xero through the free, hosted
[AI Agent Connector by Meridian](https://xero-connector.meridian.pilot.com/).

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

- MCP endpoint: `https://xero-connector.meridian.pilot.com/mcp`
- [Privacy policy](https://xero-connector.meridian.pilot.com/privacy)
- [Terms of service](https://xero-connector.meridian.pilot.com/terms)
- Support: `xero-mcp@pilot.com`

The connector is operated by [Pilot](https://pilot.com/).
