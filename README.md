# Agent Skills

[![skills.sh](https://skills.sh/b/fuadnafiz98/skills)](https://skills.sh/fuadnafiz98/skills)

Reusable agent skills by [fuadnafiz98](https://github.com/fuadnafiz98).

Licensed under the [MIT License](LICENSE).

## Available skills

### clean-code

Reviews code changed in the current task and applies focused readability and maintainability improvements without changing behavior.

Install it with:

```sh
npx skills add fuadnafiz98/skills --skill clean-code
```

### review-comments

Reviews comments and docstrings in current code changes, removes maintenance noise, and preserves durable rationale.

Install it with:

```sh
npx skills add fuadnafiz98/skills --skill review-comments
```

### batch-dependency-bumps

Rolls several open dependency-bump pull requests into one branch with a single lockfile regeneration, verifies it, then closes the originals as superseded.

Install it with:

```sh
npx skills add fuadnafiz98/skills --skill batch-dependency-bumps
```

### output

Formats replies to actually get read: verdict on the first line, blocks of at most ten lines, hard-wrapped at 80 columns, front-loaded headings. Eight modes on top of that floor — layer-cake, bluf, receipts, hook-loop, patch-notes, sparkline, quiz, greentext — chosen to fit the reply, or named explicitly (`/output 4chan`, `/output bluf`, `/output 72`). Persists for the session.

Install it with:

```sh
npx skills add fuadnafiz98/skills --skill output
```

Or install every skill in this repository:

```sh
npx skills add fuadnafiz98/skills
```

## Publishing

Skills are discovered from `skills/*/SKILL.md`. After pushing this repository to GitHub, validate and publish a release with:

```sh
gh skill publish --dry-run
gh skill publish --tag v1.0.0
```

The first install through the Skills CLI makes the skill eligible to appear automatically on [skills.sh](https://skills.sh).
