# 📧 Browser Bookmarklets Built with Claude

A collection of single-prompt browser bookmarklets — tiny JavaScript snippets that live in your bookmark bar and do something useful on any page you visit. No installs. No extensions. No code experience required.

Built and shared as part of a LinkedIn series on practical AI automation at work. Each one was generated using Claude's free plan at [claude.ai](https://claude.ai).

**[→ View the live explainer demo](https://[your-username].github.io/bookmarklet-explainer)**

---

## What is a bookmarklet?

A bookmarklet is a browser bookmark that runs JavaScript instead of opening a URL. You drag it to your bookmark bar once, and from then on, clicking it while on any page triggers a small automation — no extension, no login, no setup.

The constraint to know upfront: bookmarklets can read the current page but cannot directly access other apps like Gmail or Slack. For anything that needs to talk to an external service, a Chrome extension is the next step — and Claude can build that too.

---

## The bookmarklets in this collection

### 📧 "did we already fall for this one?"
**The problem:** You land on a vendor's pricing page — another AI tool, another SaaS platform — and can't remember if your team already reached out, did a demo, or got ghosted after three follow-ups.

**What it does:** Reads the current page's domain and opens Gmail in a new window pre-filtered to every thread from or to that domain.

**The prompt:**
```
Create a bookmarklet I can drag to my bookmark bar. When I click it 
on any website, it should open Gmail in a new window filtered to 
emails from or to that site's domain. 
Name it "did we already fall for this one?"
```

---

### 🗓️ Past-date highlighter
**The problem:** You're skimming a Confluence page, a project wiki, or a vendor's roadmap and have no idea which dates have already passed.

**What it does:** Scans the current page for any dates and highlights everything in the past in amber. Instant stale-content scan.

**The prompt:**
```
Create a bookmarklet that scans the current page for any dates in 
common formats (Month DD YYYY, MM/DD/YYYY, etc.) and highlights 
any that have already passed in a bright amber color.
Name it "flag old dates"
```

---

### ✅ Unassigned action finder
**The problem:** You just sat through a meeting, someone dropped notes in Confluence, and now no one knows what's actually assigned to them.

**What it does:** Scans the current page for lines containing "TBD", "?", or text with no @mention and outlines them in red. One click to see exactly what's unowned.

**The prompt:**
```
Create a bookmarklet that scans the current page for any line or 
paragraph containing "TBD", a standalone "?", or text that has no 
@ symbol (indicating no one is assigned). Highlight those sections 
with a red left border and a light red background.
Name it "find unassigned"
```

---

### 🔖 "Read later" dropper
**The problem:** You're reading an article or newsletter and want to save it, but you don't want to set up yet another read-later app.

**What it does:** Opens a Gmail compose window pre-filled with the current page's title and URL, addressed to yourself, so you can drop it into any label you already use.

**The prompt:**
```
Create a bookmarklet that opens a Gmail compose window addressed to 
my own email, with the subject line set to the current page title 
and the body containing the current page URL. 
Name it "save to read later"
```
> Update the prompt with your actual email address before using.

---

### 🔢 Jira row numbering
**The problem:** During standups, your Jira board gets sorted by status and no one can quickly find the story they're giving an update on by position.

**What it does:** Injects a sequential row number next to each story card in any Jira board or backlog view. Reload the page to reset.

**The prompt:**
```
Create a bookmarklet that adds a sequential row number to the left 
of each issue row in a Jira board or backlog view. The numbers 
should appear in a small muted badge. It should work on any Jira 
cloud URL.
Name it "number Jira rows"
```

---

## How to install any bookmarklet

1. Claude will give you a line of code starting with `javascript:`
2. Create a new bookmark in your browser (any page, any name)
3. Edit the bookmark and paste the `javascript:` code into the **URL field**
4. Rename it to whatever you like
5. Done — click it on any page

---

## Tips for prompting Claude

- Be specific about **what page or app** it should work on
- Tell it exactly **what you want it to look for** (text, dates, URLs)
- Tell it **what to do with what it finds** (open a window, highlight, inject text)
- Give it a **name** — Claude will include it in the bookmark label
- If it doesn't work quite right, just say what's wrong and ask it to fix it

Claude's free plan at [claude.ai](https://claude.ai) handles all of these. No subscription needed.

---

## When to graduate to a Chrome extension

Bookmarklets are great for read-only page manipulation and opening filtered URLs. You'll need an extension when you want to:

- Show an overlay with live data from another app (Gmail, Slack, Jira)
- Run automatically on page load without clicking
- Store state or settings across sessions
- Communicate with an external API

Claude can scaffold a Chrome extension from a plain English description. Ask it to start with a `manifest.json` and a `content.js` and go from there.

---

## Contributing

Found a useful bookmarklet? Open a PR with the name, the problem it solves, and the prompt that built it.

---

## License

MIT. Use freely, share freely, remix freely.
