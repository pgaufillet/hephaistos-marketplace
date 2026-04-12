# Hephaistos Marketplace

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) plugin marketplace.

## Available Plugins

### JARPA

**Journal, Architecture, Requirements, Plan, Actions** - Structured documentation methodology for AI-assisted software engineering.

- **Version**: 0.2.1
- **Category**: Productivity
- **Repository**: [pgaufillet/jarpa](https://github.com/pgaufillet/jarpa)

Automated session workflows, journal archiving, context monitoring, and documentation discipline for Claude Code projects.

## Setup

Add the Hephaistos marketplace to your Claude Code settings (`~/.claude/settings.json`):

```json
{
  "extraKnownMarketplaces": {
    "hephaistos": {
      "source": {
        "source": "git",
        "url": "https://github.com/pgaufillet/hephaistos-marketplace.git"
      }
    }
  }
}
```

Then install plugins:

```bash
claude plugin install jarpa@hephaistos
claude plugin enable --scope local jarpa@hephaistos
```

## Adding a Plugin

To add a plugin to this marketplace, add an entry to `.claude-plugin/marketplace.json`:

```json
{
  "name": "my-plugin",
  "description": "Plugin description",
  "version": "1.0.0",
  "author": {
    "name": "Author Name"
  },
  "source": {
    "source": "url",
    "url": "https://github.com/user/my-plugin.git"
  },
  "homepage": "https://github.com/user/my-plugin",
  "category": "development"
}
```

## License

MIT License - See [LICENSE](LICENSE) file for details.
