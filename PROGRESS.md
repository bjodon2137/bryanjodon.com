# Progress Log

Running log of autonomous work on bryanjodon.com. One entry per change, newest first.

---

### 2026-06-26 — Full voice/copy rewrite pass across homepage, articles, and reference pages
**Files:** `index.html`, `articles/index.html`, `articles/what-is-disc.html`, `articles/giving-feedback-by-style.html`, `articles/d-vs-c-at-work.html`, `articles/i-vs-s-at-work.html`, `disc-explanations.html`, `disc-analogies.html`, `disc-call-stages.html`
**What:** Applied a 10-file copy deck (produced by a prior content-review pass) across the whole site: removed em-dashes from visible body text, cut AI-tell phrases ("load-bearing," "seamlessly," etc.), tightened restate-the-closer habits, and varied sentence length, all via exact-string Python replacements guarded by `assert count==1` so only text nodes changed, never markup. `/call-flow.html` was left untouched per the deck (its script data and the call-stages page quote it verbatim). On the three reference pages, only narrative wrapper text changed; the 20-item DISC content arrays and the call-stages page's quoted script lines/"Watch for" notes are untouched reference artifacts. Also fixed a pre-existing truncation bug found in `articles/index.html` (missing a card, footer, and closing tags since at least commit 33b9581) as its own separate commit.
**Next up:** None outstanding from this pass. Title/meta-tag em-dashes were left alone since the copy deck never specified changes there.

### 2026-06-25 — Add disc-explanations.html, link from homepage Tools section
**Files:** `disc-explanations.html` (new), `index.html`
**What:** Built a new reference page with 20 common cable/internet tech-support concepts (TV & video, internet & connectivity, equipment & maintenance), each explained four ways — one per DiSC style (D/i/S/C) — matching the visual style of the existing `/articles/` pages (serif headings, 720px column, style-card pattern). Linked it as a new "Reference" work-card in the homepage Projects & Tools grid, right after the Call Flow Tool card. Page links back to `/` and forward to `/call-flow.html`.
**Next up:** Build `disc-analogies.html` (same format, DISC-style analogies for explaining tech issues) and link it from the same Tools section.

### 2026-06-25 — Add disc-analogies.html, link from homepage Tools section
**Files:** `disc-analogies.html` (new), `index.html`
**What:** Built the companion analogies page — 20 everyday comparisons (highway bandwidth, garden hose vs. fire hose, pizza-slice splitters, rush-hour congestion, etc.) for common network concepts, each reshaped for D/i/S/C. Same visual template as `disc-explanations.html`, cross-linked to it. Added as a third "Reference" work-card in the homepage Tools grid.
**Next up:** Move to MISSION content priorities — stage-by-stage DISC communication guidance mapped to the call-flow lifecycle (open, discovery, diagnosis, resolution, misread recovery, escalation, close), tied into the existing call-flow.html / MISREAD_RECOVERY system.

### 2026-06-25 — Add disc-call-stages.html, link from homepage Tools section
**Files:** `disc-call-stages.html` (new), `index.html`
**What:** Built the stage-by-stage DISC communication guide covering the full support-call lifecycle: open/greeting, discovery, diagnosis, resolution, misread recovery, escalation, close. Each stage has a D/i/S/C style-card with example language and a "watch for" note, plus a short scenario callout. Read call-flow.html's STEPS array and MISREAD_RECOVERY const first to ground stage boundaries and quote the tool's actual recovery banner language verbatim in the Misread Recovery section, so this page accurately ties into the live 23-step/92-script tool rather than an assumed structure. Linked as a fourth "Reference" work-card on the homepage.
**Next up:** Per the MISSION priorities, remaining open items are mostly already covered (DISC adaptation per stage, do/don't language, scenarios, tie-in to call-flow.html/MISREAD_RECOVERY, nav/voice/visual consistency). Future work could expand individual stages into longer treatments or add more scenario variety per style.

