# Test cases

The same cases serve three purposes: the store reviews (OpenAI asks for exactly 5 positive and 3 negative cases), the `claude plugin eval` suite in `evals/`, and a manual check before each release. They are generated from one source, so the three never drift.

## Positive: the assistant should use Hippocampus

| Case | Prompt | Tools | Expected |
|---|---|---|---|
| A free overview of the workspace before any search | What's in our Hippocampus knowledge base? | `start` | Calls start once and lists the top folders with one line each. Spends no credits and does not search. |
| A cited answer from one document | What is the notice period in our supplier agreement? Quote it. | `search`, `read` | Answers with the exact sentence from the supplier agreement, names the document and the page, and gives the link that opens the passage. Does not invent a period that the document does not state. |
| Browsing a folder without spending credits | Open the Policies folder and list what's in it. | `open` | Calls open on /Policies and lists the documents with one line each. No search, no credits. |
| Finding what changed recently | Which of our documents changed in the last week? | `find` | Calls find for the most recently changed documents and lists them with their changed time. No search, no credits. |
| Keeping a decision for the team | Save these meeting notes to /Meetings in Hippocampus: Decision: the launch moves to 3 March. Owner: Anna. | `ingest`, `ingest_status` | Imports the notes as a Markdown document in /Meetings (on a connection made read-only, the person is first asked to allow adding documents), follows the import and reports the new document's address and who can read it. |

## Negative: the assistant should not call Hippocampus

| Case | Prompt |
|---|---|
| A general question that is not about company documents | What will the weather be in Stockholm tomorrow? |
| Creative writing with no company material | Write a short poem about autumn. |
| A calculation that needs no company documents | Convert 100 euros to Swedish kronor. |

## Demo workspace the cases need

The reviewer account must open a workspace that holds:

| Folder | Document | Must contain |
|---|---|---|
| `/Policies` | Employee handbook | A section on remote work |
| `/Contracts` | Supplier agreement | A clause with the notice period |
| `/Meetings` | (any notes) | At least one document changed within 7 days of the review |
| `/Reports` | Board report | A list of risks |

The reviewer account needs password sign-in without MFA or an email link, credits that do not run out, and no expiry. Its credentials go only into the store forms, never into this repository.
