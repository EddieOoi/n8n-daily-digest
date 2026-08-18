<div align="center">

  <img src="./n8n-hero-banner.svg" alt="n8n Automated Workflow Hero Banner" width="100%" />

  <br/><br/>

  [![n8n Workflow](https://img.shields.io/badge/n8n-Workflow-FF6D5A?style=for-the-badge&logo=n8n&logoColor=white)](https://n8n.io/)
  [![Google Gemini](https://img.shields.io/badge/Google_Gemini-AI_Synthesizer-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white)](https://gemini.google.com/)
  [![Slack Integration](https://img.shields.io/badge/Slack-Daily_Digest-4A154B?style=for-the-badge&logo=slack&logoColor=white)](https://slack.com/)

  An automated backend workflow built with <font color="#FF6D5A"><b>n8n</b></font> that aggregates multi-source daily data (Weather, Google Calendar, News RSS, Notion, and Trello), synthesizes it into a concise briefing using <font color="#8E75B2"><b>Google Gemini AI</b></font>, and delivers a formatted Markdown digest directly via <font color="#4A154B"><b>Slack</b></font>.

---

</div>

### <font color="#FF6D5A">eddie@github</font> ~ $ ./architecture_overview.sh

```text
[ Every Morning 7 AM ] 
          │
          ├───► OpenWeather API ────────┐
          ├───► Google Calendar ────────┤
          ├───► News RSS Feeds ─────────┼──► [ Merge All Data ] ──► [ Format AI Input ] ──► [ Gemini AI ] ──► [ Format Markdown ] ──► [ Slack DM ]
          ├───► Notion Tasks API ───────┤
          └───► Trello REST API ────────┘

```
