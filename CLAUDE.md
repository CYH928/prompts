# CLAUDE.md

## Role
- **Who am I**: I am XXX
- **Born**: 
- **Email**: 
- **My role**: 

## Communication
- **Language**: zh-Hant
- **Response**: 
    - our chat, can you reply me in **short** (main-ideas/keypoints), don't write a long report to me.
    - don't say too much useless stuff, I don't like to read too much text.
    - try to **reduce AI token/usage**.
- **Decisions**: 
    - please use **web search** to find and recommend the accurate latest **best practices or industry standards** to me. (I prefer you)
    - when you need to make any decisions, please **discuss with me** first, don't suddenly make any decisions or take actions by yourself.
    - when you provide different options, please ***explain the pros and cons*** of each option, and ***provide your recommendations*** based on best practices + industry standards for the situation.
        - provide options in menu to let me easy to choose, not show the options in text message.
- **Clarification**: 
    - when my instruction/prompt is not clear, please **ask me some questions to clarify** for you.
    - **don't guess anything you know**.

## Actions Constraints
- **DON'T execute/do any dangerous actions** in my device, vm, cloud, or any other local/remote environment ***without my consent***.

---

## Hooks

### Completed
- when you complete your task, please tell me what are you doing above in my device (cuz I want to know: does you doing any dangerous actions in my device)
    - short summary is ok, dont provide too many details

## Agents
- you can **spawn** any different role (do/modify/review) **subtask agents** to assist with your main task.

## Loop Engineering (for coding tasks)
My loop always is (plan -> discuss (best practice) -> write code -> testing -> commits and push): 
1. **Plan it yourself** (tell me what is the best practice and industry standards for doing it, via websearch)
2. **Discuss and decide** with me (ask me questions to clarify, provide options and your recommendations)
3. **Write code** (after I give you the consent, you can execute our final decided plan)
4. **Test and fix** (after you write the code, you should V&V (verify and validate) and self test to provide the simple test results to me, spwan code-review agents to review your code/work, if the code about the web UIUX, you should spwan agent to use playwright to test it)
5. **Commits and push** 
    - MUST need my consent to git commit and push
        - after modify, not equal you can auto commit without my consent 
    - commit how many times: ask me every time (group all-in-one or split into multiple)
        - please commit in bulk, don't commit one by one file
    - for CLAUDE: you NEVER add youself of `Co-Authored-By` in commit message!
6. **Deploy and rollout** 
    - need my consent
    - sometime no need to rollout

---

## AI Tools

### Basic
- `web search/fetch`: when you need to get any latest information, you can auto use websearch tools to get the accurate information (don't follow your memory/out-of-date knowledge)
- `code-review`

### Plugins
- [x] `playwright`: to do browser actions (e.g., web scraping, web UIUX testing, etc.)

### MCPs
- [x] `markitdown`: convert different file types to mardown.

### Custom
- [x] `gws` cli: to access my Google account services (e.g, Google Drive, Docs, Gmail, Calendar, etc.)