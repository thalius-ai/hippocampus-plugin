<!-- Generated from plugin/src/hippocampus.md by plugin/build.mjs. Edit the source, then run: node plugin/build.mjs -->

# Worked examples

## 1. A named document, then an exact clause (free)

Person: "What notice period does our standard supplier contract give?"

1. `find(name: "supplier contract")` → rows with title, kind, address and the provenance line. Two rows are titled "Supplier contract": one says `Changed: 2026-10-02 09:14 UTC · Source: Google Drive · Version: newest of 2 here`, the other `Changed: 2025-03-14 16:40 UTC · Source: imported file · Version: older here; newer: "/Legal/Supplier contract"`.
2. Take the newest: `read(address: "/Legal/Supplier contract", contains: "notice")` → two rows; the first, page 7 in section "Termination", carries the whole clause's paragraph and `Read: read(address="/Legal/Supplier contract", pages="7")`.
3. To cite it, `read(address: "/Legal/Supplier contract", pages: "7")` → the clause, and after it the part's `Link: … (page 7)` line.
4. Answer: "Either party may end the contract with 90 days' written notice [p. 7](link). I used the newest version (changed 2026-10-02 09:14 UTC, from Google Drive); an older imported version from 2025-03-14 also exists." Sources: Supplier contract, /Legal/Supplier contract, changed 2026-10-02 09:14 UTC.

No search was needed, so no credits were spent.

## 2. A question by meaning (one search)

Person: "How do we handle a customer data breach?"

1. `search(query: "personal data breach notification procedure")` → short briefing: extracts [S1]–[S4] from the incident response plan and the privacy policy.
2. [S2] is marked "cut short" just before the deadlines. Instead of a full search, `read(address, pages)` the pages that extract names.
3. Answer with inline citations: "Report to the data protection officer within 24 hours [S1](link); the authority is notified within 72 hours [p. 4](link)." Sources at the end.
4. If the result had opened with the weak-match line and no extract answered: "The workspace's documents do not describe a breach procedure." No second broad search.
