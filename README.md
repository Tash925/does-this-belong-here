# 🛡️ Does This Belong Here?

**A friendly phishing checker for the people in your life who still get spam.**

Paste in an email or text that feels off, and it walks you through it the way a security analyst would — in plain English, no jargon. One-line verdict, the red flags it spotted *and why each one matters*, and one calm next step. Every answer ends with the question that keeps you safe: **"Does this belong here?"**

Built with [Gemma](https://ai.google.dev/gemma), Google's open-weight model, for the [Hacktoberfest 2026 "Build for a Friend" Weekend Challenge](https://dev.to/challenges/hacktoberfest-weekend-2026-10-01).

> Part of [DataSec Chronicles](https://www.datasecchronicles.com) — storm to SOC, finding what doesn't belong.

---

## Why I built it

My mom knows not to click the link. My husband does too. Most people have picked up the *don'ts* — but nobody ever explained the *why*, and the why is the part that actually protects you when a real scam lands at 11pm looking urgent and official.

This tool closes that gap. It doesn't try to make anyone a security expert. It hands them the **instinct** — the same *"does this belong here?"* question a SOC analyst asks on every alert, pointed at their own inbox.

## What it does

- **Verdict** — "This looks safe," "Be careful — a few red flags," or "This looks like a scam."
- **What I noticed** — the red flags, each with the plain-language reason it matters (the threat behind it).
- **What to do** — one clear, calm next step.
- **Does this belong here?** — the question to carry forward.

No shaming. No jargon. Just a kind, patient explanation anyone can act on.

## How it works

One self-contained HTML file. No build step, no backend, no framework.

1. You paste a suspicious message.
2. The app sends it to **Gemma** with a system prompt that tells it to act as a warm, plain-spoken helper — name the red flags, explain *why* each matters, never shame the person for asking.
3. It returns a clean, structured answer.

The app queries which models your API key can access and automatically picks an available Gemma model, so it keeps working even as model names change.

## Run it yourself

1. Get a free API key from [Google AI Studio](https://aistudio.google.com/apikey).
2. Open `does-this-belong-here.html` in your browser.
3. Paste your key into the setup box, paste in a suspicious email, and hit **Check it for me**.

That's it. Your key stays in your browser — it isn't stored or sent anywhere except to the model.

## Why open innovation matters here

The whole point is to check a **real email** — which often contains personal details, names, account references.

Because Gemma is **open-weight**, this can be *local-first*: the same tool can run entirely on your own machine (via something like [Ollama](https://ollama.com)), so your private emails never have to leave your computer. A closed API can't promise that — "paste your suspicious email here" would mean "send your private email to someone else's cloud."

For a tool built specifically for the people most likely to be targeted by scams, that privacy guarantee isn't a nice-to-have. It's the point.

## Tech

- [Gemma](https://ai.google.dev/gemma) (open-weight) via the Google AI Studio API
- Plain HTML / CSS / JavaScript — one file, no dependencies

## License

MIT — use it, fork it, hand it to someone you love.

---

*the tool changes, the question doesn't. 💜*
