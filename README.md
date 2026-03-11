# 🏛️ مجلس المحاسبة الاحترافي العالمي — AI Chat

> **AI Assistant — Powered by المجلس الأعلى للشؤون المحاسبية**

A production-ready AI chat interface powered by Claude Opus, embodying the Global Professional Accounting Council.

## 🚀 Deploy to Vercel (One Click)

### Step 1: Prepare your repository

```bash
# Clone or download this project
git init
git add .
git commit -m "Initial commit: Accounting Council AI Chat"

# Push to GitHub
gh repo create accounting-council-chat --public
git push -u origin main
```

### Step 2: Deploy on Vercel

1. Go to [vercel.com](https://vercel.com) → **Add New Project**
2. Import your GitHub repository
3. Framework preset: **Next.js** (auto-detected)
4. Click **Deploy** — Vercel will build automatically

### Step 3: Add your API Key (CRITICAL)

After deployment:
1. Go to your project on Vercel Dashboard
2. Click **Settings** → **Environment Variables**
3. Add new variable:
   - **Name:** `ANTHROPIC_API_KEY`
   - **Value:** `sk-ant-api03-your-key-here`
   - **Environment:** Production, Preview, Development (check all)
4. Click **Save**
5. Go to **Deployments** → Click the 3 dots on latest → **Redeploy**

Your API key is at: https://console.anthropic.com/

---

## 💻 Local Development

```bash
# 1. Install dependencies
npm install

# 2. Create environment file
cp .env.example .env.local

# 3. Add your API key to .env.local
# ANTHROPIC_API_KEY=sk-ant-api03-xxxx

# 4. Run development server
npm run dev

# 5. Open http://localhost:3000
```

---

## 📁 Project Structure

```
accounting-council-chat/
├── app/
│   ├── api/
│   │   └── chat/
│   │       └── route.ts          # API route (hides API key)
│   ├── globals.css               # Dark luxury theme
│   ├── layout.tsx                # SEO + fonts
│   └── page.tsx                  # Main page
├── components/
│   ├── Chat.tsx                  # Main chat logic
│   ├── ChatMessage.tsx           # Message with markdown
│   ├── ChatInput.tsx             # Input with streaming stop
│   └── Sidebar.tsx               # Session history
├── lib/
│   ├── system-prompt.ts          # Full council system prompt
│   └── types.ts                  # TypeScript types
├── .env.example                  # Environment template
├── vercel.json                   # Vercel configuration
└── package.json
```

---

## ✨ Features

- 🔱 **Full Council System Prompt** — All 19+ accounting firms, 18 expert members
- ⚡ **Real-time Streaming** — Token-by-token response display
- 💬 **Chat History** — Persisted in localStorage
- 📋 **Copy Messages** — One-click copy
- 🔄 **Regenerate** — Re-run last response
- 🗑️ **Clear Chat** — Reset conversation
- 📱 **Fully Responsive** — Mobile, tablet, desktop
- 🌙 **Dark Mode** — Luxury dark theme by default
- 📝 **Markdown Support** — Tables, code, headings, bold, RTL
- 🔒 **Secure** — API key never exposed to client
- 🚀 **Vercel Ready** — One-click deployment

---

## 🔧 Technical Stack

| Layer | Technology |
|-------|-----------|
| Framework | Next.js 15 (App Router) |
| Language | TypeScript |
| Styling | Tailwind CSS |
| AI | Anthropic Claude Opus (`claude-opus-4-6`) |
| Streaming | SSE (Server-Sent Events) |
| Fonts | Cormorant Garamond + DM Sans |
| State | React useState + localStorage |
| Markdown | react-markdown + remark-gfm |

---

## 🛡️ Security

- ✅ API key stored server-side only (env variable)
- ✅ All Claude API calls go through `/api/chat` route
- ✅ No API key in client bundle
- ✅ Request validation before forwarding to Anthropic

---

Built with ❤️ for the Global Professional Accounting Council
