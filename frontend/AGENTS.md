# Agent instructions

## Commit convention

- Use Conventional Commits: `<type>(<optional-scope>): <summary>`.
- Use `feat` for new features, `fix` for bug fixes, `refactor` for restructuring without behavior changes, `docs` for documentation, `style` for formatting, `test` for tests, and `chore`, `build`, or `ci` for maintenance, build, or automation changes.
- Write a concise, imperative summary, starting with a lowercase verb and without a trailing period.
- Use a scope when it helps identify the affected area, for example `feat(home): add Bakehub branding`.
- Mark breaking changes with `!` before the colon and explain them in a `BREAKING CHANGE:` footer.
- Keep each commit focused on one logical change; commit documentation separately when practical.

## Commit and push workflow

- When asked to commit or push, inspect the current branch, Git status, diffs, untracked files, and configured remote first.
- Include requested untracked files and the related tracked changes needed to keep the commit complete. Preserve unrelated work and never stage secrets, dependencies, caches, or generated build output.
- Review the staged diff and run checks appropriate to the changes before committing. For frontend application changes, run `npm run build` from `frontend`; report any failures or checks that could not run.
- When the user explicitly requests both commit and push, carry out both steps without asking for redundant confirmation, subject to required environment approvals.
- Push the current branch to its configured upstream, setting an upstream only when needed. Do not force-push, amend published commits, or rewrite history unless explicitly requested.
- After pushing, verify the working tree and branch synchronization. Report the commit hashes, commit messages, destination branch, and validation results.
