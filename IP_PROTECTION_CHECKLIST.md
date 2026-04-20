# IP Protection Checklist · Signal Desk

**Version**: v1.0 · Established 2026-04-20
**Owner**: Wilson L Yang
**Purpose**: The 10-minute defense routine executed every time a new term is coined.

---

## Core Thesis

On the internet, IP cannot be made secret — any content can be copied. IP can only be made **unambiguously attributable**. The objective is not to prevent copying; it is to ensure that when copying happens, the origin is instantly provable.

The defense mechanism is a **distributed timestamp chain**: five or more independent timestamps, across platforms Signal Desk does not control, created within minutes of each other, all pointing to the same Wilson L Yang authorship event.

This document is the routine that builds that chain.

---

## When to Execute This Routine

**Execute once per coined term**, at the moment of first public introduction.

Specifically:
- The day a new term is introduced in a Signal Desk long-form piece (the coinage event)
- Before the term is used publicly anywhere else

**Do not execute this routine for**:
- Referencing an existing Lexicon term in a new piece (no new authorship claim needed)
- Minor term variants (use the parent term's existing timestamp chain)
- Candidate-pipeline terms not yet formally coined

---

## The 10-Minute Routine

Execute in order. Each step adds one independent timestamp layer.

### Step 1 · Explicit Coinage Statement (2 min)

In the long-form piece where the term first appears, use **explicit coinage language**:

- ✓ **"I'll call this the Signal Desk [Term]..."**
- ✓ **"What I'll call the [Term]..."**
- ✗ "The [Term] describes..." *(passive — no coinage event recorded)*

Bold the term on its first appearance. Define it explicitly in the surrounding paragraph.

This creates a **textual claim to authorship** inside the piece itself, which travels with the content forever.

---

### Step 2 · Substack Publication Timestamp (counts automatically)

Publish the piece on Substack. The publication timestamp is automatically recorded by Substack's servers and is visible to readers.

No manual action required — just ensure the piece is published (not drafted, not scheduled to future date-jump).

---

### Step 3 · Archive.org Submission (1 min)

Go to **archive.org/web/** → paste the Substack article URL → click "Save Page Now".

Wait 10–20 seconds for the snapshot to complete. Copy the resulting archive URL.

The archive URL will look like:
```
https://web.archive.org/web/20260420123456/https://signaldeskwilson.substack.com/p/[article-slug]
```

**Save this URL** — it is one of the hardest independent timestamps available. Internet Archive is a third-party non-profit whose timestamps have been accepted in court.

---

### Step 4 · X Announcement Post (2 min)

Post on X a dedicated announcement of the new term. Format:

```
New framework from today's Signal Desk piece:

the [Term] — [one-line definition].

[Why it matters in one sentence.]

Full piece: [Substack URL]
```

Example:
```
New framework from today's Signal Desk piece:

the Partition Map — a 2×2 that maps AI assets across private/public
markets and global/China capital pools.

Explains why DeepSeek trades at $10B while MiniMax trades at 425x sales.

Full piece: signaldeskwilson.substack.com/p/...
```

X's timestamp is server-recorded and visible in the tweet URL.

---

### Step 5 · GitHub Commit (2 min)

Open `SIGNAL_DESK_LEXICON.md` in your local copy of the `signal-desk-lexicon` repo.

Add the new term as a full entry (following the template in the Lexicon file).

Fill in:
- Coined date
- Source URL (the Substack article)
- Archive.org URL (from Step 3)
- X announcement URL (from Step 4)

Commit with a descriptive message:
```
git add SIGNAL_DESK_LEXICON.md
git commit -m "Coin term: [Term] (2026-04-20)"
git push
```

The commit is recorded on GitHub with a SHA-256 hash and server timestamp — **immutable once pushed**.

---

### Step 6 · Substack Lexicon Page Update (1 min)

Open the public Substack Page `/lexicon` (if already created) and add the new term entry following the same structure.

If the Substack Page does not exist yet, create it once (it is a one-time setup task, not a per-term action).

This is a **public-facing registry** of your coined terms, indexable by Google.

---

### Step 7 · LinkedIn Mention (2 min)

Publish a LinkedIn post (not article) mentioning the new term. Format:

```
Published a new piece on Signal Desk today:
"[Article Title]"

Introducing what I'll call the [Term] — [one-line definition].

[One sentence on implication.]

Link in comments.
```

Post the Substack link as the first comment (LinkedIn's algorithm deprioritizes posts with external links in the body).

This adds a LinkedIn-side timestamp and makes the coinage visible to a different audience segment.

---

### Total Time: ~10 minutes

After this routine, the new term has **5 independent verifiable timestamps** pointing to Wilson L Yang as first-known-coiner:

1. Substack publication timestamp (in the article metadata)
2. Archive.org snapshot (third-party immutable)
3. X announcement tweet (server-timestamped)
4. GitHub commit (SHA-256-hashed, immutable)
5. LinkedIn post (server-timestamped)
6. (Optional) Substack Lexicon Page update

Any challenger would need to produce an **earlier** timestamp on an independent platform to contest authorship. The probability is effectively zero.

---

## Optional Hardening (for Flagship Terms Only)

For terms you consider especially valuable (like Partition Map), add one more layer:

### OpenTimestamps (Blockchain Timestamp)

1. Save the published long-form article as a local `.html` file
2. Go to [opentimestamps.org](https://opentimestamps.org)
3. Drag the file into the browser → get a `.ots` proof file
4. Store the `.ots` file in your local Signal Desk archive + commit to the GitHub repo

The `.ots` proof is anchored to the Bitcoin blockchain. It is the **strongest possible timestamp** — provably unchangeable by any entity including the US or Chinese governments.

Use sparingly (one-time setup understanding required); reserve for flagship concepts.

---

## Response Protocol When Terms Are Used Without Attribution

### Level 1: Small account, casual use, no prominent visibility
**Response**: None. ROI of intervention too low. Let it go.

### Level 2: Medium-level account (~10K followers), no attribution

**Response**: One friendly public reply on their platform:

> Good to see the [Term] concept spreading. For readers who want the original framework and the underlying data: [Substack URL]

Tone: collegial, not accusatory. This establishes your prior authorship in public view without creating conflict. In ~90% of cases, the other account adds a credit line or deletes.

### Level 3: Prominent account or formal media use, no attribution

**Response sequence**:

1. **Private outreach first** (DM / email). Include the Archive.org URL + GitHub commit URL + original Substack URL:

> Hi [Name] — noticed your recent use of [Term]. I coined this framework on April 20, 2026, in my Signal Desk piece on the China AI valuation gap.
>
> Original piece: [link]
> Timestamp: [Archive.org link]
>
> Happy to see the concept reaching wider audiences — would appreciate an attribution line when the term is used. I'm glad to answer any questions about the framework if useful.
>
> — Wilson L Yang

2. **Give 24–48 hours** for response.

3. **If no response**: One public post (X or LinkedIn), measured tone:

> Glad to see the [Term] framework gaining traction in wider discussion.
> For record-keeping: the framework was introduced in Signal Desk on
> April 20, 2026 — [link]. Precise use of the term will help the
> broader discourse.

**Never use**: "stolen," "plagiarized," "ripped off," or any language of accusation. Measured tone is itself a credibility signal. Your readers will infer the situation without explicit labels.

### Level 4: Formal academic / industry publication uses without citation

**Response**:
1. Email the publication's editor or the paper's corresponding author directly
2. Include Archive.org timestamp + publication date
3. Request formal citation correction
4. Most reputable outlets will issue a correction or updated citation

### Level 5: Deliberate bad-faith appropriation (extremely rare)

Escalation options:
- DMCA for copyrighted content (articles, charts)
- Formal attribution demand letter
- Public-forum appeal backed by timestamp chain

This level is exceedingly rare for conceptual IP. In almost all cases, Level 1–3 responses resolve the situation without escalation.

---

## Reader-Assisted Defense

**In every long-form piece that introduces or references a Lexicon term, include at the footer**:

> If you notice the [Term] (or other Signal Desk frameworks) being used elsewhere without attribution, I'd appreciate a heads-up. Shared vocabulary only compounds if attribution does too.

This recruits your core readers as distributed watchers. Once Signal Desk has 30–50 engaged readers, they will identify unattributed uses faster than any individual could.

---

## Quarterly Citation Audit

Every 3 months, execute a citation audit:

1. Google search each Lexicon term (exact phrase in quotes)
2. X / Substack / LinkedIn search for each term
3. Note every appearance:
   - Author / publication
   - Date
   - Whether Signal Desk attribution was given
   - Any action taken

Log findings in the Lexicon file under each term's "External citations tracker" section.

**Growing citation count is Signal Desk's hardest impact metric** — more meaningful than subscriber count or impression count. A term with 50 external citations across independent writers is a Lexicon term that has entered the real discourse. That is the primary long-term goal.

---

## When GitHub Is Unavailable

If GitHub is temporarily inaccessible or account issues arise, substitute **either** of these equivalent platforms (in order of preference):

1. **GitLab** (`gitlab.com/wilsonlyang`) — main GitHub alternative, equal technical credibility
2. **Codeberg** (`codeberg.org/wilsonlyang`) — European non-profit git host
3. **OpenTimestamps alone** — if no git platform available, an `.ots` proof file plus the Archive.org snapshot is sufficient timestamp evidence

Do not skip the timestamp step just because the preferred platform is unavailable. The distributed chain is the defense; one missing node does not collapse it, but skipping the whole step does.

---

## What This Routine Does Not Cover

This checklist defends **concept authorship**. It does not defend:

- **Article copying verbatim** → that is copyright (automatic, no action needed) + DMCA for takedowns
- **Chart image copying** → watermark with `signaldeskwilson.substack.com` (already in Chart Template)
- **Trademark of "Signal Desk"** → separate legal process (not recommended for now; revisit if brand name becomes a serious legal asset)
- **Data analysis methodology** → partially covered by citing data sources (keeps methodology attributable) + the Lexicon framework itself

---

## Version Log

**v1.0 · 2026-04-20** — Initial routine established. 10-minute per-term defense flow specified. Five response levels for unattributed use defined.

---

*Maintained by Wilson L Yang. Part of the Signal Desk identity layer, alongside SIGNAL_DESK_LEXICON.md and BYLINE_STANDARDS.md.*
