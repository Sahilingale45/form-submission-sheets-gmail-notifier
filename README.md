# form-submission-sheets-gmail-notifier
A real-time automation blueprint that catches form submissions, upserts client records into Google Sheets, and triggers instant Gmail notifications.
# Form Submission Ledger & Gmail Notifier Automation

This repository hosts an integration workflow blueprint designed to process user form responses instantly, catalog them efficiently inside a spreadsheet ledger, and dispatch real-time email notifications.

## 🚀 How It Works
1. **Trigger (On form submission):** Listens via real-time webhooks for inbound data packages immediately after a user clicks submit on your form.
2. **Database Upsert (Google Sheets - Append or update row):** Evaluates incoming submission fields. If a unique matching key is found, it updates the existing row with new info; otherwise, it appends a clean new line entry.
3. **Communication Alert (Gmail - Send a message):** Composes an automated template message embedded with dynamic form tokens and sends it right away as a confirmation receipt or team notification.

## 📦 What's Included
* `/blueprints/form-submission-sheets-gmail-notifier.json`: The complete structural blueprint export configuration file.

## 🔧 Setup Instructions
1. Open your workflow configuration dashboard.
2. Create a new automation scenario, locate the settings or developer control bar, and choose **Import Blueprint**.
3. Upload the `.json` blueprint file matching this repository.
4. Set up your active integration endpoints:
   * **Form Trigger:** Map the webhook URL configuration directly to your active online form builder.
   * **Google Sheets Module:** Authenticate your Google Drive workspace, choose your target directory sheet file, and configure the unique identifier column key to execute upserts safely.
   * **Gmail Module:** Authorize your specific mail handle workspace connection and structure your email templates.
5. Map form fields like `Email Address`, `Full Name`, and `Message Body` fields dynamically down the stream into the downstream modules.
6. Save your progress and activate the automation pipeline toggle to **ON**.
