# CTF-Agents

My [opencode](https://opencode.ai) agents for CTF and cybersecurity work.
Each `.md` file is a subagent I use as a small team during a challenge.

## Agents

| File         | Does what                                             |
|--------------|-------------------------------------------------------|
| `general.md` | Orchestration / fallback agent                        |
| `web.md`     | Web exploitation & application security               |
| `pwn.md`     | Binary exploitation & reverse engineering             |
| `crypto.md`  | Cryptography & math-based attacks                     |
| `osint.md`   | Recon and open-source intelligence                    |
| `writeup.md` | Turns findings into a structured writeup              |

## Setup

Copy the agents into your opencode config:

```sh
git clone https://github.com/ThatBlueIris/CTF-Agents
cp *.md ~/.config/opencode/agents/      # global
# or .opencode/agents/ for a single project
```

`opencode.json` wires up two MCP servers (both auto-install on first run):

- `puppeteer` — headless browser for web challenges (`npx`)
- `fetch` — page fetching + markdown conversion (`uvx`)

## Usage

In opencode, pick an agent (`@web`, `@pwn`, etc.) and describe the target.
Agents save full output to `./reports/<task>.log` and report back a short
summary to the orchestrator.

## License

[MIT](LICENSE)
