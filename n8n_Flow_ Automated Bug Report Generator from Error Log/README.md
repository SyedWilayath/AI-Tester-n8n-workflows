**Problem Statement:**
Build an n8n workflow that automatically generates structured bug reports whenever new error entries appear. The workflow should read error log data, send it to an LLM to generate a formatted bug report (Title, Severity, Steps to Reproduce, Expected vs Actual Result), and output the result.

**Context:**
Your QA team receives daily error logs from the application's monitoring system. Currently, testers manually read logs and write bug reports. You need to automate this process using n8n.

**Workflow Requirements:**
1. Use a Manual/Chat Trigger node to accept error log text as input
2. Connect to an AI Agent or LLM node (use Groq with llama-3.3-70b-versatile or any free model)
3. Define the LLM system prompt with the role of 'QA Engineer' and specify the exact bug report format
4. Add anti-hallucination constraint: 'Use ONLY the log data provided. Mark unknown fields as [UNKNOWN]'
5. Output the structured bug report via a 'Respond to Chat' or 'Set' node
