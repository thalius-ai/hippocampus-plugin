# Security and privacy

The full statements are on https://www.thalius.ai/security and https://www.thalius.ai/legal/privacy. This page covers what matters when an AI assistant is connected.

## What this plugin does on your machine

| Item | Detail |
|---|---|
| Runs | Nothing. The plugin contains configuration, a skill and documentation only: no scripts, hooks or binaries |
| Connects to | `https://hippocampus.thalius.ai/mcp`, over HTTPS |
| Stores | Nothing. Your AI app keeps the sign-in token it receives |
| Secrets in the repo | None. Sign-in is OAuth in the browser; no key to paste |

## What travels where

| Data | Path |
|---|---|
| Your question | From your AI app to Hippocampus, as tool arguments (a query, an address) |
| Extracts and text | From Hippocampus to your AI app, only what a tool call asks for and only what you may see |
| Processing by the AI app | The AI app (Anthropic, OpenAI, Google, Microsoft, Cursor or another) processes the returned text under its own terms, which may be outside the EU |
| Your documents at rest | Stay in Hippocampus |

## Protections in Hippocampus

| Protection | Detail |
|---|---|
| Residency | Documents, the knowledge built from them and conversation history are stored in the EU (Finland), encrypted |
| Encryption keys | Each document has its own key; Free and Starter keys are managed in Google Cloud's key management service; Corporate can hold the keys in its own service |
| Access | The assistant acts as the signed-in person and sees exactly what that person may see |
| Training | Your documents are never used to train AI models |
| Revocation | Disconnect an AI app at any time in Hippocampus, under Connect to your AI → Connected apps |

## Contact

| Need | Where |
|---|---|
| Security report | https://www.thalius.ai/security |
| Privacy questions | privacy@thalius.ai |
| Support | support@thalius.ai |
