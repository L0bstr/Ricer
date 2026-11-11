# Contributing

Every change follows one workflow: **issue → branch → PR → merge**.

## Workflow

1. **Issue:** every change starts from an issue. Open one with the [task template](.github/ISSUE_TEMPLATE/task.md).
2. **Branch:** create a branch from an up-to-date `main`.
3. **Commit:** make small commits that follow the [commit style](#commit-messages).
4. **PR:** open a pull request into `main`.
5. **Review:** read through your own diff before merging.
6. **Merge:** merge the PR and delete the branch.

Nothing is pushed straight to `main`.

## Branch names

```
<type>/<issue-number>-<short-description>
```

Use lowercase and hyphens. The type is the same as in the commit style.

```
feat/12-cli-skeleton
fix/15-apply-missing-file
docs/3-write-contributing
```

## Commit messages

```
<type>: <short summary>
```

| Type    | Use for                              |
|---------|--------------------------------------|
| `feat`  | A new feature                        |
| `fix`   | A bug fix                            |
| `docs`  | Documentation only                   |
| `chore` | Everything else (tooling, cleanup)   |

Write the summary in the imperative, lowercase, with no trailing period:

```
feat: add module sync command
```

## Pull requests

- One issue per PR.
- Put `Closes #N` in the description so the issue closes when the PR merges.
- Check the diff against the issue's acceptance criteria before merging.
