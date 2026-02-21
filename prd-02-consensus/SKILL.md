---
name: prd-02-consensus
description: Review PRD against the other AI's version. Hard diff first.
disable-model-invocation: true
allowed-tools: Read, Grep, Glob, Bash, Write
---

Before doing anything, run this:
echo -e "\n\033[1;34m══════════════════════════════════\033[0m"
echo -e "\033[1;34m  🤝 PRD: CONSENSUS\033[0m"
echo -e "\033[1;34m══════════════════════════════════\033[0m"
echo ""
echo -e "\033[1;33m── PRD DIFF ──────────────────────\033[0m"
diff --color -u ./PRD.md ./other-impl/PRD.md || true
echo -e "\033[1;33m──────────────────────────────────\033[0m\n"

Read both PRD.md and ./other-impl/PRD.md.

For each difference:
- State both positions
- Say which you think is better and why
- If you disagree with both, say what you'd do instead

For anything unclear or risky:
- Flag it as an open question for the human

Then ask me:
"Here are the changes I'd make to PRD.md: [list each one].
Should I apply them?"

DO NOT update PRD.md until I confirm.
If I say no or modify, adjust and ask again.
