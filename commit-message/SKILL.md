---
name: commit-message
description: Writes commit messages. Use when creating a commit, writing a commit message, or when the user asks to summarize changes for a commit.
---

When writing a commit message:

1. Run `git diff HEAD` to see the changes that have been made since the last commit. This will help you understand what changes you are committing and how to summarize them in your commit message.
2. Write a message following this format:

## Title
One sentence explaining what this PR does.

## Description
Brief context on why this change is needed

## Changes

- Bullet points of specific changes made
- Mention any files deleted or renamed
