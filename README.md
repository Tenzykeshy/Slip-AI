# 🎫 SlipIQ AI — SportyBet Slip Intelligence Engine

> Screenshot your bet slip → Upload → AI analyses every match → Slip Surgery removes weak legs

---

## Features

- 📸 **Screenshot upload** — take a photo of your SportyBet slip, upload it, Claude Vision reads every match automatically
- 🎫 **Booking code decode** — paste your SportyBet booking code, app calls the API directly (works locally, no CORS)
- 📋 **Text paste** — paste slip text from WhatsApp or anywhere
- 🤖 **Batch AI prediction** — every match analysed with Poisson, ELO, xG models
- 🏥 **Slip Surgery** — removes weak legs with one tap, recalculates odds
- 💡 **Better market finder** — AI suggests better markets on the same matches
- 📊 **Expected Value** — shows which legs have positive EV

---

## Setup (5 minutes)

### 1. Clone the repo
```bash
git clone https://github.com/Tenzykeshy/Slip-AI.git
cd Slip-AI
```

### 2. Install dependencies
```bash
npm install
```

### 3. Add your Anthropic API key
```bash
cp .env.example .env
```
Then open `.env` and replace `your_anthropic_api_key_here` with your real key.

Get your key free at: **https://console.anthropic.com/**

### 4. Run the app
```bash
npm run dev
```

App opens at **http://localhost:3000**

---

## How to use

### Option 1 — Screenshot (Recommended)
1. Open SportyBet on your phone
2. Go to your bet slip
3. Take a screenshot (Power + Volume Down)
4. Open SlipIQ on your computer
5. Click **Upload Screenshot** → select the image
6. Tap **Analyse Screenshot**
7. AI reads every match and predicts all legs

### Option 2 — Booking Code
1. In SportyBet app → your slip → Share → Copy Code
2. Paste code in SlipIQ → select your country
3. Tap **Decode Booking Code**
4. Direct API call to SportyBet — no CORS issues locally

### Option 3 — Paste Text
1. Copy your slip details from WhatsApp or anywhere
2. Paste in the text box
3. AI extracts teams, markets, odds from any format

---

## Build for production
```bash
npm run build
```
Output goes to `/dist` — deploy to Vercel, Netlify, or any static host.

> ⚠️ **Security note:** For production deployments, move the Anthropic API calls to a backend proxy so your key is never exposed in the browser.

---

## Tech stack
- React 18 + Vite
- Claude API (claude-sonnet) for Vision + text extraction + match prediction
- SportyBet public booking API (no key needed)
- Zero external UI libraries — custom CSS only

---

⚠️ *AI predictions are statistical models — not guaranteed outcomes. Gamble responsibly. 18+*
