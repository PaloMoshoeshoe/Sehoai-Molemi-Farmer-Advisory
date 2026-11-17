# Molemi Farm Advisor

Voice-first farm advice in Sesotho for smallholder farmers in Lesotho, a working prototype.

Farmers ask a question by chat, by USSD (`*321#`) or on a toll-free voice line. Claude answers in Sesotho or English, using **only** an approved content library. Questions it can't answer safely, and sick or dying animals, go to the district extension officer. Officers get a dashboard that shows open questions, problems that are rising and a weekly brief.

> **Prototype with sample data.** The "approved content" in this repo was written for the demo. It is **not** Ministry-approved, so don't use it for real farming decisions. This prototype supports a proposal to the Ministry of Agriculture, Food Security and Nutrition. It is not an official government service.

**Live prototype:** https://claude.ai/artifact/VLnxtVk3cZPfy71bWwtreB (only people the owner has shared it with can open it)

---

## What's in the prototype

The page has three views, which you switch between with the tabs at the top.

### 1. Farmer's phone
A simulated handset with three channels:

| Channel | What it shows | Reply limit |
|---|---|---|
| **Chat** (WhatsApp-style) | Typed or spoken questions with streamed answers, source chips and a ▶ Listen button | 90 words |
| **USSD `*321#`** | A menu that works on any phone with no data bundle: ask a question, planting calendar, livestock alerts, market prices, message an officer | 160 characters (one screen) |
| **Voice line** | A simulated call. The caller speaks, Claude answers in short spoken sentences, and the answer is read aloud | 60 words |

Next to the phone:
- **Caller profile**: district (all 10 districts of Lesotho), reply language (same as the farmer / Sesotho / English) and answer quality (Fast / Best).
- **How this answer was made**: topic, confidence, whether the question was escalated, and the exact approved passages Claude used.

### 2. Extension officer
A district dashboard you can filter by district and period (7 or 30 days):
- **KPIs**: questions, % answered by Claude, questions waiting for an officer, % that came by voice or USSD.
- **Needs an officer**: the escalation queue. Officers can **Draft with Claude** (an SMS reply of up to 300 characters, grounded in the approved content) and then send it.
- **Rising problems**: the same problem in the same district this week compared with the week before. It is flagged as a *possible outbreak* at 3 or more reports that are at least double the previous week.
- **Questions by topic**: a bar chart.
- **Weekly brief**: Claude drafts a brief of under 180 words with top issues, possible outbreaks, recommended actions and content gaps.
- **Recent questions**: a table, newest first.

### 3. Approved content
The library Claude is allowed to answer from: 18 sample passages (P01–P18) on crops, pests, livestock, soil, weather and markets. Examples are the maize planting windows, fall armyworm, sheep scab, foot rot, worms, wool and mohair quality, ticks, drought and Newcastle disease. In the pilot, these passages would come from Ministry manuals and crop calendars and be signed off by an expert.

---

## How an answer is made

1. The farmer's message, the district, the channel and the last few turns go to Claude with the full approved library.
2. Claude follows these rules:
   - Use only the approved passages. Never add facts, doses, prices, product names or dates that aren't in them.
   - If the passages don't cover the question, or an animal is very sick, send the question to the extension officer and give only the safe steps the passages contain.
   - Reply in the farmer's language (or the one chosen), in simple words, within the channel's length limit.
3. After the reply, Claude returns a small JSON block with `language`, `sources`, `confidence`, `escalate`, `topic`, `keyword` and an English summary. The page uses it for the trace panel, the officer queue and outbreak signals.
4. The page saves each question to a shared `questions` collection so it shows up on the officer dashboard.

**Fields stored per question:** question, English summary, language, district, channel, topic, keyword, answer, passages used, confidence, status (`answered` / `escalated` / `replied`), the officer's reply and timestamps. No names or phone numbers are stored.

---

## Running it

The whole app is one self-contained file, `index.html`, with no build step and no dependencies apart from Google Fonts.

It is designed to run as a **Claude artifact on claude.ai**, which gives the page these runtime capabilities:

| Capability | Used for |
|---|---|
| `sample` | Asking Claude: farmer answers, officer reply drafts, weekly brief |
| `db` | The shared `questions` collection behind the officer dashboard |
| `user` | Checking whether the viewer can save (view-only vs contributor) |
| `dictation` | Speech input on the chat and voice line |
| `tts` | Reading answers aloud |

**Opened elsewhere** (directly in a browser or on GitHub Pages), the page still loads and the content library still shows. The badge reads "Claude unavailable here", though, and answers, saving and voice won't work.

Whether Sesotho speech input works depends on the viewer's browser. If it isn't supported, farmers can type, or switch to English.

---

## Try these

- *"Ke bona liboko tse jang poone ea ka. Ke etse joang?"* (Sesotho: worms are eating my maize)
- *"My sheep are limping and their feet smell bad."*
- *"When should I plant maize in Thaba-Tseka?"*
- *"My goat has a swollen jaw and won't eat."* (this one should be escalated to an officer)

---

## Known limits of the prototype

- All advice content is sample text, not Ministry-approved.
- There are no live market prices or current subsidy rules. The pilot would link to a live price feed.
- No SMS is sent. In the pilot, full answers and officer replies would go out by SMS.
- USSD and the voice line are simulated in the browser, not connected to a mobile network.

## Repository

```
index.html   the complete app (HTML, CSS and JavaScript in one file)
README.md    this file
```
