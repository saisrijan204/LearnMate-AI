# Deployment guide

1. Visit https://script.google.com and create a project named LearnMate AI.
2. Paste `Code.gs` into the code editor.
3. Add a new HTML file named `index` (Apps Script will create `index.html`) and paste the supplied interface.
4. Save. Select `setupProject` and click Run. Approve permissions. The script creates the Google Sheet and stores its ID.
5. Open Project Settings > Script Properties and add:
   - Property: `GEMINI_API_KEY`
   - Value: your Gemini API key from Google AI Studio.
6. Deploy > New deployment > select Web app.
   - Execute as: Me (recommended for this simple setup)
   - Who has access: select the narrowest audience that works for your demo. Public access can cause abuse and API charges/quota usage.
7. Deploy and open the web app URL. Test all three modes.
8. Use the screenshots of the real running app in the report. The provided report has screenshot placeholders to replace with real screenshots after deployment.

## Troubleshooting
- Missing key: check Script Properties and redeploy if necessary.
- API errors: verify the key, model access, quotas and API configuration.
- Logging: run `setupProject()` again if the spreadsheet ID property was removed.
