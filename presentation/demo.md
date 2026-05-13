

As part of Hackathon , we did won location wise, now we need to present the idea to the Leadership team , kinda like demo. 

Idea: Use custom agents(qtest-automator and playwright-generator) and multiple mcp server(jira and playwright) to automate the manual tasks using vscode in sprint which are
1. Problem: Start of sprint developers needs to write manually the test case design steps and it sould be uploaded manually to qTest(centralized place to hold all test cases) which is used by UAT to test.

Solution: qtest-automator agent on giving the message in chat "qTest <JIRANUM1> <JIRANUM2>" will trigger the agent and pull the jira details using jira mcp then these details will be sent to llm model defined in agent or can be selected from git copilot in vscode which understands and gives the testcase design steps, then it is stored in csv(for developer compatibilit) and json(can be uploaded to qTest using API) format then the test case steps gets uploaded to qTest

2. Close to sprint end when development is complete then automation scripts needs to be written manually for automotable(since not all stories can be automated) stories

Solution: playwright-generator agent on giving the message in chat "automate<JIRANUM>" will trigger the agent which orchestrates below out of box agents provided by playwright

 a. planner explores the app and produces a Markdown test plan 
b. generator transforms the Markdown plan into the Playwright Test files 
c. healer executes the test suite and automatically repairs failing tests

for the the playwight to undertsand the application a knowledge base is provided in .md file about the application like which ui framework it uses and all

So to just give the background qTest uploader and solution are provided by others also but it isin webapp where the jira number is provided and then the testcase design is done and it gets uploaded to qTest, but in our solution customization can be done like which model to be used and some additional info can be given.

In our firm few teams uses selenium(which is gettign migrated to cypress), few cypress and few playwright, need some good points on why to use playwright against cypress,selenium. Also keeping AI in mind give the comparisons on mcp, skill which has more advantages.

Now need points on how to start the demo, like pitching idea and and conclue in 7 minutes. 5 minutes for demo and 2 min for QnA




script:


Here’s a tight, 7-minute demo script you can literally follow while presenting.
It’s structured for confidence, clarity, and impact — not too technical, but still impressive.

🎤 🔥 FULL DEMO SCRIPT (7 Minutes)
🟢 [0:00 – 1:15] Opening (Hook + Problem)

“Good morning everyone.

In every sprint, our teams spend a significant amount of time on two repetitive but critical activities:

First — writing detailed test case design steps from Jira stories.
Second — creating automation scripts once development is complete.

These tasks are essential, but they are manual, time-consuming, and often inconsistent across teams.”

👉 Pause (1–2 sec)

“On average, this can take 1–2 hours per story, depending on complexity.

Now imagine if we could reduce this effort to just a few minutes — directly within the developer’s workflow.”

🟢 [1:15 – 2:00] Solution Pitch (High-Level)

“That’s exactly what we built.

An AI-powered agent system integrated into VS Code that automates both test design and test automation — using Jira as the single source of truth.”

“It uses custom agents that:

Understand Jira stories
Generate test cases
Upload them to qTest
And even generate Playwright automation scripts”

“All of this is triggered using simple commands inside VS Code.”

🟢 [2:00 – 4:30] LIVE DEMO – Part 1 (Test Case Automation)

👉 Open Jira ticket

“Let’s start with a typical Jira story.”

👉 Switch to VS Code

Type:

qTest JIRA-101

“With a simple command, our agent is triggered.”

👉 Narrate while running:

“The agent pulls the Jira details using MCP integration, sends the context to the configured LLM, and generates structured test case design steps.”

👉 Show:

CSV file
JSON file

“We generate:

CSV format for developers
JSON format for qTest API upload”

👉 Show qTest UI

“And as you can see, the test cases are automatically uploaded to qTest.”

👉 Strong line:

“What used to take 1–2 hours is now done in under a minute.”

🟢 [4:30 – 6:00] LIVE DEMO – Part 2 (Automation Generation)

👉 Back to VS Code

Type:

automate JIRA-101

“Now let’s move to the end of the sprint — automation.”

“This triggers our Playwright-based multi-agent workflow.”

👉 Explain while showing output:

“It uses three intelligent agents:

Planner → understands the application and creates a test plan
Generator → converts it into Playwright scripts
Healer → runs and auto-fixes failing tests”

👉 Show generated test file

“We also provide a knowledge base about the application, so the agent understands UI structure, frameworks, and flows.”

👉 Strong line:

“This is not just automation — this is self-healing test automation.”

🟢 [6:00 – 6:40] Why Playwright + Architecture Advantage

“Across teams today, we use Selenium, Cypress, and Playwright.”

“We chose Playwright because:

It supports multiple browsers out of the box
Handles modern UI applications better
Has built-in parallel execution
And is highly suitable for AI-driven automation”

“Also, our architecture uses MCP — which allows us to easily integrate with tools like Jira and Playwright in a scalable way.”

👉 Punch line:

“This means we’re not locked into one tool — we can extend this system across teams and technologies.”

🟢 [6:40 – 7:00] Closing (Impact Statement)

“To summarize:

We are reducing manual effort, improving consistency, and accelerating sprint delivery — all within the developer’s existing workflow.”

“And this is just the beginning — the same approach can be extended to regression planning, defect analysis, and beyond.”

👉 Final line:

“We’re not just automating tasks — we’re enabling intelligent development workflows.”

❓ [Q&A Buffer – 2 Minutes]
If asked anything, keep answers SHORT:

👉 Accuracy?

“We keep a human validation step, and results improve with better prompts/models.”

👉 Adoption?

“Very minimal — just simple commands in VS Code.”

👉 Scalability?

“MCP makes it plug-and-play across tools and teams.”

🎯 Delivery Tips (Important)
Speak slightly slower than normal
Pause after key lines
Don’t rush demo — even if small delay, narrate confidently
Smile during opening and closing