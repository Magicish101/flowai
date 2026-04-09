# FlowAI 🧠
### An AI-powered procrastination coach for teens

FlowAI helps you manage time by detecting emotional bias in how you pick tasks, explaining the neuroscience behind procrastination, and using AI to give you personalised nudges.

---

## 🚀 Step 1 — Put FlowAI on GitHub Pages

This makes your app live at a real URL, which is required for Google Calendar to work.

1. **Create a GitHub account** at [github.com](https://github.com) if you don't have one
2. **Create a new repository**
   - Click the **+** icon (top right) → **New repository**
   - Name it exactly: `flowai`
   - Set visibility to **Public**
   - Leave everything else as default → click **Create repository**
3. **Upload the files**
   - Click **Add file** → **Upload files**
   - Drag in all three files: `index.html`, `README.md`, `_config.yml`
   - Scroll down → click **Commit changes**
4. **Enable GitHub Pages**
   - Go to your repo's **Settings** tab
   - Click **Pages** in the left sidebar
   - Under **Source** → select **Deploy from a branch**
   - Branch: **main** · Folder: **/ (root)** → click **Save**
5. **Your app is live!**
   - After about 1 minute, visit: `https://YOUR-USERNAME.github.io/flowai`
   - Bookmark this URL — it's your FlowAI app

---

## 📅 Step 2 — Connect Google Calendar (optional, ~10 min)

This lets FlowAI import your Google Calendar events as tasks automatically.

### 2a — Google Cloud setup

1. Go to [console.cloud.google.com](https://console.cloud.google.com) and sign in
2. Click the project dropdown (top left) → **New Project** → name it `FlowAI` → **Create**
3. Go to **APIs & Services** → **Library** → search **Google Calendar API** → click it → **Enable**
4. Go to **APIs & Services** → **OAuth consent screen**
   - User type: **External** → **Create**
   - App name: `FlowAI`
   - User support email: your email
   - Developer contact: your email
   - Click **Save and Continue**
   - Click **Add or Remove Scopes** → search `calendar.readonly` → check it → **Update** → **Save and Continue**
   - Click **Add Users** → add your own Google email → **Save and Continue**
5. Go to **Credentials** → **Create Credentials** → **OAuth Client ID**
   - Application type: **Web application**
   - Name: `FlowAI`
   - Under **Authorised JavaScript origins** click **Add URI** and paste:
     ```
     https://YOUR-USERNAME.github.io
     ```
     (replace YOUR-USERNAME with your actual GitHub username)
   - Click **Create**
6. A popup shows your **Client ID** — copy it (looks like `123456789-abc.apps.googleusercontent.com`)

### 2b — Paste your Client ID into FlowAI

1. Open your FlowAI app at `https://YOUR-USERNAME.github.io/flowai`
2. Click the **Google Cal** button in the top navigation
3. The setup guide opens — paste your Client ID into the box at step 7
4. Click **Connect →**
5. A Google sign-in popup appears — sign in and allow access
6. Your calendar events for the next 30 days will appear for review — choose which ones to import as tasks

> **Your Client ID is saved in your browser** — you never need to paste it again on the same device.

---

## 🔒 Privacy

- Your calendar data goes **directly from Google to your browser**
- FlowAI has **no server** — nothing is sent or stored anywhere except your own device
- Your tasks are stored in your browser's `localStorage`
- The Google Client ID is public by design — Google secures it by only allowing requests from your authorised URL

---

## ✨ Features

| Feature | Description |
|---|---|
| **AI Prioritisation** | Tasks ranked by urgency, importance and effort |
| **Smart Scheduling** | Fits tasks into your actual free time windows |
| **Procrastination Tracker** | Detects effort avoidance, easy-first bias, repeat delays |
| **Brain Science** | Explains the neuroscience behind each pattern |
| **AI Coach** | Claude AI gives personalised nudges based on your tasks |
| **Google Calendar Sync** | Imports events as tasks automatically |
| **Monthly Calendar** | All tasks shown on a visual calendar |
| **Weekly Setup** | Set your free hours each day before the week begins |

---

## 🛠 Tech

- Pure HTML + JavaScript — no frameworks, no build step
- [Claude API](https://anthropic.com) for AI coaching
- Google Calendar API + Google Identity Services for calendar sync
- Browser `localStorage` for data persistence
- Works as a Progressive Web App (PWA) — installable on desktop and mobile via Chrome

---

## 🏆 Built for

TAI Challenge — Teens in AI · Spring 2026 · VibeApp category
