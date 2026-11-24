# Installing Thalius Hippocampus

Hippocampus is a remote MCP server. Nothing is installed locally and no API key is needed.

1. Make sure the person has a Thalius account. A free account works: https://hippocampus.thalius.ai/register
2. Add a remote MCP server named `hippocampus` with the address `https://hippocampus.thalius.ai/mcp` and the Streamable HTTP transport. In Cline: MCP Servers → Remote Servers, name `hippocampus`, the address, Streamable HTTP, then Add Server. When editing the settings file instead, set `"type": "streamableHttp"`.
3. The first call answers HTTP 401. That is expected: the client reads the sign-in metadata and shows an Authenticate button or opens a browser window. The person signs in to Hippocampus there.
4. Check the connection by calling the tool `start`. It returns the workspace name, the person's permissions, the credits and the top folders. It is free.

Settings file entry (Cline):

```json
{
  "mcpServers": {
    "hippocampus": {
      "type": "streamableHttp",
      "url": "https://hippocampus.thalius.ai/mcp",
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

Guides for other clients: https://www.thalius.ai/developers/mcp
