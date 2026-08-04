# commit-message

**Stop writing "fix stuff". Get a commit message you'll still understand in six months.**

Every commit gets the same three-part shape — a one-sentence title, why the change was needed, and a bulleted list of what actually moved. Your `git log` becomes something you can read back instead of something you have to `git show` your way through.

It works from the diff, not from the conversation. That's the part that matters: asked for a commit message off the back of a working session, a model summarizes the session — so the thing you fixed in passing goes unmentioned, and the thing you talked about but didn't do can end up in the message. This runs `git diff HEAD` first and describes the commit that's actually staged.

Renames and deletions get called out explicitly, because they're the changes most often dropped from a summary and the most annoying to rediscover six months later.

## What you get

```markdown
## Title

One sentence explaining what this PR does.

## Description

Brief context on why this change is needed

## Changes

- Bullet points of specific changes made
- Mention any files deleted or renamed
```

Note this isn't [Conventional Commits](https://www.conventionalcommits.org) — no `feat:` or `fix:` prefixes, nothing for a semver tool to parse. It optimizes for a human reading the log.

## Using it

Ask for a commit message and it applies itself. Or call it:

```
/commit-message
```

## Installing

```bash
cp -r commit-message ~/.claude/skills/
```

Only `SKILL.md` is read by Claude Code; this README rides along and is ignored.
