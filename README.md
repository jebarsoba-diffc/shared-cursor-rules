# Shared Cursor Rules

A centralized repository of Cursor IDE rules for consistent development workflows across projects.

## What are Cursor Rules?

Cursor rules are instructions that guide the AI assistant in Cursor IDE, helping ensure consistent coding standards, commit conventions, and project setup instructions across your team.

## Installation

### Using Symbolic Links (Recommended)

Create symbolic links to the rules in this repository so they stay in sync across all your projects:

1. Clone this repository to a central location (e.g., `~/dev/shared-cursor-rules`)

2. In your project, ensure the `.cursor/rules/` directory exists:
```bash
mkdir -p /path/to/your/project/.cursor/rules
```

3. Create symbolic links for each rule you want to use:
```bash
# From your project's root directory
ln -s ~/dev/shared-cursor-rules/.cursor/rules/application-setup.mdc .cursor/rules/application-setup.mdc
ln -s ~/dev/shared-cursor-rules/.cursor/rules/conventional-commits.mdc .cursor/rules/conventional-commits.mdc
```

Or create a single symlink for all rules:
```bash
# From your project's root directory
ln -s ~/dev/shared-cursor-rules/.cursor/rules .cursor/rules/shared
```

**Note:** Replace `~/dev/shared-cursor-rules` with the actual path to your cloned repository.

### Manual Installation

Copy the rules you need from this repository to your project's `.cursor/rules/` directory:

```bash
cp .cursor/rules/application-setup.mdc /path/to/your/project/.cursor/rules/
```

## Available Rules

### General Rules

- **`application-setup.mdc`** - Instructions for running, testing, and building applications
- **`conventional-commits.mdc`** - Commit message conventions and standards

### Python Rules

- **`python/api-core-actions.mdc`** - Standards and patterns for Python API Actions in `core/actions` directory structure

## Contributing

1. Add new rule files to the `.cursor/rules/` directory
2. Follow the `.mdc` format with proper frontmatter
3. Submit a pull request with a clear description