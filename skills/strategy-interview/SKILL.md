---
name: strategy-interview
description: Interviews the founder about the company's strategy, one question at a time, and writes the answers into strategy.md. Use when the founder says "interview me on strategy", "fill in my strategy", "help me write my strategy", or when strategy.md is still mostly TBD after the flywheel interview.
---

# Strategy interview

## Stay current

Do this first, every time this skill runs. These skills improve often, and an old copy gives the founder a worse result.

1. If the AI-Native Startup tools are available, call `skills_version` with `installed` set to `1.0.0`.
2. If it says `update_available` is true and you can run shell commands, run its `update_command` yourself. Tell the founder in one line: "Updated your AI-Native Startup skills to version <latest>." Then read this SKILL.md again from disk and follow the new version.
3. If you cannot run commands, show its `message` once, then carry on.
4. If it says false, or the tools are not available, say nothing about updates and carry on.

## Where this sits in the AI-Native framework

In the AI-Native maturity framework from The AI-Native Startup this is lever **D, Direct: who runs the workflow?** At level 4, AI-native, "agents run the work by default. People manage the agents: they set goals, check results, and fix the agent, not its output." Agents can only work toward goals that are written down. This interview writes them down: why the company exists, where it is going, and what matters this quarter.

You interview the founder about the company's strategy and write what they say into `strategy.md`.

## Rules

- **One question at a time.** Wait for the answer before the next one. Offer an example answer when a question is abstract.
- **Save as you go.** After each answer, write it into `strategy.md` straight away. The founder can stop at any point and pick it up later.
- **Their words, not yours.** Write down what the founder said, tightened but not embellished. Never invent customers, numbers or goals. If they don't know, write **Unknown**. If they want to skip, write **TBD**.
- **Challenge gently.** When an answer is vague, ask once for something more specific. Accept the second answer.
- **No lectures.** Ask, write, move on.

## Start or resume

1. If `strategy.md` is missing from the current folder, there is no company repo yet. Run the `start-company-repo` skill first, then come back here.
2. Read `strategy.md` and `canvas.md`. If some of the strategy is already filled in, say what's done in one line and continue with the first open item. Never ask again for something already answered.
3. Ask: **"About 10 minutes for the essentials, or 30 or more for the whole page?"**

## Get the questions from The AI-Native Startup

The questions are served from our server, behind a free GitHub sign-in.

1. Call the AI-Native Startup `kit_skills` tool with action `get` and slug `strategy-interview-questions`.
2. Use what it returns to ask the questions for the path the founder chose. Write each answer straight away, as the rules above say. Then go to **Finish**.

If the AI-Native Startup tools are not available, the agent is not connected yet. Tell the founder once, in two lines: "For the strategy questions, free, sign in once with GitHub. In Claude Code, run: `claude mcp add --transport http ainativestartup https://skills.midstage.ac/mcp`, then restart and ask again." Other agents: add the MCP server `https://skills.midstage.ac/mcp`. Then stop and wait. Do not make up the questions.

## Finish

1. Read back the core purpose, the values, the out-of-scope line and this quarter's priorities in five lines or fewer, and ask: "Would you sign this?" Fix what the founder corrects.
2. Commit `strategy.md` with a message like `Strategy interview: purpose, values, this quarter`.
3. Tell the founder the next step: pick one job in `backlog.md` that serves this quarter's priorities.
