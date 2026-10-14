# OWASP Subdomain Monitoring

Project Overview
An automated subdomain monitoring workflow built with n8n. It collects OWASP subdomains, cleans and filters hostname data, uses an AI agent to classify hostnames, assigns review priorities, and generates a structured report for Google Docs.

 Workflow
1. Schedule Trigger – Starts monitoring on a daily schedule.
2. HTTP Request – Retrieves hostname data from the configured API.
3. Code in JavaScript – Cleans and deduplicates hostname records.
4. AI Agent – Classifies hostnames into admin, dev, staging, api, or other.
5. Code in JavaScript1 – Parses AI responses into structured fields.
6. Filter – Keeps hostnames that meet the configured priority threshold.
7. Code in JavaScript2 – Groups hostnames and builds the report.
8. Create a document – Creates a Google Docs report.
9. Update a document – Inserts the generated report into the document.

 Technologies
- n8n workflow automation
- HTTP API integration
- JavaScript
- GPT-4o-mini
- Google Docs

 Setup
1. Import the workflow JSON into n8n.
2. Configure the required AI model and Google Docs credentials.
3. Verify the API endpoint and schedule settings.
4. Test the workflow and confirm that the report is inserted into Google Docs.

 Security and Limitations
Hostname labels and priority scores are preliminary review indicators, not proof of vulnerabilities. The workflow should only be used for authorized monitoring. Review exported workflow files and remove credentials or sensitive information before sharing.

