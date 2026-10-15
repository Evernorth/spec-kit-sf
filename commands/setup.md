---
description: "Automated dependency checker and installer (sf, gh, code-analyzer)."
---

# Environment Setup

## User Input

$ARGUMENTS

## Instructions

Analyze the environment and install missing dependencies for SFSpeckit.

### Step 1: Detect Operating System

Identify whether the user is on **macOS**, **Windows**, or **Linux**.

### Step 2: Check Salesforce CLI (`sf`)

1. Run: `sf version`
2. If found: Report version.
3. If NOT found:
   - **macOS**: Suggest `brew install --cask salesforce-cli`
   - **Windows**: Suggest `winget install Salesforce.SalesforceCLI` or `npm install --global @salesforce/cli`
   - Ask for permission to run the install command.

### Step 3: Check GitHub CLI (`gh`)

1. Run: `gh --version`
2. If found: Report version.
3. If NOT found:
   - **macOS**: Suggest `brew install gh`
   - **Windows**: Suggest `winget install GitHub.cli`
   - Ask for permission to run the install command.

### Step 4: Check SF Code Analyzer (`@salesforce/plugin-code-analyzer`)

1. Run: `sf plugins inspect @salesforce/plugin-code-analyzer`
2. If found: Report version (Code Analyzer v5).
3. If NOT found or legacy `sfdx-scanner` is installed:
   - Inform the user: "Code Analyzer v4 (`sfdx-scanner`) was retired in August 2025. SFSpeckit requires modern Code Analyzer v5 (`@salesforce/plugin-code-analyzer`)."
   - Suggest: `sf plugins install @salesforce/plugin-code-analyzer`
   - Ask for permission to run the install command.

### Step 5: Verify Permissions & Login

1. Check if user is authenticated to any org: `sf org list`
2. If no orgs found:
   - Provide instruction: `sf org login web --alias dev`

### Step 6: Summary Report

Generate a status table:

| Tool | Status | Version | Action Taken |
|------|--------|---------|--------------|
| Salesforce CLI | ✅ / ❌ | X.X.X | [Installed/None] |
| GitHub CLI | ✅ / ❌ | X.X.X | [Installed/None] |
| Code Analyzer | ✅ / ❌ | X.X.X | [Updated/None] |

## Next Step

Environment is ready. Run `/speckit.sf.constitution` to initialize your project principles.

## Output

- **Status Table**: Final state of all dependencies.
- **Confirmation**: Final readiness check for SFSpeckit commands.
