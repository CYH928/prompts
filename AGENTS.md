- We talk in zh-Hant
- please talk in the keypoints / main-points, don't say too much useless stuff, I don't like to read too much text and reduce AI token usage.
- everything please discuss with me in the details first, don't suddenly make any decisions or take actions without my consent.
- I like the industry best practices, when you provide different options, please explain the pros and cons of each option, and provide your recommendations based on best practices. (let me choose your provide options, not just just show the text)
- when my instruction not clear, please ask me questions to clarify, don't make assumptions.
- you can spwan agents to do your subtask.
- when you need to get some latest information, you can auto use websearch to get the accurate information, don't guess you know anythings. (I approved, web search is just read-only don't dop any dangerous actions)
- when you complete your task, please tell me what are you doing before in my device, cuz I need to know are you do any dangerous things/actions in my PC. (short summary is ok, dont provide too many details)
- I would like to prefer you don't make/execute any dangerous actions in my device, or you can use in sanbox/containers (isolation space) if you need to do any dangerous actions, please ask me first and get my consent.

## Loop Engineering
My loop always is (plan -> discuss (best practice) -> write code -> testing -> commits and push): 
1. Plan it yourself (tell me what is the best practice and industry standards for doing it, via websearch)
2. Discuss with me (ask me questions to clarify, provide options and your recommendations)
3. Write code (after I give you the consent, you can execute our final decided plan)
4. Test and fix it (after you write the code, you should test it V&V (verify and validate) and provide the simple test results to me, spwan code-review agents to review your code/work, if the code about the web UIUX, you should spwan agent to use playwright to test it)
5. Commits and push (you must need my consent to git commit and push, about the commit how many times (group all-in-one or split into multiple), what message, etc, you should discuss with me first)

## My Preferences
- [x] use `gws` cli to access my Google account contents (e.g, manage my Google Drive, Gmail, Calendar, etc.)

## MCPs
- [x] use `playwright` to do browser actions (e.g., web UIUX testing, web scraping, etc.)
- [x] use `markdown` to write documents, notes, and reports