---
name: worklog
description: "Log what was accomplished in this Claude Code session. Invoke at end of session with an optional note: /worklog [note]. Appends a structured markdown entry to ~/worklog/worklog.md."
---

You are writing a work log entry for what was accomplished in this session.

## Instructions

1. **Gather context**: Review the full session to understand what was done — files changed, bugs fixed, features added, refactors, investigations, etc.

2. **Use the user's note if provided**: The user may have provided a note as arguments: `$ARGUMENTS`. If present, use it to guide and inform the summary. If empty or absent, infer everything from session context alone.

3. **Write the entry** in this exact format:

```
## YYYY-MM-DD

**Summary:** One to three sentences describing what was accomplished.

**Value:** What this unblocked, improved, or delivered.

---
```

Use today's date. Be concise and concrete — no filler, no preamble.

4. **Append to file** using Bash:

```bash
mkdir -p ~/worklog
cat >> ~/worklog/worklog.md << 'ENTRY'

<the entry content here>
ENTRY
```

Create the directory and file if they don't exist. Append — never overwrite.

5. **Confirm** by telling the user what was logged, quoting the entry briefly.
