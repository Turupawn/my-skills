---
name: prd-01-init
description: Generate a PRD from existing code.
disable-model-invocation: true
allowed-tools: Read, Grep, Glob, Bash, Write
---

Before doing anything, run this:
echo -e "\n\033[1;34m══════════════════════════════════\033[0m"
echo -e "\033[1;34m  📋 PRD: INIT\033[0m"
echo -e "\033[1;34m══════════════════════════════════\033[0m\n"

Explore the codebase and generate a PRD based on: $ARGUMENTS

The PRD should include:
- Summary of what exists now (from the code, not assumptions)
- Proposed changes
- High-level logic for each change
- Files likely affected
- Open questions for the human to decide

Save it to PRD.md in the project root.
Keep it high-level. No code if possible.
