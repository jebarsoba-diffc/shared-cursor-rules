# Shared Cursor Rules

A centralized repository of Cursor IDE rules for consistent development workflows across projects.

## What are Cursor Rules?

Cursor rules are instructions that guide the AI assistant in Cursor IDE, helping ensure consistent coding standards, commit conventions, and project setup instructions across your team.

## Installation

### Using Cursor Workbench Extension

1. Install the [Cursor Workbench](https://marketplace.visualstudio.com/items?itemName=cursor-workbench) extension
2. Add this repository as a remote registry in the extension settings
3. Import rules into your projects as needed

### Manual Installation

Copy the rules you need from this repository to your project's `.cursor/rules/` directory:

```bash
cp rules/application-setup.mdc /path/to/your/project/.cursor/rules/
```

## Available Rules

- **`application-setup.mdc`** - Instructions for running, testing, and building applications
- **`conventional-commits.mdc`** - Commit message conventions and standards

## Contributing

1. Add new rule files to the `rules/` directory
2. Follow the `.mdc` format with proper frontmatter
3. Submit a pull request with a clear description