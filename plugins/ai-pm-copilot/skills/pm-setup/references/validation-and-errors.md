# Validation & Error Handling

## Validation

After each step, validate that essential information is provided:

**Essential per required file:**

- product-info.md: name, description, stage, target market, value prop (all required)
- tech-stack.md: frontend, backend, database, infrastructure, architecture (all required)

**For optional files:**

- strategic-goals.md: at least vision OR 3 priorities
- business-metrics.md: at least 2 metrics
- team-info.md: team size and cadence

If essential fields missing:

```
Warning: Missing required information:
- [Field name]: [Brief explanation of why it's needed]

Would you like to:
1. Provide this information now
2. Cancel this file

Your choice (1/2):
```

---

## Error Handling

**If .claude/ directory doesn't exist:**

```bash
mkdir -p .claude/product-context
```

**If file write fails:**

```
Error writing to [file_path]

Possible issues:
- Directory permissions
- Disk space

Would you like to:
1. Retry
2. Skip this file
3. Cancel setup

Your choice (1/2/3):
```

**If agent invocation fails** (for strategic-goals):

```
Error invoking product-strategist agent

Falling back to manual input. Let's capture your strategic direction:

[Proceed with manual questions for strategic-goals]
```

**If user quits mid-setup:**

```
Setup incomplete. Files created so far:
- product-info.md (created)
- tech-stack.md (not created)

Required files are incomplete. Please run /pm-setup again to finish.
```
