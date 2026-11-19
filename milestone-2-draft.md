# Milestone 2 Draft: System Design

**Name: Diksha Durairaj**

*Make your own copy before you start: click File, then Make a copy. Keep the headings. You can delete the instructions in italics as you go.*

*This doc holds your agent cards, skills, and sources. Your system map goes in section 7 of your course board, and you link the board in Part 5. To see the level of detail I'm looking for, look at the example submission.*

## Part 1: My outcome and standards

*Paste these from your Milestone 1 Final. Update them if your thinking has changed.*

- **My system will produce: For each blog submission, a ready to be uploaded Markdown file, a folder of resized images, and a drafted Slack message for the director.**
- **It's for: Me and the other Blog Chairs, so we stop wasting time formatting each post, and the Web Committee Director, so she is notified as soon as a draft is staged.**
- **They'll use it to: I will upload the Markdown file and images directly to GitHub, and then send the drafted Slack message to the director. She will use the Slack ping to review the GitHub link and approve the post to go live.**
- **It starts from these inputs: The raw text and Google Drive image links from the submitter's intake form, and the CSS grid dimension rules for our website found on WordPress.**

| \# | Quality standard | Covered by |
| :---- | :---- | :---- |
| 1 | The Markdown file's header contains the author's name and the event title spelled as they were in the intake form. | Post Formatter |
| 2 | The output Markdown file has the exact same number of paragraphs as the original form submission text. | Post Formatter |
| 3 | The drafted Slack message contains the event title and tags "@Web Committee Director" | Director Notifier |

## Part 2: Agent cards

*One card per agent. Copy the table for each one. Each agent has one job. If you need the word and to describe it, it might be two agents.*

### Agent 1: Post Formatter

|  |  |
| :---- | :---- |
| **Does the job of** | Blog Chair, step 3 of your human system map (the formatting/reformatting step) |
| **Its one job** | Turn the raw parts of one intake form submission into a Markdown file with the repo's headers. |
| **Inputs** | Raw submission text; author name; event title; Google Drive image link — all from the Google Form response spreadsheet. Repo header rules — from the GitHub repo rules in step 3 of your human system map. |
| **Output** | A formatted Markdown file, handed to the Blog Chair for the GitHub upload. |
| **Allowed to** | Read files, edit files, run commands, use the web. List only what its job needs, and say what it can't do |
| **Standards it helps meet** | 1 & 2 |
| **Skills it uses** | Header Mapping, Verbatim Copy |

### Agent 2: Director Notifier

|  |  |
| :---- | :---- |
| **Does the job of** | Web Committee Director notification step (drafting the Slack ping) |
| **Its one job** | Draft one Slack message announcing a staged draft to the director. |
| **Inputs** | Event title — from the form submission. The staged draft's GitHub link — from the Blog Chair. |
| **Output** | The drafted Slack message, handed to the Blog Chair, who sends it to the Director. |
| **Allowed to** | Read the form row and the GitHub link. Write only the file that holds the Slack draft. It can't edit other files, run commands, use the web, post to Slack, or approve anything. |
| **Standards it helps meet** | 3 |
| **Skills it uses** | Title Carry-Through |

## Part 3: Skills

*One table for each skill named on your agent cards. A skill is a method an agent follows the same way every time. Every rule needs a source: a research log entry, a handbook or rule you found, or a real source. Copy the table for each skill.*

### Skill 1: Header Mapping

|  |  |
| :---- | :---- |
| **Used by** | Post Formatter |
| **What it's for** | Put the author name and event title into the Markdown header without changing how they're spelled. |
| **The steps or rules** | 1. Author name is spelled and capitalized exactly as in the form. 2. Event title is spelled and capitalized exactly as in the form. 3. Both go in the Markdown header. |
| **Where the know-how came from** | 1–2: Quality standard 2 → spelled as they were in the intake form. 3: Quality standard 2 → GitHub repo header rules, step 3 of your human system map; plus your clarification that the header comes from a line in the Google Form. |

### Skill 2: Verbatim Copy

|  |  |
| :---- | :---- |
| **Used by** | Post Formatter |
| **What it's for** | Keep the body text exactly as written while turning it into Markdown. |
| **The steps or rules** | 1. Count the paragraphs in the raw text. 2. The Markdown file has the same number of paragraphs. 3. Leave the paragraph text exactly as written. |
| **Where the know-how came from** | 1–2: Quality standard 3 → same number of paragraphs as the original. 3: Your clarification that body text must stay exactly as written. |

### Skill 3: Title Carry-Through

|  |  |
| :---- | :---- |
| **Used by** | Director Notifier |
| **What it's for** | Make the drafted Slack message name the right event and reach the director. |
| **The steps or rules** | 1. The message contains the event title. 2. The message contains "@Web Committee Director". 3. It's a draft only; the Blog Chair sends it. No GitHub link. |
| **Where the know-how came from** | 1–2: Quality standard 4 → "The drafted Slack message contains the event title and tags '@Web Committee Director'." 3: Added by you — Part 5 says "I will ... send the drafted Slack message," and you confirmed the link is left off for now. |

## Part 4: Sources

*The files your system reads. One row per source. Start from the Inputs and Sources section of your course board.*

| Source | What's in it | Read by | How it gets into my project folder | Do I have it? |
| :---- | :---- | :---- | :---- | :---- |
| Google Form response spreadsheet | Author name, event title, body text from one row per submission | Post Formatter (Header mapping, Verbatim copy) | Exported (fresh each run) | Yes — Part 8: "the 3 past blog submissions from our Google Form spreadsheet that I've already manually formatted and published." Only the 3 test rows are confirmed. |
| Event title (for the Slack draft) | The same title from the same row | Director Notifier (Title carry-through) | Exported with the sheet | Yes — same source as above. |
| Google Form itself | Where submitters enter answers that land in the sheet | No agent | Typed in by submitters | Yes, implicitly — Part 8 and Part 9 both refer to the intake form. |
| Repo header rules | The exact formatting and structure required for the Markdown headers | Post Formatter (Header mapping) | Saved as a text file in the project folder, or written directly into the skill | Yes |
| Staged draft's GitHub link | The URL to the staged Markdown file | Director Notifier (Title carry-through) | Typed in by the Blog Chair after staging the draft | Yes, created during the process |

## Part 5: My course board

*Paste the view link to your course board. Your system map is in section 7. Test the link in a private browser window.*

**Board link: https://www.figma.com/board/F77NwWjqF8vPzztFuWx2nl/Diksha---Systems-Thinking-and-AI-Agents---Course-Board--Copy-?node-id=6-501&t=JuRnQ0C4bcDqdNb8-1**

**My biggest open question: One thing about your design you're least sure of**

Since I'm leaving the automated Github integration and image formatting for a later time, my biggest open question is about the handoff between the agents and the Blog Chair. Where and how should the Post Formatter and Director Notifier deliver the finished Markdown file and the drafted Slack message so that it actually saves the Blog Chair time, instead of creating a new task of hunting down the generated files?