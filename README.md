<div align="center">

  <img src="./n8n-hero-banner.svg" alt="n8n Automated Workflow Hero Banner" width="100%" />

  <br/><br/>

  [![n8n Workflow](https://img.shields.io/badge/n8n-Workflow-FF6D5A?style=for-the-badge&logo=n8n&logoColor=white)](https://n8n.io/)
  [![Google Gemini](https://img.shields.io/badge/Google_Gemini-AI_Synthesizer-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white)](https://gemini.google.com/)
  [![Slack Integration](https://img.shields.io/badge/Slack-Daily_Digest-4A154B?style=for-the-badge&logo=slack&logoColor=white)](https://slack.com/)

  <p align="center">
    <b>An automated backend workflow engineered to synthesize multi-source daily intelligence into actionable Slack briefs.</b>
  </p>

</div>

---

### ⚡ System Architecture

```text
               ┌────────────────────────┐
               │  OpenWeather API      │
               ├────────────────────────┤
               │  Google Calendar       │
 ⏰ Every Morning ──►  News RSS Feeds      ├───► [ Merge JSON ] ──► [ Gemini 2.5 AI ] ──► [ Markdown Parser ] ──► [ Slack DM ]
    7:00 AM    ├────────────────────────┤
               │  Notion Tasks API      │
               ├────────────────────────┤
               │  Trello REST API       │
               └────────────────────────┘
```
<!-- Tech Stack & Integrations Header -->
<h2>🛠️ Tech Stack & Integrations</h2>

<p>Below is a breakdown of the key architecture milestones and technical insights gained while building this workflow:</p>

<!-- Key Achievements Callout Section -->
> [!NOTE]
> ### 🚀 Key Achievements
> 
> * **Multi-Source Data Aggregation:** Designed parallel API execution branches to cleanly merge 5+ disparate endpoints into a single unified JSON payload.
> * **Trello REST API Filtering:** Dynamically resolved board structures, isolated targeted list IDs (`🎯 To do`), and filtered card metadata using custom JavaScript algorithms inside n8n Code nodes.
> * **Resilient Pipeline Architecture:** Implemented `Continue On Fail` logic across all data-fetching endpoints to ensure network drops or dead APIs gracefully output fallback notifications instead of breaking downstream AI/Slack delivery.
> * **AI Synthesis & Dual Formatting:** Engineered Gemini AI prompts to deliver an engaging conversational intro while programmatically maintaining distinct list structures for Notion Tasks and Trello To-Do Cards.

<br />

<!-- What I Learned Code Section -->
### 💡 Core Takeaways

```typescript
interface DeveloperLearnings {
  n8nWorkflow: "Mastered parallel branch orchestration, custom code data transformation, and state handling across complex workflow nodes.";
  apiIntegration: "Handled custom REST endpoints, authentication keys, dynamic URL parameters, and list/board metadata extraction.";
  promptEngineering: "Optimized LLM context windows to strictly enforce word limits, tone constraints, and structural output formats.";
  markdownParsing: "Built custom JS formatting scripts tailored specifically to Slack's block and Markdown rendering engine.";
}
