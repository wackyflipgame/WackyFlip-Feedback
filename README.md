# 🐞 WackyFlip-Feedback

**Embedded Feedback & Bug Reporting System for Wacky Flip**

`WackyFlip-Feedback` is a lightweight, user-friendly tool that allows players to **submit feedback, bug reports, and feature requests** directly from [wackyflip.com](https://wackyflip.com). All submissions are funneled into internal **support/dev dashboards** for quick triage and resolution.

---

## 🎯 Features

| Feature                  | Description                                                             |
| ------------------------ | ----------------------------------------------------------------------- |
| 📝 In-Game/Site Form     | Embed feedback & bug report form into any Wacky Flip page               |
| 📎 Screenshot Support    | Players can attach images/screenshots for better context                |
| 🛠 Category Filters      | Tag reports as bugs, feedback, feature requests, or questions           |
| 📍 Auto-Context Capture  | Automatically logs browser/device info, page URL, and game state        |
| 🚦 Priority Flags        | Players can indicate urgency of reports                                 |
| 🔔 Dashboard Integration | Sends submissions to support & dev dashboards (Jira, Trello, or custom) |
| 📧 Email/Webhook Alerts  | Notifies relevant team members in real-time                             |

---

## 🛠 Tech Stack

* **Frontend:** React + TailwindCSS
* **Backend:** Node.js + Express / Serverless Functions
* **Storage:** MongoDB / Firebase / PostgreSQL (configurable)
* **Integrations:** Slack, Discord, Jira, Trello, or internal dev tools
* **File Handling:** AWS S3 / WackyFlip-CDN for screenshot uploads

---

## 📁 Repository Structure

```
WackyFlip-Feedback/
├── components/
│   ├── FeedbackForm.tsx
│   ├── ScreenshotUploader.tsx
│   ├── CategorySelector.tsx
│   └── ConfirmationModal.tsx
├── pages/
│   └── api/
│       └── submit-feedback.ts
├── utils/
│   └── contextCapture.ts
├── styles/
├── public/
└── README.md
```

---

## 🚀 Getting Started

1. Clone the repo:

```bash
git clone https://github.com/wackyflipgame/WackyFlip-Feedback.git
cd WackyFlip-Feedback
npm install
```

2. Add environment variables in `.env.local`:

```
FEEDBACK_DB_URI=your-database-url
FEEDBACK_WEBHOOK_URL=optional-webhook
```

3. Start the dev server:

```bash
npm run dev
```

4. Embed the feedback widget:

```tsx
import FeedbackForm from '@/components/FeedbackForm';

<FeedbackForm gameId="flip-bottle" />
```

---

## 📬 Contribution Guidelines

* Keep forms minimal but informative — user convenience first
* Validate input and sanitize file uploads
* Ensure **mobile responsiveness** for in-game overlay feedback
* Test webhook integrations before deploying live

---

## 🔗 Related Repositories

* [`WackyFlip-Support`](https://github.com/wackyflipgame/WackyFlip-Support) – Main support center UI & ticket tracking
* [`WackyFlip-Monitor`](https://github.com/wackyflipgame/WackyFlip-Monitor) – Logs and diagnostic tools for reported bugs
* [`WackyFlip-Docs`](https://github.com/wackyflipgame/WackyFlip-Docs) – Developer documentation for feedback API

---

## 📜 License

MIT © 2025 Wacky Flip Studios track *how often* feedback is submitted and *which issues* appear most. That way, you’ll have real data to prioritize fixes.
