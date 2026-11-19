# SWE Web Blog Pipeline

Milestone 2 (agent system design) and Milestone 3 (first build) for DTX 495. Project: for each blog submission, the pipeline produces a **ready-to-upload Markdown file** and a **drafted Slack message** for the Web Committee Director — so the Blog Chairs stop wasting time formatting each post.

## Version 1 path (the one being built first)

A single blog submission row from the Google Form response spreadsheet:

```
One Google Form row (author, event title, body text)
  → Post Formatter           → drafts/<event>.md         (repo headers + verbatim body)
  → Director Notifier        → draft-notifications/<event>.md  (Slack draft, @Web Committee Director)
  → Blog Chair sends the Slack draft
```

**Left for later:** image downloading/resizing, automated GitHub uploads, and the "needs changes" revision loop.

## Repository layout

| Path | Contents |
| --- | --- |
| `.opencode/agents/` | The two subagent definitions: `post-formatter` and `director-notifier` |
| `.opencode/skills/` | The three shared skills: `header-mapping`, `verbatim-copy`, `title-carry-through` |
| `milestones/` | `milestone-1-final.md` (M1 Final) and `milestone-2-draft.md` (M2 design document) |
| `sources/` | Raw inputs: the Google Form response export and the repo header rules |
| `drafts/` | Generated Markdown blog posts (work in progress, not approved) |
| `draft-notifications/` | The drafted Slack messages for the Director |

## Agents

- **Post Formatter** — turns one intake form row into a Markdown file with the repo's headers (Header Mapping) and the body copied verbatim (Verbatim Copy). Writes to `drafts/`.
- **Director Notifier** — drafts one Slack message announcing the staged draft, tagging "@Web Committee Director" (Title Carry-Through). Writes only its own draft file; never posts to Slack itself.

## Skills

- **Header Mapping** — author name and event title go into the header, spelled exactly as in the form.
- **Verbatim Copy** — the body keeps the same number of paragraphs, text exactly as written.
- **Title Carry-Through** — the Slack draft names the right event and tags the Director.

## Rules that stay with people

The Blog Chair uploads the Markdown file to GitHub and sends the Slack draft. The Web Committee Director approves the post to go live. No agent in version 1 posts to Slack, approves anything, or uploads to GitHub.

## Course board (Figma System Map)

Board link: https://www.figma.com/board/F77NwWjqF8vPzztFuWx2nl/Diksha---Systems-Thinking-and-AI-Agents---Course-Board--Copy-?node-id=6-501&t=JuRnQ0C4bcDqdNb8-1

## Status

- Milestone 1 and Milestone 2 design documents complete.
- Agent and skill definitions scaffolded for the version 1 path.
- First end-to-end test running one of the 3 past form submissions is next.