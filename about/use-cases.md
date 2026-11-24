# Use cases

Each row is a question people ask their assistant once Hippocampus is connected, and what the assistant does with it.

## By team

| Team | Ask | What happens |
|---|---|---|
| Legal and procurement | "Compare the termination clauses in our supplier contracts." | Searches across the contracts, reads each clause, quotes every one with its document, page and link |
| Business processes | "Check this offer against our discount rules." | Reads the current rules and names the rule behind each correction, with its page |
| Engineering | "What does the spec say about the retry limit, and which design decision set it?" | Reads the specification section and the decision record, quotes both with their pages |
| Finance and board | "What risks does the latest board report list?" | Finds the newest report by name, reads its risk section, cites each item |
| Operations and frontline | "What is the current routine for handing over medication?" | Searches the procedures, quotes the current routine and its page |
| HR | "What does the handbook say about remote work?" | Quotes the handbook passage and links to it |
| Research and regulatory | "What do our reports say about sample retention?" | Searches across every report, groups the extracts by document |
| Management | "Which documents changed this week?" | Lists the recently changed documents with their changed time, free |
| Anyone in a meeting | "Save these notes to /Meetings." | Adds the notes as a document the team can read and search |
| Developers | "Build an agent that answers HR questions from our handbook." | Uses search and read as the retrieval step, with citations in every answer |

## Working patterns

| Pattern | Tools | Why |
|---|---|---|
| Browse, then read | `open` → `read` | Free: no search needed when the person names the document |
| Search inside a folder | `search(within)` | Fewer, closer extracts; one search instead of several |
| Check an exact phrase | `read(contains)` | Free: finds where a word or phrase occurs |
| Cite as you go | `search` → `read(pages)` | The answer quotes the exact passage with its page |
| Keep a decision | `ingest` | The decision stays for the team once imported |

## What it is not for

| Request | Why not |
|---|---|
| General knowledge, weather, news | Hippocampus holds the company's own documents only |
| Creative writing with no company material | Nothing to look up |
| Documents the person may not see | The assistant acts as the person and sees only what they may see |
