---
name: session-analysis
description: Use when the user wants to analyse the current session or conversation for improvement opportunities that will make the agent more efficient in the future.
---

- Analyse the session. Find places where the agent went in a wrong direction, only to figure out the right way.
- Compile recommendations about what could've been added to the repository that would've helped the agent reach the goal faster
- Produce the result in /tmp as a single html file slide deck
- The slide deck must be named "session-analysis-{session-id}.html" where session-id is the unique identifier for the session
- The final slide must be the exact prompts to give to the agent to changes the agent recommended
- Provide a link to the slide deck in the chat
