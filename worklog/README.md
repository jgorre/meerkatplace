# worklog

A Claude Code plugin that logs what you accomplished in a session.

## Usage

At the end of a Claude Code session, run:

```
/worklog
```

Or with an optional note:

```
/worklog fixed the Trino gap detection query, unblocked the pipeline
```

Entries are appended to `~/worklog/worklog.md` in structured markdown format.

## Entry format

```markdown
## 2026-04-02

**Summary:** Fixed the Trino gap detection query that was producing false positives on partition boundaries.

**Value:** Unblocked the data pipeline team; nightly ingestion now completes without manual intervention.

---
```
