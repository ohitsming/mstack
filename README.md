# mstack

Opinionated Claude Code skills for building and shipping products. Each one plans before it acts, asks before risky changes, and shows evidence instead of claiming success.

## Install

In Claude Code:

```text
/plugin marketplace add ohitsming/mstack
/plugin install mstack@mstack
```

Third-party marketplaces don't auto-update by default. To turn it on, run `/plugin`, open **Marketplaces**, select `mstack`, and enable auto-update. To update by hand, run `/plugin marketplace update mstack`.

## Skills

| Command | Use it when |
| --- | --- |
| `/mstack:swe` | You want a change built as a staff engineer would: understand the code, plan and wait for your OK, reproduce bugs first, implement, then prove it works. |
| `/mstack:audit` | Before you push. Reviews your uncommitted and unpushed changes through three lenses (staff engineer, QA, pentester) and ranks the findings. Pass a ref like `main` to diff against it. |
| `/mstack:brainstorm` | You have an idea and want a decision, not a list. Frames the problem, compares approaches, and ends with a one-page plan and a kill criterion. Writes no code. |
| `/mstack:ux` | You're designing or building UI. Covers the user's moment, every state, real microcopy and accessibility, then implements it. |
| `/mstack:marketing` | You need positioning, copy, or a go-to-market call tied to a measurable outcome. Produces final drafts, not outlines. |

## Permissions

Only `audit` pre-approves tools, and only read-only ones (`Read`, `Glob`, `Grep`, and `git diff/log/status/show/merge-base`). Every other skill uses your normal permission prompts.

## Project rules come first

Every skill reads your project's `CLAUDE.md` and follows it over its own defaults, so put your style rules, guardrails and locked decisions there.

## License

[MIT](LICENSE)
