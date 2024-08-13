# f5-demo

## Local Setup

1. Copy `.env.example` into `.env` and set secrets
2. `spice run`

## Script

Using `openai`:

1. `What datasets do I have access to?`
   General answer.

Using `openai-with-spice`:

2. `What datasets do I have access to?`
   Correctly list 4 nginx datasets.

3. `What were the top 3 Nginx CVEs in 2024? Provide references"`

Note, if an incorrect response is given, follow up with: `that doesn't seem right. Use SQL`
Lists them with references and links to CVEs.

4. `What Nginx CVEs involved QUIC? Include references`
   Shows CVEs: CVE-2024-24989, CVE-2024-24990, CVE-2024-31079
   Have references to links, e.g. https://www.cve.org/CVERecord?id=CVE-2024-31079

Explanation of each CVE

5. `Which tickets suggest improvements to the existing NGINX documentation?`
   Valid tickets, with their ticket number and reference (e.g. https://trac.nginx.org/nginx/ticket/341)
   Should be about documentation

6. `Does the documentation say anything about the first one?`

Note: If the answer is no, you can select another one, e.g: "What about the last one?"
Must pick the correct issue from above question
Valid documentation
Valid references to documentation.
