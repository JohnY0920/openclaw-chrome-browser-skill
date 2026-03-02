# browser-use Skill for OpenClaw

A comprehensive browser automation skill for OpenClaw agents using the `browser-use` CLI.

## Overview

This skill enables agents to:
- Navigate websites and extract data
- Fill forms and interact with web elements
- Take screenshots and capture page state
- Run AI-powered browser agents in the cloud
- Manage browser sessions and profiles
- Create tunnels to expose local development servers

## Installation

1. Install the `browser-use` CLI:
```bash
pip install browser-use
```

2. Verify installation:
```bash
browser-use doctor
```

3. Copy this skill to your OpenClaw skills directory:
```bash
cp -r browser-use ~/.claw/skills/
```

## Quick Start

```bash
# Open a website
browser-use open https://example.com

# Get page state (shows clickable elements)
browser-use state

# Click an element (use index from state)
browser-use click 5

# Type text
browser-use input 3 "Hello World"

# Take screenshot
browser-use screenshot page.png

# Close browser
browser-use close
```

## Browser Modes

| Mode | Description | Use Case |
|------|-------------|----------|
| `chromium` | Headless Chromium (default) | Fast, isolated, testing |
| `chromium --headed` | Visible Chromium | Debugging |
| `real` | Real Chrome binary | Needs real browser |
| `real --profile` | Chrome with your logins | Authenticated sites |
| `remote` | Cloud browser | AI agents, heavy tasks |

## Documentation

See [SKILL.md](SKILL.md) for complete documentation.

## License

MIT
