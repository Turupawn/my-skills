---
name: ship
description: Get it done. No safety nets.
disable-model-invocation: true
allowed-tools: Read, Write, Edit, Bash, Grep, Glob
---

Before doing anything, run this:
echo -e "\n\033[1;35m══════════════════════════════════\033[0m"
echo -e "\033[1;33m  ⚡ SHIP MODE ⚡\033[0m"
echo -e "\033[1;35m══════════════════════════════════\033[0m\n"

Task: $ARGUMENTS

Rules:
- Use ONLY existing patterns, conventions, and libraries already in the codebase
- Do NOT introduce new patterns, new abstractions, new utilities
- Do NOT add error handling, try/catch, validation, or fallbacks
- Do NOT add defensive programming or input validation
- Do NOT refactor or "improve" anything I didn't ask about
- Do NOT add dependencies without asking
- Look at how similar things are already done in the code and do it the same way
- Minimal changes. Get it working. Stop.
