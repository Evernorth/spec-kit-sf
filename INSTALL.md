# Installation Guide — SFSpeckit

SFSpeckit can be installed into any Salesforce DX project using the GitHub Spec-Kit CLI.

## Quick Install (Spec-Kit CLI)

Run the following command in your Salesforce DX project root:

```bash
specify extension add sf --from https://github.com/evernorth/spec-kit-sf
```

For specific tagged versions:

```bash
specify extension add sf --from https://github.com/evernorth/spec-kit-sf/archive/refs/tags/v1.0.0.zip
```

## Automated Environment Verification

Once installed, execute the automated environment setup command:

```bash
/speckit.sf.setup
```

This command inspects your local environment for required tools:
1. **Salesforce CLI (`sf`)**: Minimum version 2.0.0
2. **GitHub CLI (`gh`)**: Minimum version 2.0.0
3. **Salesforce Code Analyzer (`@salesforce/plugin-code-analyzer`)**: Version 5.x with PMD 7 and DFA