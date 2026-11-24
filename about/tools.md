# Tools (server 0.2.2)

The server at `https://hippocampus.thalius.ai/mcp` offers these tools. Every tool has a title and a read-only or write label. The server's own descriptions are the reference; this page summarises them.

| Tool | Title | Reads or writes | Cost | What it returns |
|---|---|---|---|---|
| `start` | Start here: workspace map, permissions, credits | read | free | Who you act as, what you may do, what actions cost and the credits left, the top folders and documents with one line each |
| `search` | Search documents by meaning | read | credits | Extracts S1, S2… grouped by document, each with section, pages and a link to cite; `within` narrows to a folder or document; `detail` is `short` or `full` |
| `find` | Find a document by name, or the recently changed | read | free | Up to 25 rows with address, changed time and source; one match also shows its summary and outline |
| `open` | Open a folder, document or section | read | free | A folder's contents, a document's summary and outline, or a section's summary and subsections |
| `read` | Read exact text, or find a word in it | read | free | The exact text in parts of about 16,000 characters with a link per part; with `contains`, where a word or phrase occurs |
| `balance` | Credit balance | read | free | The plan, credits left and used, the renewal date, and whether spending is paused |
| `ingest` | Add a document | write | credits per page | Markdown text you pass, or a one-time link to upload a file; only in folders where you can add documents yourself |
| `ingest_status` | Import progress | read | free | An import's status and, when done, each document's address and who can read it |

## Addresses

Every folder, document, section and page has an address such as `/Policies/Employee handbook`. Results give addresses; tools take them. `/` is the top.

## Accepted files for `ingest`

PDF (scanned PDFs too), Word (`.docx`), PowerPoint (`.pptx`), Excel (`.xlsx`), Markdown and text, up to 64 MiB.

## Limits

| Limit | Value |
|---|---|
| Calls at once | 8 |
| Calls a minute | 60 |
| Searches a minute | 20 |
| Time per call | 60 s |

`start` shows the limits that apply to the connection.

## Suggested order

`start` (once) → `find` or `open` to locate the document → `search` inside it → `read` the passage you cite.

## Prompts and guide

| Name | Kind | What it does |
|---|---|---|
| `ask` | Prompt, argument `question` | Answers from your documents and quotes the passage with its page and link |
| `overview` | Prompt | What is in the workspace: top folders, what you may do, credits left |
| `hippocampus://guide` | Resource (Markdown) | How an assistant searches, reads and cites at the lowest credit cost |

Clients that list prompts show them as commands, for example `/mcp__hippocampus__ask` in Claude Code.

## Before sign-in

The server card, `https://hippocampus.thalius.ai/mcp/server-card`, tells any client or directory what this server is without a token: name, description, icons and address. It lists no tools or data.
