# Global Gitignore

A centralized gitignore configuration repository containing common ignore patterns for development environments.

## Installation

### 1. Create symbolic link to ~/.gitignore

```bash
# Navigate to this repository
cd /path/to/global-gitignore

# Create symbolic link (replace /path/to/global-gitignore with actual path)
ln -sf "$(pwd)/.gitignore" ~/.gitignore
```

### 2. Configure Git to use global ignore file

```bash
# Set global gitignore path in Git config
git config --global core.excludesfile ~/.gitignore

# Verify the configuration
git config --global --get core.excludesfile
```

## Usage

Once configured, Git will automatically apply these ignore patterns to all repositories on your system. The patterns include:

- Environment files (`.env`, `.envrc`)
- Terraform files (`.terraform/`, `*.auto.tfvars`, `*.tfoverride`)
- Terraform CLI configuration (`.terraformrc`, `terraform.rc`)
- Lock files (`.~lock.*#`)

## Maintenance

To update the global ignore patterns, simply edit the `.gitignore` file in this repository. Changes will be immediately reflected across all Git repositories.

## Repository Structure

- `.gitignore` - Main configuration file with ignore patterns
- `AGENTS.md` - Guidelines for coding agents working in this repository