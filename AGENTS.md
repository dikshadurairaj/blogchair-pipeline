# AGENTS.md: SWE Web Blog Pipeline Handbook

Every agent working in this project reads and follows this handbook.

## Who we are

The SWE Web team publishes blog posts from the intake form onto the club website. This pipeline turns one blog submission into a formatted Markdown draft and a drafted Slack message for the Web Committee Director.

## The team (version 1)

- **Post Formatter** (subagent): turns one intake form row into a Markdown file with the repo's headers and verbatim body text. Writes to `drafts/`.
- **Director Notifier** (subagent): drafts one Slack message announcing the staged draft to the Web Committee Director. Writes only its own draft file in `draft-notifications/`. Never posts to Slack itself.
- **Blog Chair** (the human in this chat): uploads the Markdown file to GitHub, sends the drafted Slack message, and is the only one who can move a post toward approval.

## Folders

- `sources/`: raw inputs. The Google Form response export (one row per submission) and the repo header rules. Read-only inputs.
- `drafts/`: generated Markdown blog posts. Work in progress; nothing here is approved.
- `draft-notifications/`: the drafted Slack messages for the Director, one per staged draft.
- `milestones/`: the course design documents (Milestone 1 final, Milestone 2 draft).
- `.opencode/agents/` and `.opencode/skills/`: the agent and skill definitions.

## Rules

1. The Google Form response row is the source of truth for the author name, event title, and body text. Spelling and capitalization come from the form, never "corrected."
2. The body text is copied verbatim — same number of paragraphs, text left exactly as written.
3. Every drafted Slack message contains the event title and tags "@Web Committee Director". It is a draft only; the Blog Chair sends it.
4. No agent posts to Slack, approves anything, or uploads to GitHub. Those stay with the Blog Chair and the Director.
5. Version 1 does not resize images, automate GitHub uploads, or run a "needs changes" revision loop.

## Version 1 one-path flow

```
One Google Form row (author, event title, body text)
  → Post Formatter  → drafts/<event>.md        (repo headers + verbatim body)
  → Director Notifier → draft-notifications/<event>.md  (Slack draft, @Web Committee Director)
  → Blog Chair sends the Slack draft
```

Left for later: image downloading/resizing, automated GitHub uploads, and the "needs changes" revision loop.