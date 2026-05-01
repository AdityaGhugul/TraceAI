# TraceAI
AI log analyzer built for enterprise use cases where data privacy actually matters.

The core problem I kept running into — log traces in production apps contain PII. Customer emails, IP addresses, auth tokens, UUIDs. Standard AI tools are off-limits for this data.

What I built (one holiday weekend):

🔒 PII Redaction Layer
Regex pipeline that strips emails, IPs, JWTs, phone numbers, card numbers, UUIDs before the log ever leaves your browser. AI only sees anonymized data.

🤖 AI Root Cause Analysis
Paste any stack trace → get structured output: root cause, error chain, numbered fix steps, prevention tips.

💬 Contextual Follow-ups
Full conversation history maintained — ask "how do I fix this?" or "could this cause a memory leak?" and the AI has full context.

Stack: Vanilla JS, Anthropic Claude API, deployed on Netlify. No backend, no database, no tracking.

🔗 Live: https://trace-debug-aibot.netlify.app/

Next step I'm exploring: replacing the API call with a local LLM (Ollama) so logs never leave the internal network at all — full air-gap privacy.

Open to thoughts from anyone working on developer tooling or enterprise AI.
