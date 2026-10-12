<p align="center">
  <picture>
    <source media="(prefers-reduced-motion: reduce)" srcset="assets/logo.png">
    <img src="assets/logo-animated.gif" alt="Cadre octopus logo" width="120" height="120">
  </picture>
</p>

<h1 align="center">Cadre</h1>
<p align="center">A workspace for your coding agents.</p>
<p align="center">
  <a href="https://github.com/ayorcodes/cadre/releases/latest/download/Cadre-mac-arm64.dmg">Download for Mac</a>
  · <a href="https://github.com/ayorcodes/cadre/releases/latest">Release notes</a>
</p>

Describe what you want to build or fix. Cadre coordinates agents that research
your code, plan the changes, write them and review the result. Follow the work
and answer their questions in one place, then review the pull request.

Works with **Claude Code, Codex and Cursor's agent**, using your existing account
or API key. The current desktop release is for Macs with Apple silicon.

## Get started

You'll need:

- A Mac with Apple silicon running **macOS 13 or later**.
- Claude Code, Codex or Cursor's agent installed and signed in.
- The [GitHub CLI](https://cli.github.com/) installed and signed in if you want
  agents to open pull requests.

1. [Download the Mac installer](https://github.com/ayorcodes/cadre/releases/latest/download/Cadre-mac-arm64.dmg).
2. Open the DMG and drag Cadre into Applications.
3. Open Cadre, add your repository folder and choose your coding agent.
4. Describe the task and start a run.

The installer is signed and notarized. Each release includes `SHA256SUMS.txt`.
To check your download, run this in the folder containing the installer and
compare the result with the checksum on the same release:

```bash
shasum -a 256 Cadre-mac-arm64.dmg
```

## How your task gets done

The Chief agent reads your request and routes it to the right agents. Each
agent has its own conversation and instructions. Agents share findings, ask
each other questions and send work back when it needs changes.

| Task                         | How agents approach it                                                                 |
| ---------------------------- | -------------------------------------------------------------------------------------- |
| A bug with a known cause     | An agent writes the fix, then a separate reviewer checks it.                           |
| A new feature                | Agents research the code, plan the feature and design the changes before writing code. |
| A bug that keeps coming back | Agents investigate and test possible causes before writing a fix.                      |
| Several tasks                | Agents group the work into phases and check each phase before starting the next.       |

Completed changes become a pull request assigned to you. You decide whether
to merge it.

## While agents work

- **Follow the conversation.** Read each agent's work, questions and answers.
  Message the Chief or type `@` to address another agent.
- **Answer questions as they come up.** When an agent needs your input, the run
  pauses. Choose a suggested answer or write your own. Auto lets agents answer
  for you and records what they decided.
- **See the review rounds.** A separate reviewer checks the changes against
  the design and your project's standards, then sends problems back for a fix.
- **Track usage and estimated costs.** See tokens, elapsed time and estimated
  cost for each agent and the whole run. Check a message's estimated cost
  before sending it.
- **Work on several tasks.** Start a separate run for each task; each keeps its
  changes on its own branch.
- **Use the keyboard.** Find actions in the command palette or use shortcuts.

## Your code and accounts

Agents read and edit files in your local checkout. Your coding agent may send
code and prompts to its provider, just as it does when you use it directly.
Your provider's data policies still apply.

Cadre uses the coding agent you choose with your existing plan or API key.
Cursor support is newer and may have rough edges.

## Releases and feedback

This repository contains public desktop downloads, release notes and brand
assets. The application and engine source repositories are maintained separately.

- [All releases](https://github.com/ayorcodes/cadre/releases)
- [Report a problem or request a feature](https://github.com/ayorcodes/cadre/issues)

For a bug report, include your macOS version, the Cadre version, the coding
agent you selected and the steps that reproduce the problem.
