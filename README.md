# AI Client Retention Analyzer

A tool for beauty and wellness professionals to identify at-risk clients and automatically generate personalized re-engagement messages using AI.

---

## What It Does

Paste in your client visit history (CSV-style) and the tool:

1. **Classifies each client** as Healthy, At Risk, or Churned based on days since last visit
2. **Shows a retention dashboard** with summary metrics
3. **Writes a personalized re-engagement SMS** for each at-risk or churned client, mentioning their favorite service by name

| Status | Threshold |
|--------|-----------|
| Healthy | < 60 days since last visit |
| At risk | 60–119 days |
| Churned | 120+ days |

---

## Demo

![Demo screenshot](screenshot.png)

---

## Setup

1. Clone the repo
```bash
git clone https://github.com/profarav/client-retention-analyzer
cd client-retention-analyzer
```

2. Add your Anthropic API key in `index.html`:
```javascript
const ANTHROPIC_API_KEY = 'your-key-here';
```

3. Open `index.html` in your browser — no build step, no dependencies.

---

## Example Input

```
Name, Last Visit, Total Visits, Total Spend, Favorite Service
Jessica M., 2024-08-12, 14, $1820, Balayage
Priya K., 2025-02-01, 3, $340, Blowout
Tanya R., 2024-05-30, 22, $3100, Color + Cut
```

## Example Output

```
Jessica M. — Churned (216 days since last visit)
"Hey Jessica! It's been a while since your last balayage — we miss you!
We'd love to have you back. Book this week and we'll take 15% off."
```

---

## Why This Matters 

Most salon owners don't know who's slipping away until it's too late — and writing personalized outreach for every client manually isn't realistic.
This tool is an AI-first approach to that problem: paste your data, get instant retention intelligence and ready-to-send messages. No spreadsheets, no guesswork.

---

## Tech

- Vanilla HTML/CSS/JS — zero dependencies
- Anthropic Claude API (`claude-opus-4-5`) for classification and message generation
- Single file, runs in any browser

---

*Built by [Arav Lohe](https://github.com/profarav)*
