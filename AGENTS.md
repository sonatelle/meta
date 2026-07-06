# Sonatelle Agent Guide

Sonatelle is a personal open-source workspace for careful tools, quiet experiments, and software shaped with patience.

The public tone should be restrained, sincere, and craft-focused. Do not over-market projects, inflate scope, or use startup-style language. When the emotional origin matters, express it indirectly: memory becoming craft, unfinished things becoming work, and persistence without spectacle.

## Workspace Model

- Treat `/Users/aliaxy/Documents/Sonatelle` as the local organization workspace.
- The root workspace may have its own meta repository for organization-level notes, assets, policies, and agent instructions.
- Each direct project directory should normally be its own Git repository.
- Do not turn the whole workspace into a monorepo for project code.
- Avoid Git submodules unless the user explicitly asks for them.

Recommended layout:

```text
Sonatelle/
  AGENTS.md
  README.md
  ROADMAP.md
  brand/
  docs/
  scripts/
  .github/
```

`brand/` is the source of organization visual assets.
`.github/` is the GitHub organization profile and default community-health repository.
Direct project directories are independent repositories unless the user explicitly chooses another model.

## Brand And Writing

- Prefer the display name `Sonatelle`.
- Prefer the organization description: `Open-source works from memory into craft.`
- Keep README copy short, calm, and concrete.
- Prefer plain English for public docs unless the user asks for Chinese.
- Avoid hype words such as revolutionary, ultimate, fastest, best, or all-in-one unless they are objectively proven and necessary.
- Do not expose private emotional details in public-facing files without explicit user approval.

### README Opening Style

- Project README openings may use the Sonatelle profile style: restrained, lyrical, and craft-focused.
- It is acceptable to begin from a musical form, memory, return, patience, or unfinished things becoming work, as long as the emotional origin remains indirect and dignified.
- When a project name comes from a musical form, explain the name briefly, connect it to the project's temperament, then move quickly into what the software does.
- Keep introductions short. Do not over-explain private context, and do not let lyrical writing replace clear scope, status, usage, or limitations.

## Engineering Values

- Favor reliability, safety, clarity, and maintainability over feature breadth.
- Make project boundaries explicit.
- Prefer small, testable crates or modules with clear APIs.
- Keep public claims aligned with implemented behavior.
- Document limitations honestly.
- Treat security-sensitive code, especially parsers and filesystem operations, as high-risk.

## Rust Defaults

For Rust projects under Sonatelle:

- Prefer a Cargo workspace when a project naturally has multiple crates.
- Prefer `MIT` unless the user chooses another license.
- Use `thiserror` or equivalent structured errors for library-facing errors.
- Use `tracing` for structured diagnostics when logging is needed.
- Keep unsafe code out unless there is a clear reason, and document every unsafe block.
- Add tests around path handling, error mapping, cancellation, and edge cases.

## File And Repository Hygiene

- Do not overwrite user-created files without checking their current contents.
- Preserve unrelated local changes.
- Put durable user-facing outputs in sensible project paths, not temporary folders.
- Keep generated assets and source assets clearly separated.
- Prefer concise comments and docs that explain intent, constraints, and non-obvious choices.

## Git Workflow

- Follow `.github/CONTRIBUTING.md` for branch, commit, pull request, and verification conventions.
- Keep commits focused on one intent and avoid mixing unrelated cleanup with feature or bug work.
- Use Conventional Commits for commit subjects, such as `docs(profile): add organization README`.
- Do not commit unrelated local changes, generated noise, or formatting churn outside the requested scope.
- Before committing, run the relevant checks for the changed project and record what was verified.
- Before creating any commit, show the proposed commit message to the user and wait for explicit approval of that message.
- If a direct project directory has its own `AGENTS.md` or `CONTRIBUTING.md`, follow the more specific project-level rules.

### Branch And Merge Discipline

- Keep `main` stable: it should represent work that is ready to run, publish, or build on.
- Use a short-lived branch for each meaningful change. Prefer one branch per intent, such as one feature, fix, documentation update, or cleanup.
- Avoid long-running branches. If a branch starts to collect unrelated work, split the work before merging when practical.
- Before merging, inspect the diff, run the relevant checks, and confirm the branch contains only the intended changes.
- Treat merge conflicts as design questions, not mechanical chores. Understand both sides of a conflict before resolving it.
- For solo development, pull requests are optional. Use a pull request when it helps create a clear checkpoint for review, release notes, risky changes, or future memory; do not require one for every small local change.
- Prefer fast-forward or squash merges for small, focused branches. Use a merge commit only when preserving the branch history is useful.
- After a branch is merged and no longer needed, delete it to keep the workspace easy to read.

## Agent Collaboration

- Before creating new project structure, check the current directory contents.
- When making design choices, explain the tradeoff briefly and choose a conservative default.
- When editing files, keep changes scoped to the request.
- When verification is possible, run it before claiming success.
- If a request touches GitHub, prefer explicit repository names and avoid guessing remote state.
- If a task requires network or filesystem access outside the current permission scope, ask for only the specific permission needed.
