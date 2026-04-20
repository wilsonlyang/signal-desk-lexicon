IP Protection Checklist · Signal Desk
Version: v1.1 · Updated 2026-04-20
Owner: Wilson L Yang
Purpose: The defense routine executed every time a new term is coined, and the verification routine executed before a term is proposed for coinage.

Core Thesis
On the internet, IP cannot be made secret — any content can be copied. IP can only be made unambiguously attributable. The objective is not to prevent copying; it is to ensure that when copying happens, the origin is instantly provable.
The defense mechanism is a distributed timestamp chain: five or more independent timestamps, across platforms Signal Desk does not control, created within minutes of each other, all pointing to the same Wilson L Yang authorship event.
But a timestamp chain is only valuable if the underlying concept is genuinely original to Signal Desk. This document now covers both:

Pre-coinage verification — ensuring the term is actually coinable
Post-coinage defense — ensuring the timestamp chain is built correctly


Part I · Pre-Coinage Verification (Mandatory, Added v1.1)
The Three-Search Protocol
Before any term is proposed for coinage — whether by Wilson L Yang or an AI assistant preparing a recommendation — these three searches must be executed and the results recorded.
Search 1 · Primary Context
"[exact phrase]" + keywords from the primary domain where the term would be used.
Example: "Mandate Discount" finance valuation
Example: "Partition Map" capital markets framework
Search 2 · Adjacent Context
"[exact phrase]" + keywords from adjacent professional domains where the phrase might have independent established use.
Example: "Partition Discount" real estate appraisal (revealed this term is occupied in RE)
Example: "Capability-Price Decoupling" economics
Adjacent domains to consider: real estate, legal, accounting, insurance, actuarial, academic, consumer marketing, engineering, biotech.
Search 3 · Variant Search
"[exact phrase]" OR "[plausible variant]" to catch alternative phrasings that might represent prior coinage of the same concept under a different name.
Example: "Mandate Discount" OR "mandate-driven discount"
Example: "Scarcity Bubble" OR "Scarcity Stack"
Disposition Rules
Finding across all three searchesActionZero relevant prominent results✅ CLEAN — proceed to coin; record verification in Lexicon entryResults exist but in unrelated domain (e.g., physics, chemistry, biology)✅ CLEAN with caveat — note in Lexicon entry, ensure usage context is unambiguousEstablished use in an adjacent professional domain❌ DO NOT COIN — propose renameEstablished use in the same domain❌ DO NOT COIN — this is an existing term, not coinable
Confidence Framing (Non-Negotiable Honesty)
"Clean based on search" ≠ "Never used anywhere, ever."
Search engines do not index:

Podcasts and video content (audio text hard to retrieve)
Many paywalled academic journals
Foreign-language usage (Chinese finance literature, etc.)
Private research notes at investment firms / consultancies
Small blogs / Substacks not well-SEOed

Realistic confidence ceiling: ~95% that no prominent prior authorship exists. The residual 5% covers obscure or non-indexed usage.
This confidence level is sufficient for IP defense, because any future challenger must produce public, searchable, timestamped prior art to contest authorship. A challenge based on "I also thought of this privately years ago" has no standing without prior public evidence.
Enforcement Mechanism
If Claude (or any AI assistant) proposes a term without recorded three-search verification, Wilson L Yang will respond with the single-phrase interrupt:

"搜了吗？" (or in English: "Did you search?")

This functions as a hard stop. The assistant must execute the three searches and present results before the recommendation is reconsidered. This guardrail exists because discipline under pressure is empirically unreliable — an external prompt is more reliable than self-regulation.
Recording Verification in Lexicon
Every Lexicon entry must include a Three-Search Verification block structured as:
markdown**Three-Search Verification** (YYYY-MM-DD):
- Primary: `"[phrase]" keywords` → [finding summary]
- Adjacent: `"[phrase]" adjacent_keywords` → [finding summary]
- Variant: `"[phrase]" OR "[variant]"` → [finding summary]
- **Disposition**: ✅ CLEAN | ❌ NOT CLEAN
Entries lacking this block are provisional and must not be used externally.

Part II · Coin Ceremony Defense (Original v1.0, Preserved)
When to Execute This Routine
Execute once per coined term, at the moment of first public introduction.
Specifically:

The day a new term is introduced in a Signal Desk long-form piece (the coinage event)
Before the term is used publicly anywhere else

Do not execute this routine for:

Referencing an existing Lexicon term in a new piece (no new authorship claim needed)
Minor term variants (use the parent term's existing timestamp chain)
Candidate-pipeline terms not yet formally coined

The 10-Minute Routine
Execute in order. Each step adds one independent timestamp layer.
Step 1 · Explicit Coinage Statement (2 min)
In the long-form piece where the term first appears, use explicit coinage language:

✓ "I'll call this the Signal Desk [Term]..."
✓ "What I'll call the [Term]..."
✗ "The [Term] describes..." (passive — no coinage event recorded)

Bold the term on its first appearance. Define it explicitly in the surrounding paragraph.
Step 2 · Substack Publication Timestamp (counts automatically)
Publish the piece on Substack. The publication timestamp is automatically recorded by Substack's servers.
Step 3 · Archive.org Submission (1 min)
Go to archive.org/web/ → paste the Substack article URL → click "Save Page Now".
Save the resulting archive URL.
Step 4 · X Announcement Post (2 min)
Post on X a dedicated announcement of the new term. Format:
New framework from today's Signal Desk piece:

the [Term] — [one-line definition].

[Why it matters in one sentence.]

Full piece: [Substack URL]
Copy the tweet URL.
Step 5 · GitHub Commit (2 min)
Open SIGNAL_DESK_LEXICON.md in the signal-desk-lexicon repo. Add the new term as a full entry. Fill in:

Three-Search Verification block (from Part I)
Coined date
Source URL (the Substack article)
Archive.org URL
X announcement URL

Commit with a descriptive message: Coin term: [Term] (YYYY-MM-DD) — verified clean
Step 6 · LinkedIn Mention (2 min)
Publish a LinkedIn post (not article) mentioning the new term. Place the Substack link as the first comment.
Total Time: ~10 minutes (plus ~5 minutes for Three-Search Verification in Part I)
After this routine, the new term has 5 independent verifiable timestamps:

Substack publication timestamp
Archive.org snapshot (third-party immutable)
X announcement tweet (server-timestamped)
GitHub commit (SHA-256-hashed, immutable)
LinkedIn post (server-timestamped)


Part III · Optional Hardening (Flagship Terms Only)
OpenTimestamps (Blockchain Timestamp)
For flagship terms (e.g., Partition Map), consider adding one more layer:

Save the published long-form article as a local .html file
Go to opentimestamps.org
Drag the file into the browser → get a .ots proof file
Store the .ots file in the local Signal Desk archive + commit to the GitHub repo

The .ots proof is anchored to the Bitcoin blockchain — the strongest possible timestamp.
Use sparingly; reserve for flagship concepts where additional defense is worth the friction.

Part IV · Response Protocol When Terms Are Used Without Attribution
Level 1: Small account, casual use, no prominent visibility
Response: None. ROI of intervention too low.
Level 2: Medium-level account (~10K followers), no attribution
Response: One friendly public reply:

Good to see the [Term] concept spreading. For readers who want the original framework and the underlying data: [Substack URL]

Level 3: Prominent account or formal media use, no attribution
Response sequence:

Private outreach first (DM / email). Include Archive.org URL + GitHub commit URL + Substack URL:


Hi [Name] — noticed your recent use of [Term]. I introduced this framework on [date], in my Signal Desk piece.
Original piece: [link]
Timestamp: [Archive.org link]
Concept registry: [GitHub link]
Happy to see the concept reaching wider audiences — would appreciate an attribution line when the term is used.
— Wilson L Yang


Give 24–48 hours for response.
If no response: one public post, measured tone:


Glad to see the [Term] framework gaining traction in wider discussion.
For record-keeping: the framework was introduced in Signal Desk on
[date] — [link]. Precise use of the term will help the
broader discourse.

Never use: "stolen," "plagiarized," "ripped off." Measured tone is itself a credibility signal.
Level 4: Formal academic / industry publication uses without citation
Response: Email the publication's editor + timestamp evidence. Most reputable outlets will issue a correction.
Level 5: Deliberate bad-faith appropriation (extremely rare)
Escalation: DMCA for copyrighted content, formal attribution demand letter, public-forum appeal backed by full timestamp chain.

Part V · Reader-Assisted Defense
In every long-form piece introducing or referencing a Lexicon term, include in the footer:

If you notice the [Term] (or other Signal Desk frameworks) being used elsewhere without attribution, I'd appreciate a heads-up. Shared vocabulary only compounds if attribution does too.

This recruits core readers as distributed watchers.

Part VI · Quarterly Citation Audit
Every 3 months:

Google search each Lexicon term (exact phrase in quotes)
X / Substack / LinkedIn search for each term
Log every appearance in the Lexicon's "External citations tracker":

Citing author / publication
Date
Whether Signal Desk attribution was given
Any action taken



Growing citation count is Signal Desk's hardest impact metric — more meaningful than subscriber count or impression count.

Part VII · When GitHub Is Unavailable
Substitute in order of preference:

GitLab (gitlab.com/wilsonlyang) — main alternative, equal credibility
Codeberg (codeberg.org/wilsonlyang) — European non-profit git host
OpenTimestamps alone — if no git platform available, .ots proof + Archive.org snapshot is sufficient

Do not skip the timestamp step; one missing node is acceptable, skipping the whole step is not.

What This Routine Does Not Cover

Article copying verbatim → copyright (automatic) + DMCA takedowns
Chart image copying → watermark with signaldeskwilson.substack.com (in Chart Template)
Trademark of "Signal Desk" → separate legal process
Data analysis methodology → partially covered by citing data sources


Version Log
v1.1 · 2026-04-20 — Added mandatory Three-Search Verification Protocol (Part I). Added "搜了吗？" interrupt as enforcement mechanism. Extended Lexicon commit template to require verification block. Added Response Protocol levels and reader-assisted defense sections.
v1.0 · 2026-04-20 — Initial routine established. 10-minute per-term defense flow specified.

Maintained by Wilson L Yang. Part of the Signal Desk identity layer, alongside SIGNAL_DESK_LEXICON.md and BYLINE_STANDARDS.md.
