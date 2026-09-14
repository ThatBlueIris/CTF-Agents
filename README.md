# CTF-Agents

My [opencode](https://opencode.ai) agents for CTF and cybersecurity work.
Each file is a subagent I use as a small team during a challenge.

All agents live in `.opencode/agents/`:

- `general.md` - orchestration / fallback agent
- `web.md` - web exploitation & application security
- `pwn.md` - binary exploitation & reverse engineering
- `crypto.md` - cryptography & math-based attacks
- `osint.md` - recon and open-source intelligence
- `writeup.md` - turns findings into a structured writeup

## Setup

Clone it and run opencode from the project root - everything auto-loads:

    git clone https://github.com/ThatBlueIris/CTF-Agents
    cd CTF-Agents
    opencode

Want the agents globally instead?

    cp .opencode/agents/*.md ~/.config/opencode/agents/

## MCP servers

`.opencode/opencode.json` enables two MCP servers (auto-install on first run):

- `puppeteer` - headless browser for web challenges (`npx`)
- `fetch` - page fetching + markdown conversion (`uvx`)

## Usage

In opencode, pick an agent (`@web`, `@pwn`, etc.) and describe the target.
Agents save full output to `./reports/<task>.log` and report a short summary
back to the orchestrator.

## License
MIT
