# What Thalius Hippocampus is

Hippocampus turns a company's documents into an expert its AI can consult. People import policies, contracts, procedures, specifications, reports and notes (PDF, scanned PDF, Word, PowerPoint, Excel, Markdown or text), or sync them from Google Drive and OneDrive. Behind it is an LLM wiki: at import, language models write every document into folders, documents and sections, each with a summary, an outline and the exact text.

Vector search cuts documents into chunks and mixes them. It is fast on simple lookups but loses the thread on complex questions and large collections. Hippocampus keeps each document whole, so an answer comes from the right document, section and page, and the AI reads a few passages instead of whole files.

This plugin connects an AI assistant to that expert over the Model Context Protocol (MCP). The assistant answers from the company's source of truth and quotes the passage it used, with the page and a link that opens it.

## Who it is for

| Who | What they get |
|---|---|
| Teams with many documents | The exact clause, figure or routine, with the page it stands on |
| People who must check answers | Every extract carries its document, section, pages and a link |
| Developers building agents | Retrieval over the company's documents through MCP or the API, on a free account |
| Companies with sensitive material | Encrypted in the EU, documents stored in Finland; the assistant sees only what the signed-in person may see |

## What the assistant can do

| Task | Tool | Cost |
|---|---|---|
| See the workspace map, permissions and credits | `start` | free |
| Search by meaning, with cited extracts | `search` | credits |
| Find a document by name, or the recently changed | `find` | free |
| Open a folder, a document outline or a section | `open` | free |
| Read the exact text, or find a word in it | `read` | free |
| Show the plan and credits left | `balance` | free |
| Add a document (Markdown text or a file) | `ingest`, `ingest_status` | credits per page |

Full reference: [tools.md](tools.md).

## How it connects

| Item | Value |
|---|---|
| Server address | `https://hippocampus.thalius.ai/mcp` |
| Transport | Streamable HTTP |
| Sign-in | OAuth in the browser; no key to paste |
| Account | A Thalius account; a free account works |
| Acts as | The signed-in person, with their access |

## Links

- Website: https://www.thalius.ai
- Developer docs: https://www.thalius.ai/developers/mcp
- Security: https://www.thalius.ai/security
- Plans and prices: https://www.thalius.ai/pricing
