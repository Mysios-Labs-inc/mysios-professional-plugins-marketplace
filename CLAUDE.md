# Mysios Labs Claude Plugins Marketplace

Professional Claude Code plugin marketplace for AI-powered productivity and career acceleration tools.

## Repository Purpose

This repository serves as a **plugin marketplace catalog** that references external plugin repositories. It follows the modern external plugin architecture pattern recommended for third-party marketplaces.

## Repository Structure

```
claude-plugins-marketplace/
├── marketplace.json          # Marketplace catalog and metadata
├── README.md                # User-facing documentation
├── LICENSE                  # MIT license terms
├── CLAUDE.md               # This file - Claude-specific documentation
└── .gitignore              # Development file exclusions
```

## Marketplace Configuration

### Core Files

- **`marketplace.json`**: The marketplace manifest that defines available plugins and their sources
- **`README.md`**: Public documentation for users discovering the marketplace
- **`LICENSE`**: MIT license governing the marketplace and its contents

### Key Features

- **External plugin architecture**: References plugins hosted in separate repositories
- **Version pinning**: Uses `ref` pinning for stable plugin delivery
- **Comprehensive metadata**: Includes keywords, licensing, and author information
- **Modern source format**: Uses recommended GitHub source configuration

## Plugin Architecture

### External Plugin Model

This marketplace uses an **external plugin model** where:

1. **Marketplace repository** (this repo) contains only the catalog
2. **Plugin repositories** are maintained separately with their own versioning
3. **Users install** the marketplace first, then individual plugins

### Plugin Sources

```json
{
  "source": {
    "source": "github",
    "repo": "Mysios-Labs-inc/claude-jobseeking-plugin",
    "ref": "main"
  }
}
```

Benefits:
- ✅ **Clean separation** of marketplace and plugin development
- ✅ **Independent versioning** for each plugin
- ✅ **Scalable architecture** supporting unlimited external plugins
- ✅ **Clear ownership** with plugin-specific maintenance

## Development Workflow

### Adding New Plugins

1. **Create plugin repository** with proper `.claude-plugin/plugin.json` manifest
2. **Update marketplace.json** to include new plugin entry
3. **Test installation** locally before publishing
4. **Commit and push** changes to trigger marketplace update

### Version Management

- **Marketplace version**: Tracked in `metadata.version`
- **Plugin versions**: Specified in individual plugin entries
- **Source pinning**: Uses `ref` for stable delivery

### Quality Standards

- **JSON validation**: All configuration files must be valid JSON
- **Schema compliance**: Follow Claude Code marketplace schema
- **Professional metadata**: Include descriptions, keywords, licensing
- **Documentation**: Maintain clear README and installation instructions

## Installation Commands

### For Users

```bash
# Add the marketplace
/plugin marketplace add Mysios-Labs-inc/claude-plugins-marketplace

# Install available plugins
/plugin install jobseeking-plugin@mysios-labs
```

### For Developers

```bash
# Local development testing
/plugin marketplace add ./path/to/local/marketplace
/plugin validate .
```

## Maintenance Guidelines

### Regular Tasks

1. **Monitor plugin availability** - ensure external repositories remain accessible
2. **Update version references** - coordinate with plugin maintainers for releases
3. **Review metadata accuracy** - keep descriptions and keywords current
4. **Test installation flow** - verify marketplace and plugin installation works

### Quality Assurance

- Run `/plugin validate .` before committing changes
- Test plugin installation in clean environment
- Verify all external plugin repositories are accessible
- Maintain consistent metadata across all plugin entries

## Contributing

This marketplace welcomes community plugin contributions. To add your plugin:

1. Ensure your plugin follows Claude Code plugin standards
2. Host your plugin in a public GitHub repository
3. Submit a pull request adding your plugin to `marketplace.json`
4. Include comprehensive metadata and testing information

## Support

- **Marketplace issues**: Report via GitHub Issues on this repository
- **Plugin-specific issues**: Contact individual plugin maintainers
- **General support**: hello@mysioslabs.com

---

*This marketplace demonstrates modern Claude Code plugin distribution patterns and serves as a reference implementation for external plugin marketplaces.*