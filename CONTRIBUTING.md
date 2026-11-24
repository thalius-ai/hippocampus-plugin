# Contributing

This repository is generated. Every file comes from `plugin/` in Thalius's server repository by `plugin/build-public.mjs`, and a release of the server publishes it here with the same version. Pull requests here are welcome as suggestions; the change is made at the source and comes back with the next release.

| What | Where it comes from |
|---|---|
| Names, descriptions, links, prompts, test cases | `plugin/public-src/listing.json` |
| Guidance (skill, AGENTS.md, GEMINI.md, Cursor rule) | `plugin/src/hippocampus.md` |
| About pages, README, install notes | `plugin/public-src/` |
| Icons | `plugin/public-src/assets/` |
| Server address and version | `plugin/build.mjs` |

Before a store submission:

| Check | Command or step |
|---|---|
| Claude manifest | `claude plugin validate --strict .` |
| Antigravity manifest | `agy plugin validate --json` |
| Gemini gallery | the repository topic `gemini-cli-extension` |
| OpenAI review | `review.demo_recording_url` added to `plugin.json` once the demo video exists |
| Registry | `mcp-publisher publish` with `server.json` |

Report security issues through https://www.thalius.ai/security, not as public issues.
