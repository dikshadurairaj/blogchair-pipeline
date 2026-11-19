# Milestone 1 Final: Problem and Systems Brief

**Name: Diksha Durairaj**

*Make your own copy before you start: click File, then Make a copy. Keep the headings. You can delete the instructions in italics as you go.*

*This is your project proposal. Parts 1 to 4 come from your draft, revised. Parts 5 to 9 are new. To see the level of detail I'm looking for, look at the [example submission](https://docs.google.com/document/d/1tBJ5s8A2n7nrIurvxohvs3toqBReEjuoznyikOT8XzQ/edit).*

## Part 1: The problem

*Paste this from your draft, then revise it with what you've learned. 3 to 5 sentences.*

- **Who has the problem: Me, as one of the blog chairs on the SWE Web team, the Web Committee director that manages the publishing schedule, and the general SWE members who submit posts but never receive status updates.**  
- **The job they're trying to get done: Get blog submissions from the form onto the website efficiently. Make sure all the posts are high quality and accurate to the event they are about, and do so in a timely manner with posts going up 2-3 days after being submitted and twice a week. All posts must also be formatted properly with correctly sized images.**  
- **Where it goes wrong today: Right now, the process of uploading submissions to the site takes forever because of all the manual data entry. Blog chairs spend 30+ minutes per post downloading and resizing images and retyping text into the correct format, while the approval system relies entirely on manual Slack pings instead of automated notifications.**

## Part 2: Research log

*Paste your rows from the draft and add any new ones. Have at least 3 rows. Use a made-up name or a label like Interview 1 for every person. Quotes must come from a real person or a real source.*

*Type: Conversation, Observation (you watched someone do the work, or did it yourself and wrote down each step), or Source (something people wrote or recorded about doing this work).*

| \# | Type | Who or what | What they said or showed | What I concluded |
| :---- | :---- | :---- | :---- | :---- |
| 1  | Observation & Conversation | Other Blog Chair | I watched as she uploaded a new submission. She said it takes her at least 30 minutes to download all the photos and resize them, and also fix the text formatting | The main issue is the lack of automated data transformation. Downloading images and reformatting the text by hand makes it tedious |
| 2  | Conversation | Web Committee Director | She said that she wants us to start really getting that twice a week schedule down but the approval process is inefficient since she doesn’t get notified when an upload is ready, only when someone pings her on Slack or she checks the github repo | There is no automated notification system between the blog chairs and our director, and it relies entirely on manual communication |
| 3  | Conversation | General SWE Member  | She said she wrote a summary of the corporate networking event that happened a few weeks ago and hasn’t gotten an update on the post status | Submitters don’t know what’s going on about their posts. They don’t know whether they’ve been approved or rejected which can discourage them from submitting |

## Part 3: What I learned

*Paste this from your draft, then revise it. 1 to 2 sentences each.*

- **What surprised me: I was surprised to find that the biggest time waster wasn’t reviewing all the submissions and checking for quality but the transformation of it from the sheet to the webpage through all the reformatting and copy/pasting. All the images have to be downloaded and resized, while the text needs to be checked for errors then copy pasted.**  
- **What changed in my thinking since Assignment 1: I originally thought it was just an issue with how tedious the system is but the entire thing is pretty broken. Everything from the submission to the approval process can be improved. There is a lack of automation in all the steps, from notifying the director about pending drafts and letting submitters know their post is live.**  
- **My biggest open question: How can we implement an automation system that will be effective but also simple enough for future blog chairs to maintain that manages to connect our intake form, Github, and Slack?**


## Part 4: My course board

*Paste the view link to your copy of the course board. Test it in a private browser window.*

**Board link: [https\://www\.figma.com/board/F77NwWjqF8vPzztFuWx2nl/Diksha---Systems-Thinking-and-AI-Agents---Course-Board--Copy-?node-id=0-1\&t=IHwNLO5ptEQj6cwJ-1](https://www.figma.com/board/F77NwWjqF8vPzztFuWx2nl/Diksha---Systems-Thinking-and-AI-Agents---Course-Board--Copy-?node-id=0-1&t=IHwNLO5ptEQj6cwJ-1)** 

*Sections 2 to 5 should show your updated stakeholder map, human system map, inputs and sources, and iceberg.*

## Part 5: The outcome

*One or two sentences each. Name a thing you could hold up and show someone.*

- **My system will produce: For each blog submission, a ready to be uploaded Markdown file, a folder of resized images, and a drafted Slack message for the director.**  
- **It's for: Me and the other Blog Chairs, so we stop wasting time formatting each post, and the Web Committee Director, so she is notified as soon as a draft is staged.**  
- **They'll use it to: I will upload the Markdown file and images directly to GitHub, and then send the drafted Slack message to the director. She will use the Slack ping to review the GitHub link and approve the post to go live.**  
- **It starts from these inputs: The raw text and Google Drive image links from the submitter's intake form, and the CSS grid dimension rules for our website found on WordPress.**

## Part 6: Quality standards

*3 to 5 rules a good result always meets. Each one has to be checkable: two people checking the same result should get the same answer. Judgment calls go in Part 7, not here.*

| \# | The standard | Where it came from | How I'll check it |
| :---- | :---- | :---- | :---- |
| 1 | Every downloaded image is resized to exactly 800 pixels wide | Research log \#1 (other blog chair) | I will open the image file properties and check the dimensions. Passes if the width is 800 pixels. |
| 2 | The Markdown file's header contains the author's name and the event title spelled as they were in the intake form. | The GitHub repo rules from step 3 of my human system map | I will compare the text in the Markdown file to the original Google Form response spreadsheet. Passes if the spelling and capitalization match. |
| 3 | The output Markdown file has the exact same number of paragraphs as the original form submission text. | Research log \#1  | will count the number of paragraphs in the raw form submission and the output Markdown file. Passes if they’re the same. |
| 4 | The drafted Slack message contains the event title and tags "@Web Committee Director" | Research log \#2 (The Web Committee director) | I will read the drafted Slack message. Passes if both the correct event title and the "@" are present. |

## Part 7: Human decisions

*The calls your system should not make on its own. Look for approvals, sign-offs, and anything someone is held responsible for. Have at least 1\.*

| Decision | Who makes it | Why it stays with a person |
| :---- | :---- | :---- |
| Approving the staged post to go live on the website | Web Committee Director | She is the person responsible for what the club publishes. A system can check formatting, but a human must judge if the content is accurate to the facts and appropriate for the SWE brand. |
| Deciding if the resized images look visually acceptable | Blog Chair | The system can force an image to be exactly 800 pixels wide, but it might look awkward. A person needs to confirm the image looks right before placing it. |
| Evaluating if the writing flows well and makes sense | Blog Chair 1st and Web Committee Director 2nd | Assessing tone and how readable something is subjective. The system can keep the paragraphs, but it cannot determine if the recap is actually a well written summary of the event. |

## Part 8: My first version

*One path through your system, working start to finish. You'll build it in Milestone 3, due Nov 21\.*

- **It takes in: A completed SWE blog intake form submission, including the raw text, author name, event title, and a Google Drive link to the image folder.**  
- **It produces: A fully formatted Markdown file with the correct headers ready for GitHub, and a drafted Slack message for the Web Committee Director.**  
- **The one path I'll build first: A blog submission goes in, and the system converts the raw text into the structure required by our repo, while drafting the Slack notification**  
- **Leaving for later, and why: Automatically downloading and resizing the Google Drive images because dealing with the different sharing permissions is too complex right now, the GitHub pull request integration, because I’m not too sure how to handle the branch management and authorization, and automated email updates to the submitters because it’s not as crucial as the other parts.**  
- **I'll test it on: The 3 past blog submissions from our Google Form spreadsheet that I’ve already manually formatted and published.**

## Part 9: Feedback and what I changed

*At least 2 pieces of feedback from me, your critique group, or the people you talked to. If you didn't change something, say why. That counts too.*

| Feedback | From | What I changed, or why I didn't |
| :---- | :---- | :---- |
| Start by automating just one repetitive task rather than the whole GitHub Actions system to keep things simple. | Tj & Aarnav  | I changed my First Version plan in Part 8\. Instead of trying to build automated GitHub integrations now, I scaled it back to just generating the formatted Markdown text and drafting the Slack message |
| What happens if a submitter's Drive link isn't shared publicly? | Lucia & Aarnav  | I realized that handling blocked Google Drive permissions through an automated script is too much work right now. Because of this, I moved automated image downloading to my "Leaving for later" section. To try and fix the root cause, I will to update the intake form instructions to tell submitters to set their links to "Anyone with the link can view." |

