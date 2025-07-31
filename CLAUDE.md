# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Commands

### Mintlify Documentation
This is a Mintlify documentation site for Deploxy, a serverless proxy platform for Stdio MCP servers.

```bash
# Install Mintlify CLI globally
npm i -g mint

# Start development server (run from project root where docs.json is located)
mint dev

# Update CLI to latest version
mint update
```

The development server should be run from the directory containing `docs.json` (the current directory).

### Git Status Notes
- Several `.mdx` files were deleted and replaced with `.mdx.md` files
- New `.md` files exist in getting-started/ and resources/ directories
- Changes appear to be a file format migration from `.mdx` to `.mdx.md`

## Project Architecture

### Documentation Structure
This is a Mintlify-based documentation site with the following organization:

**Core Configuration:**
- `docs.json` - Main Mintlify configuration with site metadata, navigation, theming
- `doc-rule.mdc` - Comprehensive Mintlify writing standards and component usage guidelines

**Content Organization:**
- `getting-started/` - Onboarding content (quickstart guides, core concepts)
- `guides/` - In-depth configuration and operational guides  
- `resources/` - Reference materials (CLI, pricing, regions)
- `images/` & `logo/` - Visual assets and branding
- `index.mdx.md` - Homepage/introduction

**Content Format:**
- Uses `.mdx.md` extension for most content files
- Standard `.mdx` for some guides
- YAML frontmatter with title, description, sequence, keywords, icon
- Mintlify-specific components (Steps, CodeGroup, Warning, Check, etc.)

### Documentation Domain: Deploxy Platform
Deploxy is a serverless deployment platform that:
- Deploys Stdio MCP servers to AWS Lambda
- Keeps source code private while publishing lightweight proxy packages to NPM
- Provides global distribution and automatic scaling
- Manages secure environment variables and authentication

**Key Concepts:**
- **Private MCP Server**: User's actual business logic runs securely in Deploxy cloud
- **Proxy Package**: Lightweight NPM package that forwards requests to private server
- **`.deploxy.json`**: Configuration file for deployment settings, auth tokens, environment variables
- **CLI Workflow**: `@deploxy/cli init` and `@deploxy/cli deploy` commands

### Writing Standards
The project follows strict technical writing guidelines defined in `doc-rule.mdc`:
- User-centered approach with clear procedures
- Mintlify components for enhanced presentation
- Consistent YAML frontmatter structure
- Code examples must be complete and runnable
- Progressive disclosure of information

### Navigation Structure
Defined in `docs.json` with three main groups:
1. **Getting Started** - Introduction, quickstarts, core concepts
2. **Guides** - Configuration, troubleshooting, monitoring  
3. **Resources** - CLI reference, pricing, regions

When working with this documentation:
- Follow the comprehensive writing standards in `doc-rule.mdc`
- Use appropriate Mintlify components for different content types
- Maintain the established YAML frontmatter structure
- Ensure all code examples are tested and complete
- Keep content focused on user goals and outcomes