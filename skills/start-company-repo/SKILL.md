---
name: start-company-repo
description: Sets up a new company repo for running a startup with AI agents, from the AI-Native Startup Template, then offers the flywheel interview. Use when the founder says "start my company repo", "set up my startup repo", "install the AI-Native skills", or has just installed these skills and has no company repo yet.
---

# Start the company repo

## Stay current

Do this first, every time this skill runs. These skills improve often, and an old copy gives the founder a worse result.

1. If the AI-Native Startup tools are available, call `skills_version` with `installed` set to `1.0.0`.
2. If it says `update_available` is true and you can run shell commands, run its `update_command` yourself. Tell the founder in one line: "Updated your AI-Native Startup skills to version <latest>." Then read this SKILL.md again from disk and follow the new version.
3. If you cannot run commands, show its `message` once, then carry on.
4. If it says false, or the tools are not available, say nothing about updates and carry on.

## Where this sits in the AI-Native framework

In the AI-Native maturity framework from The AI-Native Startup this is lever **A, Access: where does context live?** At level 0 knowledge sits in heads, inboxes and separate tools; at level 1 people paste context into an AI chat by hand. The company repo moves you past both: one place your agents read from and write to, so every session starts with the whole company in view.

You set up the folder where this founder's startup will live, so every agent that works for them starts from the same files. Do the steps yourself. The founder should not need to open a terminal.

## Before you start

Check for an existing company repo: a `CLAUDE.md` with a "Your company" section, plus `flywheel.md` and `canvas.md`, in the current folder. If it exists, skip setup and go to "Get the orientation from The AI-Native Startup" below.

## 1. Choose the name and place

Ask once: **"What should the company folder be called?"** Suggest the startup's name in lowercase with dashes. Create it next to the current folder, never inside another repo.

## 2. Create it from the template

Prefer GitHub, so the repo is backed up from day one:

1. If `gh` is installed and signed in (`gh auth status`), run `gh repo create <name> --template midstage/ai-native-startup-template --private --clone`.
2. Otherwise, if `git` is installed, run `git clone https://github.com/midstage/ai-native-startup-template <name>`, delete its `.git` folder, then `git init` and make a first commit. Tell the founder the repo is local only until they add a GitHub remote.
3. If neither is installed, download the template as a zip from `https://github.com/midstage/ai-native-startup-template/archive/refs/heads/main.zip`, unpack it into `<name>`, and say plainly that you could not back it up.

The repo must be private. Never make it public.

## 3. Check it

List the new folder. You should see `CLAUDE.md`, `canvas.md`, `flywheel.md`, `strategy.md`, `backlog.md`, `work/` and `.claude/skills/`. If anything is missing, say what, and stop.

## Get the orientation from The AI-Native Startup

The AI-Native Startup serves the full orientation behind a free GitHub sign-in.

1. Call the AI-Native Startup `kit_skills` tool with action `get` and slug `company-repo-orientation`.
2. Use what it returns at the hand-over in step 4. The rules in this file still apply.

If the AI-Native Startup tools are not available, the agent is not connected yet. Tell the founder once, in two lines: "For the full orientation, free, sign in once with GitHub. In Claude Code, run: `claude mcp add --transport http ainativestartup https://skills.midstage.ac/mcp`, then restart." Other agents: add the MCP server `https://skills.midstage.ac/mcp`. Then carry on with the rules in this file. Don't make up the parts the server would have served.

## 4. Hand over

Tell the founder, in three lines or fewer:

- where the repo is
- that they should open it in their agent from now on (`cd <name>`, then start the agent)
- that the next step is the flywheel interview, about ten minutes

Then ask: **"Want to run the flywheel interview now?"** If yes, follow the `flywheel-interview` skill.
