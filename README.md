# Agent Skills

[![skills.sh](https://skills.sh/b/fuadnafiz98/skills)](https://skills.sh/fuadnafiz98/skills)

Six skills for coding agents, by [fuadnafiz98](https://github.com/fuadnafiz98).
Each one is a single `SKILL.md` — no dependencies, nothing to configure.

## Install

Every skill:

```sh
npx skills add fuadnafiz98/skills
```

Or just the ones you want:

```sh
npx skills add fuadnafiz98/skills --skill clean-code --skill review-comments
```

Works with any agent that reads `SKILL.md` files, including Claude Code, where
each skill is also available as a slash command (`/clean-code`).

## The skills

| Skill | What it does | Reach for it when |
| --- | --- | --- |
| **clean-code** | Improves naming, structure, and dependency placement in code changed during the current task, without changing behaviour. | You have just implemented something and want it tidied before review. |
| **review-comments** | Removes comment and docstring noise — the obvious, the outdated, the ticket-specific — and keeps the rationale worth maintaining. | A diff is carrying comments that will not survive six months. |
| **rethink-solution** | Runs a second design pass over finished work to expose shortcuts, accidental complexity, and validation that only proves the happy path. | It works, but you suspect it is messy, overbuilt, or the easy path. |
| **resolve-conflicts** | Resolves every conflict in an in-progress rebase or merge, keeping the target branch's structure and reapplying the incoming intent. | Git has stopped mid-rebase and the conflicts are not trivial. |
| **batch-dependency-bumps** | Rolls a backlog of dependency-bump pull requests into one branch with a single lockfile regeneration, verifies it, then closes the originals as superseded. | Dependabot or Renovate has opened more PRs than anyone will review. |
| **output** | Reformats replies to be readable: the answer on line one, hard-wrapped at 80 columns, blocks of at most ten lines, and modes for headings, evidence, changelogs, and sparklines. | Wide-terminal replies are a wall of text you skip. |

## Licence

[MIT](LICENSE).
