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

## Comments And Documentation

Comments must be present, purposeful, and free of noise: do not skip them, do not
under-document public surfaces, and do not restate what the code already says.
These rules apply to every language, not only Rust.

### What To Comment

- Explain intent, constraints, invariants, and non-obvious tradeoffs — the "why",
  not a paraphrase of the "what".
- Give every public API item a doc comment stating what it does, its inputs and
  outputs, and its notable failure modes.
- Open every file or module with a one-line statement of its responsibility.
- In security-sensitive code (path handling, parsers, filesystem, concurrency,
  unsafe), document the invariant it upholds and the precondition it assumes.

### What Not To Comment

- Do not narrate obvious code (`// increment i`).
- Do not leave commented-out code; delete it, since history keeps it.
- Do not leave an unowned `TODO`/`FIXME`; link an issue or drop it.
- Do not restate the type signature in prose.

### Density

- Match the comment density of the surrounding code.
- Prefer one clear sentence over a paragraph. If a comment needs a paragraph, the
  code may need simplifying first.
- Write comments in English.

### Doc-Comment Form Per Language

Use each language's idiomatic doc-comment form; keep the content rules above
identical across all of them.

| Language | Item doc comment | Module / file header | Inline note |
| --- | --- | --- | --- |
| Rust | `/// ...` | `//! ...` | `// NOTE:`, `// SAFETY:` |
| Go | `// Foo does ...` (starts with the name) | `// Package foo ...` | `// NOTE:` |
| TypeScript / JavaScript | `/** ... */` (JSDoc) | top-of-file `/** ... */` | `// NOTE:` |
| Python | `"""..."""` docstring | module docstring | `# NOTE:` |
| Shell | `# foo: ...` above the function | shebang plus a `# ...` summary | `# NOTE:` |

### Example

Prefer intent over restatement:

```rust
// Bad: restates the code.
// Add one to the retry counter.
retries += 1;

// Good: explains why.
// A transient DNS failure is expected on cold start; retry before surfacing it.
retries += 1;
```

## Git Workflow

- Follow `.github/CONTRIBUTING.md` for branch, commit, pull request, and verification conventions.
- Keep commits focused on one intent and avoid mixing unrelated cleanup with feature or bug work.
- Use Conventional Commits for commit subjects, such as `docs(profile): add organization README`.
- Do not commit unrelated local changes, generated noise, or formatting churn outside the requested scope.
- Before committing, run the relevant checks for the changed project and record what was verified.
- Before creating any commit, show the proposed commit message to the user and wait for explicit approval of that message.
- If a direct project directory has its own `AGENTS.md` or `CONTRIBUTING.md`, follow the more specific project-level rules.

### Branch And Merge Discipline

- Use one short-lived branch for each relatively independent feature, fix, refactor, documentation change, or cleanup. Split unrelated work before opening a pull request.
- Do not merge completed work locally into long-lived branches. Push the short-lived branch to GitHub and merge through a pull request, even for solo development.
- Use GitHub `Rebase and merge` by default. Use `Squash and merge` only when collapsing noisy work-in-progress commits is clearer.
- Fill out pull request details carefully: what changed, why it changed, how it was verified, and any risks, limitations, or follow-up work. Delete short-lived branches after merge.
- Long-lived branches may include `main`, `develop`, `release/*`, and `stable`. Keep them stable for their purpose and do not use them for active feature work.

### Commit Timing

- Commit in small, single-intent increments. Land a coherent unit as soon as it
  stands on its own and passes its checks, rather than accumulating a large batch.
- Prefer several small commits over one broad commit. If a change touches unrelated
  concerns, split it before committing.
- Scaffold with native tooling (for example `cargo new`, `cargo add`) and then edit,
  instead of hand-writing generated files.
- Each commit should build and pass the relevant checks on its own, so history stays
  bisectable.
- Keep each self-contained slice to its own pull request; do not let one branch grow
  into an unreviewable change.

## Agent Collaboration

- Before creating new project structure, check the current directory contents.
- When making design choices, explain the tradeoff briefly and choose a conservative default.
- When editing files, keep changes scoped to the request.
- When verification is possible, run it before claiming success.
- If a request touches GitHub, prefer explicit repository names and avoid guessing remote state.
- If a task requires network or filesystem access outside the current permission scope, ask for only the specific permission needed.
