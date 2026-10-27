# Changelog

All notable changes to this project will be documented in this file.
We follow the [Semantic Versioning 2.0.0](http://semver.org/) format.

## [1.0.0] - 2026-04-13

### Added
- **Extension Identity**: Formally registered as `sf` extension for Spec-Kit.
- **Hybrid AI Architecture**: Implemented a "Self-Contained but Aware" model. The extension works with zero dependencies but can leverage existing Salesforce agent skills as optional accelerators.
- **Unified Scoring Rubric**: Created `docs/scoring.md` featuring a 555-point expert rubric for Metadata, Apex, Flow, and LWC.
- **Automated Setup**: Added `/speckit.sf.setup` command to automatically install Salesforce CLI, GitHub CLI, and Code Analyzer v5.
- **Salesforce Code Analyzer v5 Support**: Full integration with PMD 7 and DFA scanner engines.
- **Auto-Heal Implementation Loop**: Added automated remediation logic to `/speckit.sf.implement` (up to 3 retries).
- **Blast Radius Analysis**: Integrated CLI-driven dependency mapping in `/speckit.sf.plan` to prevent architectural regressions.
- **19 Lifecycle Commands**: Complete coverage including Pre-Implementation Analysis (`/speckit.sf.analyze`), Project Constitution, Multi-org Deployment, and UAT.
- **Bundled Lifecycle Templates**: 9 standardized markdown templates under `templates/` for specs, technical plans, clarify reports, stories, hotfixes, and test scripts.
- **Skill-to-Command Sync**: Synchronization utility (`scripts/sync_skills_to_commands.py`) to maintain alignment between skills and extension commands.
- **Zero-Dependency Mode**: Removed requirement for external foundational skills; all best-practice knowledge is now embedded in the extension documentation.

### Fixed
- **Manifest**: Registered `/speckit.sf.setup` in `extension.yml` to enable CLI discovery.
- **Documentation**: Standardized official homepage link to GitHub Pages across manifest and README.
- **Branding**: Completed audit and removal of legacy external namespace references.

### Removed
- Deleted standalone migration guides in favor of a clean, unified workflow.
- Removed hard dependencies on external agent skills.

---
© 2026 Evernorth Strategic Development, Inc. Original work © 2026 Sumanth Yanamala.
