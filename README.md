# 🤖 Meetly – AI Meeting Insights & Follow-Up Agent

**Meetly** is a smart, no-code automation agent that uses AI to turn your virtual meeting transcripts into actionable follow-ups. Built with [n8n](https://n8n.io), it automatically summarizes meetings, extracts to-dos per participant, and sends reminders via Email, Slack, or Google Calendar — all without writing a single line of code.

---

## 🚀 Features

- 📄 **Transcript Ingestion** – Accepts transcripts from Google Docs, Notion, or direct webhook input
- ✨ **AI Summarization** – Uses OpenAI to summarize meetings and extract action items
- 🧑‍🤝‍🧑 **Participant-Specific Tasks** – Assigns to-dos to individuals automatically
- 📬 **Follow-Up Reminders** – Sends follow-up tasks via Email or Slack
- 📆 **Calendar Integration** – Syncs deadlines with Google Calendar
- ⚙️ **Built Entirely in n8n** – Visual, drag-and-drop workflow automation

---

## 🧠 Tech Stack

| Tool                  | Purpose                                        |
|-----------------------|------------------------------------------------|
| [n8n](https://n8n.io) | Visual workflow automation platform            |
| [OpenAI GPT-4 API](https://platform.openai.com/) | NLP for summarization and task extraction |
| Google Calendar API   | Task reminders and follow-up scheduling        |
| Slack / Email Nodes   | Send notifications and follow-up summaries     |
| Google Docs / Notion  | Data input via transcripts                     |

---

## 📛 Badges

![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)
![No-Code](https://img.shields.io/badge/built%20with-n8n-brightgreen)
![OpenAI](https://img.shields.io/badge/OpenAI-API-blue)
![Follow-Up Assistant](https://img.shields.io/badge/AI-AutoMeeting%20Assistant-purple)

---

## 🔧 Setup Instructions

### Option 1: n8n Cloud (Recommended)

1. Sign up at [https://n8n.io](https://n8n.io)
2. Import the `.json` workflows from the `/workflows` folder
3. Configure credentials for:
   - OpenAI API Key
   - Google Calendar (OAuth2 setup in n8n)
   - Email/Slack integrations (as needed)
4. Test using a demo transcript file or a Google Doc link

---

### Option 2: Self-Hosted via Docker

```bash
docker run -it --rm \
  -p 5678:5678 \
  -v ~/.n8n:/home/node/.n8n \
  n8nio/n8n

Then open http://localhost:5678, import the workflow JSON, and connect your API keys.

---

## 📁 Project Structure

pgsql
Copy
Edit
AutoMeetMate/
│
├── README.md
├── workflows/
│   ├── summary-workflow.json
│   └── reminder-workflow.json
├── prompts/
│   └── gpt_prompts.md
├── assets/
│   └── screenshots/
├── .env.example
└── deploy/
    └── Dockerfile or railway.json

## 🧪 Sample GPT Prompt

Summarize the following meeting transcript. Then extract all action items, grouped by participant name. Include deadlines if mentioned. Format clearly in markdown or bullet points.
[Paste meeting transcript here]

---

## 🎯 Use Case Example

After a remote team finishes a meeting, a transcript is uploaded to Google Docs. AutoMeetMate reads the transcript, summarizes key decisions, assigns tasks to each participant, and sends reminders via email and calendar — all automatically.

---

## 👥 Target Users

- Remote tech teams & startups
- Freelancers & consultants
- Online educators & bootcamp hosts
- HR & operations managers

---

## 📷 Screenshots

---

## 🔐 Environment Variables

Make sure to set the following environment variables in `.env` or n8n credentials section:

| Variable Name                  | Description                              |
|-------------------------------|------------------------------------------|
| `OPENAI_API_KEY`              | Your OpenAI GPT-4 key                    |
| `GOOGLE_CLIENT_ID`            | OAuth2 Client ID for Calendar API        |
| `GOOGLE_CLIENT_SECRET`        | OAuth2 Client Secret for Calendar API    |
| `SLACK_WEBHOOK_URL` *(opt)*   | Webhook URL to send Slack notifications  |
| `EMAIL_SMTP_USER` *(opt)*     | Email service username                   |
| `EMAIL_SMTP_PASS` *(opt)*     | Email service password or app key        |

> 👉 Copy from `.env.example` and rename to `.env`

Usage in n8n:

In your OpenAI (HTTP Request) node:
1. Set Authorization: Bearer {{ $env.AZURE_OPENAI_API_KEY }}
2. Set api-key and api-version as query params or headers
3. Use {{ $env.AZURE_OPENAI_ENDPOINT }} as the base URL
👉 Replace actual keys with your_api_key_here in your .env.example for security.

---

## 🛡️ Security Reminder

**⚠️ Do NOT commit `.env` or real API keys** to GitHub.  
Add `.env` to your `.gitignore`.

---

## 📚 Documentation

See the [`/docs`](./docs) folder (or wiki) for:

- 🔁 Workflow logic & node-by-node explanation
- ✨ OpenAI prompt variations
- ⚠️ Error handling for API timeouts
- 📅 Google Calendar auth troubleshooting

---

## 📜 License

This project is licensed under the MIT License. See the LICENSE file for full terms.

---

## 🙌 Acknowledgements/Credits

Built with ❤️ by Jigisha Baliyann
Powered by n8n & OpenAI
