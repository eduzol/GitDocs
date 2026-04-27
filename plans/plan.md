# Worktree Test Plan

## Goal

Implement three independent markdown changes in parallel using separate git worktrees. Each subagent should create its own feature branch, work in its own worktree, and produce one folder containing one markdown document.

## Planned Changes

1. Create `plans/lorem-1/lorem-1.md` with the title `# Lorem 1`.
2. Create `plans/lorem-2/lorem-2.md` with the title `# Lorem 2`.
3. Create `plans/lorem-3/lorem-3.md` with the title `# Lorem 3`.

Each document should contain simple lorem ipsum placeholder text, for example:

```markdown
# Lorem X

Lorem ipsum dolor sit amet, consectetur adipiscing elit.
```

## Parallel Worktree Branches

Use one branch per change:

- `feature/plan-lorem-1` creates `plans/lorem-1/lorem-1.md`.
- `feature/plan-lorem-2` creates `plans/lorem-2/lorem-2.md`.
- `feature/plan-lorem-3` creates `plans/lorem-3/lorem-3.md`.

## Merge Notes

After all three subagents finish, review each branch independently and merge them back into the main working branch. The changes should not conflict because each branch writes to a separate folder and file.
