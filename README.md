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
ln -s ~/dev/shared-cursor-rules/.cursor/rules/application_setup.mdc .cursor/rules/application_setup.mdc
ln -s ~/dev/shared-cursor-rules/.cursor/rules/conventional_commits.mdc .cursor/rules/conventional_commits.mdc
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
cp .cursor/rules/application_setup.mdc /path/to/your/project/.cursor/rules/
```

## Available Rules

### General Rules

- **`application_setup.mdc`** - Instructions for running, testing, and building applications
- **`conventional_commits.mdc`** - Commit message conventions and standards
- **`test_coverage.mdc`** - Test coverage requirements and conventions for actions, operations, and infrastructure (applies to both Python and TypeScript)

### Python Rules

- **`python/api_core_actions.mdc`** - Standards and patterns for Python API Actions in `core/actions` directory structure
- **`python/api_core_domain.mdc`** - Standards and patterns for Python API Domain layer in `core/domain` directory structure
- **`python/api_core_infrastructure.mdc`** - Standards and patterns for Python API Infrastructure layer in `core/infrastructure` directory structure
- **`python/api_http_operations.mdc`** - Standards and patterns for Python Web Operations (Controllers/Routers) in `web/operations` directory structure
- **`python/api_http_server.mdc`** - Standards and patterns for Python HTTP Server (Application Setup) in `web/server` directory structure
- **`python/pyproject_toml_fixed_dependencies.mdc`** - Rules for managing fixed dependencies in `pyproject.toml` files
- **`python/python.mdc`** - General Python code review criteria and standards

## Contributing

1. Add new rule files to the `.cursor/rules/` directory
2. Follow the `.mdc` format with proper frontmatter
3. Submit a pull request with a clear description