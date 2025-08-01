# Deploxy Documentation

**The serverless proxy platform for Stdio MCP servers**

Deploxy is a comprehensive deployment platform that allows you to deploy Stdio MCP (Model Context Protocol) servers to serverless infrastructure while keeping your source code private and secure. This repository contains the official documentation for the Deploxy platform.

## 🚀 What is Deploxy?

Deploxy solves the fundamental challenge of monetizing and securing MCP servers by providing:

- **Private Server Deployment**: Your MCP server code runs securely in our cloud environment, never exposed to end-users
- **Lightweight NPM Proxy**: Users install minimal proxy packages that securely connect to your hosted logic
- **Global Serverless Infrastructure**: Automatic scaling and distribution across all supported regions
- **Secure Environment Management**: Safe handling of API keys, database connections, and sensitive data
- **CLI-Driven Workflow**: Simple deployment process integrated into your development workflow

## 📚 Documentation Structure

This documentation is built with [Mintlify](https://mintlify.com) and organized into three main sections:

### Getting Started

- **Introduction** (`index.mdx`) - Platform overview and initial setup
- **Quick Start - Clone** (`getting-started/quickstart-clone.mdx`) - Deploy a sample server in 5 minutes
- **Quick Start - Existing** (`getting-started/quickstart-existing.mdx`) - Integrate existing projects
- **Core Concepts** (`getting-started/core-concepts.mdx`) - Understanding Deploxy architecture

### Guides

- **Configuration** (`guides/configuration.mdx`) - Detailed configuration options
- **Troubleshooting** (`guides/troubleshooting.mdx`) - Common issues and solutions
- **Monitoring** (`guides/monitoring.mdx`) - Monitoring your deployed servers

### Resources

- **CLI Reference** (`resources/cli-reference.mdx`) - Complete CLI command documentation
- **Pricing** (`resources/pricing.mdx`) - Pricing plans and MCP operation billing
- **Regions** (`resources/regions.mdx`) - Available deployment regions

## 🛠 Development

### Prerequisites

- Node.js 20 or higher
- Mintlify CLI

### Local Development

```bash
# Install Mintlify CLI globally
npm i -g mint

# Start development server (run from project root where docs.json is located)
mint dev

# Update CLI to latest version
mint update
```

The development server should be run from the directory containing `docs.json` (the current directory).

### Documentation Standards

This documentation follows strict technical writing guidelines defined in `doc-rule.mdc`:

- **User-centered approach** with clear, actionable procedures
- **Mintlify components** for enhanced presentation (Steps, CodeGroup, Warning, Check, etc.)
- **Consistent YAML frontmatter** structure with title, description, sequence, keywords, and icon
- **Complete and runnable** code examples
- **Progressive disclosure** of information

### File Structure

```
docs/
├── docs.json              # Mintlify configuration
├── doc-rule.mdc          # Writing standards and component guidelines
├── index.mdx             # Homepage/introduction
├── getting-started/      # Onboarding content
├── guides/               # In-depth operational guides
├── resources/            # Reference materials
├── images/               # Screenshots and diagrams
└── logo/                 # Brand assets
```

## 🔗 Related Links

- **Deploxy Platform**: https://www.deploxy.com
- **Dashboard**: https://www.deploxy.com/dashboard
- **GitHub**: https://github.com/deploxy
- **Quick Start Repository**: https://github.com/deploxy/quick-start
