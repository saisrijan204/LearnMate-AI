# LearnMate AI — SDG 4 Capstone

A simple AI-powered study assistant that supports students with topic explanations, quiz generation, and summaries.

## Files
- `Code.gs`: Google Apps Script server/backend
- `index.html`: Web app interface
- `Setup_Guide.md`: Deployment steps
- `Capstone_Report.docx` / `.pdf`: project report

## Stack
Google Apps Script + Gemini API + Google Sheets + HTML/CSS/JavaScript.

## Setup
1. Open https://script.google.com and create a new Apps Script project.
2. Replace the default `Code.gs` with the supplied `Code.gs`.
3. Create a file named `index.html` and paste in the supplied HTML.
4. Run `setupProject()` and authorize access. It creates a logging spreadsheet and stores its ID in Script Properties.
5. In Project Settings > Script Properties, add `GEMINI_API_KEY` with your Gemini API key. Do not put the key in frontend HTML.
6. Deploy > New deployment > Web app. Choose an appropriate execution setting and access option for your intended audience. Be careful: public access may expose the app and consume your API quota.
7. Open the deployed URL and test Explain, Quiz, and Summary modes.
8. Capture screenshots of the actual deployed app for the submission.

## Security and limitations
- Keep API keys server-side in Script Properties.
- Public deployment can create API usage and abuse risks. Restrict access where possible, monitor quotas, and never share the key.
- Sheets and Apps Script are suitable for a prototype, not high-scale production.
- Responses may be inaccurate; students should verify them against course materials.
