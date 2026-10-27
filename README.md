# Prism IDE — your machine, every AI, one cockpit

A web IDE prototype that shows the target experience for a personal AI cockpit:

- **File explorer + editor** with syntax highlighting and terminal
- **MCP Hub** — aggregate every tool server (filesystem, git, shell, rea, browser) behind one endpoint
- **AI Cockpit** — Claude, GPT, Gemini and GLM side by side, each connected through MCP, with tool-call approval gates
- **Tunnel panel** — bring cloud AIs to your machine via Cloudflare Tunnel / Tailscale (zero-trust, MFA)

Fully self-contained single `index.html` (no build, no dependencies).

## Run it

Open `index.html` in any browser, or visit the GitHub Pages deployment.

## Making it real on your machine

```bash
# 1) install the REA MCP toolkit
npm install -g rea-agents && rea setup --all-detected

# 2) expose the local hub to cloud AIs (authenticated tunnel)
cloudflared tunnel --url http://127.0.0.1:4620
```
