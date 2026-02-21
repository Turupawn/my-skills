---
name: prd-04-compare
description: Compare implementations between this folder and other-impl.
disable-model-invocation: true
allowed-tools: Read, Grep, Glob, Bash, Write
---

Before doing anything, run this:
echo -e "\n\033[1;35m══════════════════════════════════\033[0m"
echo -e "\033[1;35m  ⚖️ PRD: COMPARE\033[0m"
echo -e "\033[1;35m══════════════════════════════════\033[0m"
echo ""
echo -e "\033[1;33m── FILES THAT DIFFER ─────────────\033[0m"
diff -rq . ./other-impl/ --exclude=node_modules --exclude=.git --exclude=other-impl --exclude=COMPARE.md --exclude=PRD.md --exclude=.next --exclude=dist --exclude=build 2>/dev/null || true
echo -e "\033[1;33m──────────────────────────────────\033[0m\n"

For each file that differs, run:
diff --color -u ./[file] ./other-impl/[file]

Then analyze and save to COMPARE.md with TWO sections:

## Base Implementation
Pick which implementation (this or other-impl) should be used as the base. Explain why.

## Changes to Cherry-Pick from the Other
List specific things from the losing implementation that should be brought over:
- **File**: which file
- **What**: what to bring over
- **Why**: why it's better than what the base has
