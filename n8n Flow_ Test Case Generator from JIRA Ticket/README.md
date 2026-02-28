**n8n Flow: Test Case Generator from JIRA Ticket**

**Problem Statement:**
Create an n8n workflow where you input a JIRA ticket ID (or requirement text), the workflow fetches the ticket details from JIRA (or accepts text input), sends the requirement to an LLM, and generates functional test cases in a structured table format.

**Context:**
As part of the STLC, QA engineers receive JIRA tickets with feature requirements. They need to quickly generate test cases from these requirements. The workflow should automate the "Requirement → Test Case" step.

**Workflow Requirements:**
1. Use a Chat Trigger where the user types a JIRA ticket ID or pastes requirement text
2. Optionally connect to JIRA using the JIRA node with your API token
3. Pass the fetched JIRA description (or input text) to an LLM node (Groq/Ollama)
4. Use the RICE POT framework in the system prompt: Role=Senior QA Engineer, Output=Table format
5. Add constraints: 'Generate ONLY from the provided requirement. If info is missing, write "Needs clarification"'

**Evaluation Criteria (6 marks):**
- 2 marks for approach (correct node selection and logical flow)
- 2 marks for working flow (successfully processes input and generates output)
- 2 marks for output quality (structured test cases with proper coverage)

**Submission:** Build the workflow in n8n, export or screenshot it, push to GitHub, and submit the repository link.
