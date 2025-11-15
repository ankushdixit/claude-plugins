# Claude Code Plugins Marketplace

Official marketplace for Claude Code plugins by Ankush Dixit.

> **📦 Distribution Repository** - This is a marketplace for installing plugins. For Solokit plugin development, issues, and contributions, visit the main repository: **[github.com/ankushdixit/solokit](https://github.com/ankushdixit/solokit)**

## Available Plugins

### 📦 Solokit

**Structured Solo Development with AI and Quality Automation** - Build production software alone with team-level sophistication.

- **Plugin Name**: `solokit`
- **Version**: 0.1.3
- **Status**: Production-ready ✅
- **License**: MIT

**Key Features:**
- ✅ **4 Production Stacks** - T3 Stack, FastAPI, Refine, Next.js with 4 quality tiers each
- ✅ **Session Management** - AI-powered briefings with perfect context continuity
- ✅ **Work Item Tracking** - Dependency graphs, critical path analysis, spec-first architecture
- ✅ **Learning System** - AI-powered knowledge capture and curation (6 categories)
- ✅ **Quality Gates** - Automated tests, linting, security scans, documentation checks
- ✅ **Integration Testing** - API contract validation, environment checks, performance benchmarks
- ✅ **Git Workflow** - Automated commits, standardized messages, PR creation

**Commands:** 15 slash commands (`/sk:*`) for complete solo development workflow

**Documentation & Source:**
- [View Full Documentation →](https://github.com/ankushdixit/solokit#readme)
- [Standalone Repository](https://github.com/ankushdixit/solokit) (for direct clone installation)
- [Marketplace Repository](https://github.com/ankushdixit/claude-plugins) (this repo)

---

## Installation

### Quick Start

#### 1. Add This Marketplace

In Claude Code, run:
```
/plugin
```

Select **"Add marketplace"** and enter:
```
ankushdixit/claude-plugins
```

#### 2. Install the Solokit Plugin

1. Select **"Browse and install plugins"**
2. Choose `solokit`
3. Click **Install**
4. Restart Claude Code

#### 3. One-Time Setup (Required)

After installing the plugin, run this command once:

```bash
pip install -e ~/.claude/plugins/marketplaces/claude-plugins/solokit
```

This installs the `sk` command globally, enabling all slash commands to work.

#### 4. Verify Installation

```bash
# Check sk command is available
which sk

# Test the command
sk status
```

Type `/` in Claude Code to see available commands. Try:
```
/sk:init
```

You should see the Solokit initialization command ready to use.

---

## Installation Methods Comparison

Solokit can be installed in two different ways, depending on your preference:

### Method 1: Via Marketplace (Recommended)

**Install from:** `ankushdixit/claude-plugins` marketplace

**Commands use the `sk:` prefix:** `/sk:init`, `/sk:work-new`, `/sk:start`

**Best for:**
- Using Solokit across multiple projects
- Easy updates through the marketplace
- Keeping commands organized with prefixes
- Installing multiple plugins without command conflicts

**Installation:**
```bash
# 1. Add marketplace in Claude Code
/plugin marketplace add ankushdixit/claude-plugins

# 2. Install the solokit plugin (via UI)

# 3. One-time setup (enables commands)
pip install -e ~/.claude/plugins/marketplaces/claude-plugins/solokit
```

**Note:** The pip install step is required to enable the `sk` CLI command that powers all slash commands.

---

### Method 2: Direct Clone (Alternative)

**Install from:** `https://github.com/ankushdixit/solokit` repository

**Commands use NO prefix:** `/init`, `/work-new`, `/start`

**Best for:**
- Project-specific installation
- Customizing commands locally
- Using Solokit in a single project
- Wanting shorter command names

**Installation:**
```bash
# Clone into your project's .claude directory
cd /path/to/your/project
git clone https://github.com/ankushdixit/solokit .claude
```

**Note:** With direct clone, commands are available immediately without the `sk:` prefix. For example, use `/init` instead of `/sk:init`.

---

## Using the Solokit Plugin

**Note:** The examples below use the marketplace installation commands (with `sk:` prefix). If you installed via direct clone, omit the `sk:` prefix (e.g., use `/init` instead of `/sk:init`).

### Quick Start Workflow

1. **Initialize your project with a production stack:**
   ```
   /sk:init
   ```
   Choose from: T3 Stack, FastAPI, Refine, or Next.js with 4 quality tiers

2. **Create a work item:**
   ```
   /sk:work-new
   ```

3. **Start a session:**
   ```
   /sk:start
   ```

4. **Develop with Claude** and capture learnings:
   ```
   /sk:learn
   ```

5. **End the session** (runs quality gates):
   ```
   /sk:end
   ```

### Available Commands

**Session Management:**
- `/sk:init` - Initialize project with production templates
- `/sk:start` - Begin work session with comprehensive briefing
- `/sk:end` - Complete session with quality gates
- `/sk:validate` - Pre-flight check before completion
- `/sk:status` - Quick session overview

**Work Item Management:**
- `/sk:work-new` - Create new work item with dependencies
- `/sk:work-list` - List work items with filters
- `/sk:work-show` - Show work item details
- `/sk:work-update` - Update work item fields
- `/sk:work-next` - Get next recommended work item
- `/sk:work-delete` - Delete work item
- `/sk:work-graph` - Visualize dependencies with critical path

**Learning Management:**
- `/sk:learn` - Capture insight during development
- `/sk:learn-show` - Browse learnings with filters
- `/sk:learn-search` - Full-text search across learnings
- `/sk:learn-curate` - Run AI-powered curation

---

## What Makes Solokit Different?

### The Problem It Solves

Traditional AI coding sessions suffer from:
- **Context loss** between sessions - AI forgets what was done previously
- **Quality entropy** over time - Standards slip without enforcement
- **Knowledge fragmentation** - Learnings get lost across interactions
- **Lack of starting templates** - Every project starts from scratch

### The Solokit Solution

Solokit provides:
- **Production-ready foundations** with 4 battle-tested stacks × 4 quality tiers
- **Perfect context continuity** through automated briefings that load full project state
- **Quality enforcement** via automated validation gates (tests, linting, security scans)
- **Knowledge accumulation** through learnings system with AI-powered categorization
- **Dependency-driven workflow** with logical ordering based on dependencies
- **Living documentation** that stays current automatically with git integration

---

## Production Templates

Solokit includes 4 production-ready stacks, each with 4 quality tiers:

**Stacks:**
- **T3 Stack** - tRPC + Next.js + Prisma + Tailwind (Full-stack TypeScript SaaS)
- **FastAPI** - Python ML/AI API with async support
- **Refine** - React admin dashboard with Ant Design
- **Next.js** - Full-stack React framework

**Quality Tiers:**
- **Essential** - Basic linting, formatting, unit tests
- **Standard** - + Pre-commit hooks, security scanning
- **Comprehensive** - + E2E tests, mutation testing, type coverage
- **Production** - + Monitoring, load testing, performance tracking

---

## Plugin Development Status

**Current Version:** 0.1.3 (Initial Public Release)

### Core Features Complete

| Feature | Status |
|---------|--------|
| Production Templates (4 stacks × 4 tiers) | ✅ Complete |
| Session Management | ✅ Complete |
| Work Item System | ✅ Complete |
| Dependency Visualization | ✅ Complete |
| Learning Management | ✅ Complete |
| Quality Gates | ✅ Complete |
| Integration Testing | ✅ Complete |
| Git Workflow Automation | ✅ Complete |

**Test Coverage:** 2,954/2,954 tests passing (100%)

---

## Requirements

### Core Requirements

- **Claude Code**: Desktop application (required)
- **Python 3.9+**: Core scripts are written in Python
- **Git**: Required for version control integration

### Optional Tools (for quality gates)

**Python Projects:**
- `pytest` (testing)
- `ruff` (linting/formatting)
- `bandit`, `safety` (security scanning)

**JavaScript/TypeScript Projects:**
- `eslint`, `prettier` (linting/formatting)
- `npm audit` (security)

**Visualization:**
- `graphviz` (for SVG dependency graph generation)

Quality gates gracefully skip when tools aren't available, so you only need to install what you use.

---

## Contributing

### For Solokit Plugin Contributions

**This repository is for marketplace distribution only.** For Solokit plugin development:

- 🐛 **Report bugs**: https://github.com/ankushdixit/solokit/issues
- 💡 **Request features**: https://github.com/ankushdixit/solokit/issues
- 🔧 **Submit PRs**: https://github.com/ankushdixit/solokit/pulls
- 📖 **View docs**: https://github.com/ankushdixit/solokit#readme

See [CONTRIBUTING.md](CONTRIBUTING.md) for details.

### Submitting Other Plugins

To submit a different plugin to this marketplace, please open an issue with:
- Plugin name and description
- GitHub repository URL
- Brief overview of features
- Documentation link

[Open a Plugin Submission Issue →](https://github.com/ankushdixit/claude-plugins/issues/new?title=Plugin%20Submission:%20[Your%20Plugin%20Name])

---

## Repository Sync & Maintenance

### Automated Sync from Main Solokit Repo

**This repository is automatically synced** from the main Solokit repository at [github.com/ankushdixit/solokit](https://github.com/ankushdixit/solokit).

#### How It Works

1. **Automatic Sync**: Every push to the `main` branch of the Solokit repository triggers a GitHub Actions workflow
2. **File Sync**: The following files/directories are automatically synced:
   - `src/solokit/` → `solokit/src/solokit/` (complete package structure)
   - `.claude/commands/` → `solokit/commands/`
   - `pyproject.toml` → `solokit/pyproject.toml`
3. **Version Sync**: Version is automatically extracted from `pyproject.toml` and updated in `solokit/.claude-plugin/plugin.json`
4. **Preserved Files**: The following files are maintained separately in this repo and NOT synced:
   - `README.md` (this marketplace README)
   - `CONTRIBUTING.md` (directs to main Solokit repo)
   - `LICENSE`, `SECURITY.md` (static policy files)

#### Why This Approach?

- ✅ **Single Source of Truth**: All development happens in the main Solokit repo
- ✅ **Zero Manual Maintenance**: No need to manually copy files or update versions
- ✅ **Always Up-to-Date**: Plugin marketplace stays in sync with latest changes
- ✅ **Preserved Marketplace Context**: Marketplace-specific files remain unchanged

#### For Maintainers

The sync is handled by:
- **Workflow**: `.github/workflows/sync-plugin.yml` (in main Solokit repo)
- **Script**: `src/solokit/project/sync_plugin.py` (in main Solokit repo)
- **Secret**: `PLUGIN_REPO_TOKEN` (GitHub PAT with repo access)

Manual sync can be triggered via GitHub Actions workflow dispatch in the main Solokit repository.

---

## Support

### For Solokit Plugin Issues

Report issues and view documentation at the standalone Solokit repository:
- [Report Solokit Issues](https://github.com/ankushdixit/solokit/issues)
- [View Solokit Documentation](https://github.com/ankushdixit/solokit#readme)
- [Solokit Discussions](https://github.com/ankushdixit/solokit/discussions)

### For Marketplace Issues

For issues specific to the marketplace or plugin installation:
- [Report Marketplace Issues](https://github.com/ankushdixit/claude-plugins/issues)

---

## Technology Stack

**Solokit Plugin:**
- **Language:** Python 3.9+
- **Plugin System:** Claude Code native extensions
- **Visualization:** Graphviz (dependency graphs)
- **Testing:** pytest (quality gates)
- **Linting:** ruff (code quality)

---

## License

Each plugin has its own license. See individual plugin directories for details.

- **Solokit Plugin**: MIT License

---

## Resources

- [Claude Code Documentation](https://docs.claude.com/en/docs/claude-code)
- [Plugin Development Guide](https://docs.claude.com/en/docs/claude-code/plugins)
- [Marketplace Documentation](https://docs.claude.com/en/docs/claude-code/plugin-marketplaces)

---

**Ready for use!** Install the Solokit plugin and start building with team-level sophistication.
