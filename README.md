# Timewave Life Story Simulator
### Mobile-First Viral Futures | Built for Replit

---

**Timewave** is a lightweight Flask app that simulates your 1, 5, and 10-year futures based on **3 habits**, **3 principles**, **1 past choice**, and **1 social behavior** — generating gamified narratives, viral MP4s, and crypto-inspired leaderboards.

Built for **founders, dreamers, and grinders** radiating 0.000000001% founder energy (March 12, 2025) and *Simpsons*-level storytelling (April 10, 2025).

---

## ✨ Core Features
- **Ultra-Viral Mechanics**  
  Memeable MP4 clips (🪙🚀💎😎), streaks, rare badges, referrals, X auto-posts.
- **Zero Typing UX**  
  Tap-only dropdowns + ML-like auto-suggestions (DeepSeek, Vertex AI).
- **Mobile-First UI**  
  Optimized for touch screens. Neon blue (`#007BFF`) and purple (`#6F42C1`) dynamic glow.
- **Narrative Engine**  
  DeepSeek + OpenAI + Vertex AI generate life stories and alternate realities.
- **Recursion & Inversion Engines**  
  Track 10 latest entries, prune the rest. Flip to "gritty reality" mode 1x/minute.
- **Viral Growth Loops**  
  Referrals, daily/weekly quests, XP streaks, leaderboard flex.
- **Security by Design**  
  All API keys stored safely in Replit Secrets.

---

## 🛠️ Tech Stack
| Layer        | Technology                |
|--------------|----------------------------|
| Frontend     | HTML5, TailwindCSS          |
| Backend      | Python (Flask)              |
| Database     | SQLite3 (local lightweight) |
| APIs         | OpenAI, DeepSeek, Vertex AI |
| Serverless   | Google Cloud Functions (placeholder) |
| Deployment   | Replit-Ready (1-click run)   |

---

## ⚡ Quickstart (Replit)

1. Fork this repo to your Replit.
2. Add the following secrets:
    - `OPENAI_API_KEY`
    - `DEEPSEEK_API_KEY`
    - `VERTEX_AI_KEY`
3. Click **Run**.
4. Open your mobile device, start tapping, build your future.

---

## 🔥 How It Works

### Inputs:
- 3 Habits (dropdown + frequency: daily/weekly/monthly)
- 3 Principles (dropdown)
- 1 Past Choice (dropdown or short text)
- 1 Social Behavior (dropdown)

---

### Database (SQLite3)
- `users` (id, timestamp, inputs, tokens)
- `inversion_log` (user_id, timestamp)
- `streaks` (user_id, streak_count)
- `quests` (user_id, quest_type, completed)
- `referrals` (user_id, referred_id)

**Auto-prunes to last 10 entries:**
```sql
DELETE FROM users WHERE id NOT IN (
  SELECT id FROM users ORDER BY timestamp DESC LIMIT 10
);

 
