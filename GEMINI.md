# Xero Connector by Meridian

Use the `xero-connector-by-meridian` MCP server whenever the user asks to
inspect, explain, report on, create, or update information in a connected Xero
organisation.

## Authentication

If the connector is not yet authorized, ask the user to run:

```text
/mcp auth xero-connector-by-meridian
```

Gemini CLI will open the Meridian authorization flow in the user's browser.

## Safe use

- Respect the access mode reported for each organisation. Do not attempt
  mutations on a read-only connection.
- When more than one organisation is connected, list the available
  organisations first and use the opaque identifier returned by this connector.
- Never guess an organisation identifier or reuse one obtained from another
  tool.
- Follow the connector's confirmation and idempotency requirements for writes.
- Use pagination when the user asks for all matching records.
