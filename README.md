# AI-Native Skills

Skills that help you run your startup with AI agents. They set up a repo that holds your whole company, interview you about the business, and keep your agents safe and consistent. They work in Claude Code first, and in any agent that reads `SKILL.md` skills.

## Install

**With one sentence.** Paste this into your agent. No command line needed:

> Install the AI-Native skills from https://theainativestartup.com/skills/llms.txt

Or open https://theainativestartup.com/skills and use the Copy prompt, Add to Claude or Add to ChatGPT button.

**With npx:**

```
npx skills add midstage/ainative
```

Then tell your agent: `start my company repo`.

**By hand (Claude desktop app or claude.ai):** download the zips in `zips/`, then upload each one under Settings, Capabilities, Skills.

You need a GitHub account (the skills set up a private repo for your company there) and an agent such as Claude Code.

## What is in it

| Skill | What it does |
|---|---|
| `start-company-repo` | Creates your private company repo from the AI-Native Startup Template. |
| `flywheel-interview` | Interviews you, one question at a time, and writes your answers into the repo. About 10 minutes for the short path. |
| `strategy-interview` | Interviews you about purpose, goals and this quarter, and writes your strategy page. About 10 minutes for the essentials. |
| `company-memory` | Saves decisions and handovers to files, so no session starts from zero. |
| `door-rules` | Keeps agents from sending, spending or publishing without your approval. |

## Updates

The skills keep themselves current. Each time one runs, it checks The AI-Native Startup's server for a newer version. In Claude Code it installs the update itself and tells you in one line. Elsewhere it tells you once how to update. To update by hand: `npx skills update -g -y`.

## License

PolyForm Internal Use License 1.0.0, see `LICENSE.md`. Copyright Scale-up Allies LLC, dba Midstage Accelerator.
