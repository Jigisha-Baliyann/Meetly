# Meetly 🤖📅
## AI-powered Meeting Insights & Follow-up Automation System

---

## 📝 About the Project

**Meetly** is a virtual AI assistant that automates meeting follow-ups by:
- Generating key point **summaries** from meeting transcripts
- Creating **personalized to-do lists** for participants
- Sending follow-ups **automatically** to **Telegram** and **Discord**
- Scheduling action items **directly on Google Calendar**

This project was built using **n8n** automation platform integrated with **Together.ai** language models, along with Google Calendar, Discord, and Telegram APIs.

---

## 🚀 Features

✅ Automatic **meeting summaries**  
✅ Personalized **to-do lists** for participants  
✅ Direct **Google Calendar** event creation  
✅ **Discord** notifications  
✅ **Telegram Bot** notifications  
✅ Fully **automated** workflow → Zero manual intervention

---

## 🏗️ Built With

- **n8n** - Low-code automation platform
- **Together.ai API** - LLM used for summarization (Mixtral-8x7B)
- **Google Calendar API** - For meeting events and to-dos
- **Discord Webhooks** - For team notifications
- **Telegram Bot API** - Personal notifications

---

## 📊 Workflow Overview

1. **Trigger** → Scheduled execution (via n8n Cron trigger)
2. **Get Meetings** → From Google Calendar
3. **Summarize Meeting** → Using Together.ai API (Mixtral-8x7B model)
4. **Create To-Do** → New event created on Google Calendar (optional)
5. **Send Notifications** → Telegram & Discord with meeting summary + tasks

![final-workflow](https://github.com/user-attachments/assets/16ff53aa-2044-4989-9508-f69a100423bf)

---

## 📛 Badges

![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)
![No-Code](https://img.shields.io/badge/built%20with-n8n-brightgreen)
![OpenAI](https://img.shields.io/badge/OpenAI-API-blue)
![Follow-Up Assistant](https://img.shields.io/badge/AI-AutoMeeting%20Assistant-purple)

---

## 📂 Project Structure

```Meetly/
├── Meetly.json # Exported n8n workflow
├── Meetly-Demo.mp4 # Demo video of the project
├── README.md # This file
└── Meetly-Presentation.pptx # Project presentation
```

---

## ⚙️ How to Run Locally

1. Clone this repository:
```bash
git clone https://github.com/Jigisha-Baliyann/Meetly.git
```

2. Import the "meetly-workflow.json" into your n8n instance.

3. Configure your credentials:
- Together.ai API Key → https://together.ai/settings/api-keys
- Google Calendar API OAuth
- Discord Webhook URL
- Telegram Bot Token

4. Activate the workflow → Run → Sit back and relax.

---

## 🎥 Demo Video

Check the demo here https://drive.google.com/file/d/1VrpnGjl-uoV41gPbvpAQh6IC1ARUbmDC/view?usp=sharing

---

## 📜 License

This project is licensed under the Licensed under the [MIT License](https://opensource.org/licenses/MIT). See the [LICENSE](https://github.com/Jigisha-Baliyann/Meetly/blob/main/LICENSE) file for full terms.

---

## 🙌 Credits

Built with ❤️ by [Jigisha Baliyann](https://github.com/Jigisha-Baliyann)  
Powered by [n8n](https://n8n.io) and [OpenAI](https://openai.com)
