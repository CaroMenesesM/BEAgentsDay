# BEAgentsDay
BE Repo for Agents Day Hackathon submission

# Birdseye Life SRE

Birdseye is a personal SRE agent that turns Gmail signals into PagerDuty incidents using n8n, Claude, and PagerDuty MCP.

## What it does

1. n8n reads recent Gmail messages.
2. n8n generates a structured MCP prompt.
3. Claude uses PagerDuty MCP tools to create an incident.
4. A live dashboard displays latest PagerDuty incidents.

## Architecture

Gmail → n8n → Claude Desktop → PagerDuty MCP → PagerDuty → Dashboard

## Setup

### 1. n8n

Import the workflows in `/n8n`.

Required workflows:
- `gmail-to-mcp-prompt.workflow.json`
- `pagerduty-dashboard-proxy.workflow.json`

### 2. Claude MCP

## Repo structure:

birdseye-life-sre/
├─ README.md
├─ dashboard/
│  └─ birdseye-dashboard-ready.html
├─ n8n/
│  ├─ gmail-to-mcp-prompt.workflow.json
│  └─ pagerduty-dashboard-proxy.workflow.json
├─ claude/
│  ├─ claude_desktop_config.example.json
│  └─ mcp-prompts.md
├─ docs/
│  ├─ architecture.md
│  ├─ demo-script.md
│  └─ screenshots/
└─ .gitignore
