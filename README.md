# Claude Code Plugins Marketplace

Official marketplace for Claude Code plugins by Ankush Dixit.

> **📦 Distribution Repository** - This is a marketplace for installing plugins. For SDD plugin development, issues, and contributions, visit the main repository: **[github.com/ankushdixit/sdd](https://github.com/ankushdixit/sdd)**

## Available Plugins

### 📦 SDD (Session-Driven Development)

**Session-Driven Development for Claude Code** - Maintain perfect context across multiple AI coding sessions.

- **Plugin Name**: `sdd`
- **Version**: 0.6.0
- **Status**: Production-ready ✅
- **License**: MIT

**Key Features:**
- ✅ **Session Management** - Comprehensive briefings with perfect context continuity
- ✅ **Work Item Tracking** - Dependency graphs, critical path analysis, bottleneck detection
- ✅ **Learning System** - AI-powered knowledge capture and curation (6 categories)
- ✅ **Quality Gates** - Automated tests, linting, security scans, documentation checks
- ✅ **Integration Testing** - API contract validation, environment checks, performance benchmarks
- ✅ **Deployment Support** - Multi-environment deployment with validation
- ✅ **Git Workflow** - Automated commits, standardized messages, push automation

**Commands:** 15 slash commands for complete session-driven development workflow

**Documentation & Source:**
- [View Full Documentation →](https://github.com/ankushdixit/sdd#readme)
- [Standalone Repository](https://github.com/ankushdixit/sdd) (for direct clone installation)
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

#### 2. Install the SDD Plugin

1. Select **"Browse and install plugins"**
2. Choose `sdd`
3. Click **Install**
4. Restart Claude Code

#### 3. One-Time Setup (Required for v0.6.0+)

After installing the plugin, run this command once:

```bash
pip install -e ~/.claude/plugins/marketplaces/claude-plugins/sdd
```

This installs the `sdd` command globally, enabling all slash commands to work.

#### 4. Verify Installation

```bash
# Check sdd command is available
which sdd

# Test the command
sdd status
```

Type `/` in Claude Code to see available commands. Try:
```
/sdd:init
```

You should see the SDD initialization command ready to use.

---

## Installation Methods Comparison

SDD can be installed in two different ways, depending on your preference:

### Method 1: Via Marketplace (Recommended)

**Install from:** `ankushdixit/claude-plugins` marketplace

**Commands use the `sdd:` prefix:** `/sdd:init`, `/sdd:work-new`, `/sdd:start`

**Best for:**
- Using SDD across multiple projects
- Easy updates through the marketplace
- Keeping commands organized with prefixes
- Installing multiple plugins without command conflicts

**Installation:**
```bash
# 1. Add marketplace in Claude Code
/plugin marketplace add ankushdixit/claude-plugins

# 2. Install the sdd plugin (via UI)

# 3. One-time setup (enables commands)
pip install -e ~/.claude/plugins/marketplaces/claude-plugins/sdd
```

**Note:** The pip install step is required for v0.6.0+ to enable the `sdd` CLI command that powers all slash commands.

---

### Method 2: Direct Clone (Alternative)

**Install from:** `https://github.com/ankushdixit/sdd` repository

**Commands use NO prefix:** `/init`, `/work-new`, `/start`

**Best for:**
- Project-specific installation
- Customizing commands locally
- Using SDD in a single project
- Wanting shorter command names

**Installation:**
```bash
# Clone into your project's .claude directory
cd /path/to/your/project
git clone https://github.com/ankushdixit/sdd .claude
```

**Note:** With direct clone, commands are available immediately without the `sdd:` prefix. For example, use `/init` instead of `/sdd:init`.

---

## Using the SDD Plugin

**Note:** The examples below use the marketplace installation commands (with `sdd:` prefix). If you installed via direct clone, omit the `sdd:` prefix (e.g., use `/init` instead of `/sdd:init`).

### Quick Start Workflow

1. **Initialize your project:**
   ```
   /sdd:init
   ```

2. **Create a work item:**
   ```
   /sdd:work-new
   ```

3. **Start a session:**
   ```
   /sdd:start
   ```

4. **Develop with Claude** and capture learnings:
   ```
   /sdd:learn
   ```

5. **End the session** (runs quality gates):
   ```
   /sdd:end
   ```

### Available Commands

**Session Management:**
- `/sdd:init` - Initialize project structure
- `/sdd:start` - Begin work session with comprehensive briefing
- `/sdd:end` - Complete session with quality gates
- `/sdd:validate` - Pre-flight check before completion
- `/sdd:status` - Quick session overview

**Work Item Management:**
- `/sdd:work-new` - Create new work item with dependencies
- `/sdd:work-list` - List work items with filters
- `/sdd:work-show` - Show work item details
- `/sdd:work-update` - Update work item fields
- `/sdd:work-next` - Get next recommended work item
- `/sdd:work-graph` - Visualize dependencies with critical path

**Learning Management:**
- `/sdd:learn` - Capture insight during development
- `/sdd:learn-show` - Browse learnings with filters
- `/sdd:learn-search` - Full-text search across learnings
- `/sdd:learn-curate` - Run AI-powered curation

---

## What Makes SDD Different?

### The Problem It Solves

Traditional AI coding sessions suffer from:
- **Context loss** between sessions - AI forgets what was done previously
- **Quality entropy** over time - Standards slip without enforcement
- **Knowledge fragmentation** - Learnings get lost across interactions
- **Lack of process rigor** - No systematic workflow for complex projects

### The SDD Solution

Session-Driven Development provides:
- **Perfect context continuity** through automated briefings that load full project state
- **Quality enforcement** via automated validation gates (tests, linting, security scans)
- **Knowledge accumulation** through learnings system with AI-powered categorization
- **Dependency-driven workflow** with logical ordering based on dependencies
- **Living documentation** that stays current automatically with git integration

---

## Plugin Development Status

**Current Version:** 0.6.0 (Production-ready)

### Completed Phases

| Phase | Version | Description | Status |
|-------|---------|-------------|--------|
| Phase 0 | v0.0 | Foundation & Documentation | ✅ Complete |
| Phase 1 | v0.1 | Core Plugin Foundation | ✅ Complete |
| Phase 2 | v0.2 | Work Item System | ✅ Complete |
| Phase 3 | v0.3 | Dependency Visualization | ✅ Complete |
| Phase 4 | v0.4 | Learning Management | ✅ Complete |
| Phase 5 | v0.5 | Quality Gates | ✅ Complete |
| Phase 5.5 | v0.5.5 | Integration Testing | ✅ Complete |
| Phase 5.6 | v0.5.6 | Deployment Support | ✅ Complete |
| Phase 5.7 | v0.5.7 | Spec-First Architecture | ✅ Complete |
| Phase 5.8 | v0.5.8 | Marketplace Plugin Support | ✅ Complete |
| Phase 5.9 | v0.6.0 | Standard Python src/ Layout | ✅ Complete |

**Test Coverage:** 1416/1416 tests passing (100%)

### Upcoming Features

- **Phase 6** (v0.6): Spec-Kit Integration - Import work items from specifications
- **Phase 7** (v0.7+): Advanced Features - Templates, metrics, AI enhancements

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

### For SDD Plugin Contributions

**This repository is for marketplace distribution only.** For SDD plugin development:

- 🐛 **Report bugs**: https://github.com/ankushdixit/sdd/issues
- 💡 **Request features**: https://github.com/ankushdixit/sdd/issues
- 🔧 **Submit PRs**: https://github.com/ankushdixit/sdd/pulls
- 📖 **View docs**: https://github.com/ankushdixit/sdd#readme

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

### Automated Sync from Main SDD Repo

**This repository is automatically synced** from the main SDD repository at [github.com/ankushdixit/sdd](https://github.com/ankushdixit/sdd).

#### How It Works

1. **Automatic Sync**: Every push to the `main` branch of the SDD repository triggers a GitHub Actions workflow
2. **File Sync**: The following files/directories are automatically synced:
   - `src/sdd/` → `sdd/src/sdd/` (complete package structure)
   - `.claude/commands/` → `sdd/commands/`
   - `pyproject.toml` → `sdd/pyproject.toml`
3. **Version Sync**: Version is automatically extracted from `pyproject.toml` and updated in `sdd/.claude-plugin/plugin.json`
4. **Preserved Files**: The following files are maintained separately in this repo and NOT synced:
   - `README.md` (this marketplace README)
   - `CONTRIBUTING.md` (directs to main SDD repo)
   - `LICENSE`, `SECURITY.md` (static policy files)

#### Why This Approach?

- ✅ **Single Source of Truth**: All development happens in the main SDD repo
- ✅ **Zero Manual Maintenance**: No need to manually copy files or update versions
- ✅ **Always Up-to-Date**: Plugin marketplace stays in sync with latest changes
- ✅ **Preserved Marketplace Context**: Marketplace-specific files remain unchanged

#### For Maintainers

The sync is handled by:
- **Workflow**: `.github/workflows/sync-plugin.yml` (in main SDD repo)
- **Script**: `src/sdd/project/sync_plugin.py` (in main SDD repo)
- **Secret**: `PLUGIN_REPO_TOKEN` (GitHub PAT with repo access)

Manual sync can be triggered via GitHub Actions workflow dispatch in the main SDD repository.

---

## Support

### For SDD Plugin Issues

Report issues and view documentation at the standalone SDD repository:
- [Report SDD Issues](https://github.com/ankushdixit/sdd/issues)
- [View SDD Documentation](https://github.com/ankushdixit/sdd#readme)
- [SDD Discussions](https://github.com/ankushdixit/sdd/discussions)

### For Marketplace Issues

For issues specific to the marketplace or plugin installation:
- [Report Marketplace Issues](https://github.com/ankushdixit/claude-plugins/issues)

---

## Technology Stack

**SDD Plugin:**
- **Language:** Python 3.9+
- **Plugin System:** Claude Code native extensions
- **Visualization:** Graphviz (dependency graphs)
- **Testing:** pytest (quality gates)
- **Linting:** ruff (code quality)

---

## License

Each plugin has its own license. See individual plugin directories for details.

- **SDD Plugin**: MIT License

---

## Resources

- [Claude Code Documentation](https://docs.claude.com/en/docs/claude-code)
- [Plugin Development Guide](https://docs.claude.com/en/docs/claude-code/plugins)
- [Marketplace Documentation](https://docs.claude.com/en/docs/claude-code/plugin-marketplaces)

---

**Ready for use!** Install the SDD plugin and start building with perfect context continuity.
