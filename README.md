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

This documentation is organized into three main sections:

### Getting Started

- **Introduction** - Platform overview and initial setup
- **Quick Start - Clone** - Deploy a sample server in 5 minutes
- **Quick Start - Existing** - Integrate existing projects
- **Core Concepts** - Understanding Deploxy architecture

### Guides

- **Configuration** - Detailed configuration options
- **Troubleshooting** - Common issues and solutions
- **Monitoring** - Monitoring your deployed servers

### Resources

- **CLI Reference** - Complete CLI command documentation
- **Pricing** - Pricing plans and MCP operation billing
- **Regions** - Available deployment regions

## 🛠 Development

### Prerequisites

- Node.js 20 or higher
- Deploxy CLI

### Getting Started with Deploxy

```bash
# Install Deploxy CLI globally
npm install -g @deploxy/cli

# Initialize a new project
deploxy init

# Deploy to serverless infrastructure
deploxy deploy
```

### Configuration

Deploxy uses a `.deploxy.json` file for configuration. This file contains deployment settings, authentication tokens, and environment variables for your MCP server.

### Documentation Standards

This documentation follows strict technical writing guidelines:

- **User-centered approach** with clear, actionable procedures
- **Consistent structure** with title, description, and navigation elements
- **Complete and runnable** code examples
- **Progressive disclosure** of information

### File Structure

```
docs/
├── docs.json              # Site configuration
├── doc-rule.mdc          # Writing standards and guidelines
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
