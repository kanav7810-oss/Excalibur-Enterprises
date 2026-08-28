# SVS Landing Page — Resume Doc

Context for a no-context agent picking up this work. File being edited: `svs/index.html` in this repo (`kanav7810-oss/Excalibur-Enterprises`, branch `main`).

## What SVS is

Student Venture Sprint (SVS): Excalibur AI's 4-week, 1:1 venture-building program for high schoolers. Student works directly with the founder (Soham Jani) to turn one idea into a project/nonprofit/business with a concrete launch foundation. Structure: Week 1 Direction → Week 2 Validation → Week 3 Foundation → Week 4 Launch. Positioned as "not resume padding" — student's college application lists the real venture, not "SVS."

Solo-run by design (Soham only, no co-mentors), capped 1:1 cohorts. Credibility layered in over time via partnerships (e.g. YRI) and outside-expert guest talks, not by adding mentors. SVS is the pivot away from Excalibur's older tutoring/growth-infra business, which Soham considers unscalable — treat SVS as the primary Excalibur venture going forward.

Founding cohort: 5 seats, $1,047 for 4 weeks, 1 seat filled as of 2026-08-25. Applications close September 25. CTA books a fit call at `https://excalibur.neetocal.com/meetsoham`.

## Why this page is being rewritten

Ran a mock sales pitch on Kanav Thonda (Excalibur's own CTO/COO, not a real prospect) as a friction test. His objections, ranked by how hard he pushed:
1. **Credibility gap** — "why you, not a free teacher/professor." Biggest blocker.
2. Value prop unclear for non-business majors until given a concrete example.
3. Price resistance — weak, secondary.

Separately, Claude was asked to give a conservative/skeptical read of the page as a skeptical parent, independent of Kanav's feedback. Verdict: would not apply yet. Reasons: zero external proof for claims (revenue, internships, followers, college admits — all self-reported, unlinked), founder identity was completely hidden (no name/photo/LinkedIn), company has no visible track record, guarantee is soft (no defined end condition), price/CTA asked for commitment before any trust was built, and the "Honest Objections" section reads defensive rather than confident.

## Work completed so far (commits on `main`, newest first)

- `9c60a08` — Added real founder identity to the Venture Partner section: name (Soham Jani), photo (`svs/assets/soham-jani.jpeg`), LinkedIn link (`linkedin.com/in/meetsoham`), and a named/checkable track-record list (5 real roles pulled from a LinkedIn screenshot doc, see below) replacing vague self-reported stats. Revenue claim softened from "multi-five-figure in 3 months" to "five-figure within months" since exact number wasn't provided. Testimonial block added but reframed as retention-based proof (client retention in tutoring business), NOT a fabricated quote — an early draft had an invented parent quote, caught and corrected before push.
- `bbfd491` — Real scarcity/price anchor: "4 of 5 founding seats left," "$1,047 for the 4-week founding cohort." All CTA buttons repointed from a stale Tally form link to `https://excalibur.neetocal.com/meetsoham`, button copy changed to "Book Your Fit Call" / "Book a Call" (lower commitment than "Apply").
- `a1b0605` — First copy pass: cut hedging language, shortened the "Honest Objections" Q&A section, removed two duplicate FAQ items, made the "expert" self-positioning more subtle per Jordan-Belfort-style closing principles (certainty, sharpness, passion) per explicit user request.

Source of the 5 real roles used in commit `9c60a08`: a Google Doc titled "svs proof - linkedin" (`https://docs.google.com/document/d/1TcIj5_7oCII5gDdeBy1-OMJ2r1ht1BnQ6-Qc4mAi6H4/edit?tab=t.0`), which contains screenshots of Soham's LinkedIn experience section:
- Founding Engineer, Soverin Gaming (frontend + backend game systems)
- Growth Advisor, stealth startup — "validated by Stanford, NVIDIA, GM, XTrace + $1.5k+ non-dilutive grant"
- Founder, Excalibur — tutoring/mentorship program, "scaled to $xxK" (redacted, no exact figure given)
- AI Development and Ops, Inductive — worked 1:1 with the CEO
- SDR / Intern Management Lead, YRI — "generated ~$40k in lead value within 2 months... managed team of 10 interns"
- Financial & Growth Consultant, GlobalSVF — "<12% acceptance rate" program

That doc does NOT contain: an exact revenue figure, a LinkedIn follower-count screenshot, or college-admit proof. Per user instructions:
- Revenue: keep vague/range, do not state an exact number (user chose "keep as range/redacted").
- Follower count claim (~1,000): resolved by linking the LinkedIn profile itself rather than embedding a screenshot (user chose "just link LinkedIn profile") — **not yet implemented on the page**, still says "Learn more about the system" link only; no explicit follower-count line currently on page since it was removed in `9c60a08`'s proof-row cleanup.
- College admits (Emory, UIUC, UCSD, UW-Seattle): user confirmed proof exists, said "will send separately." **Not yet received or added.**

## Open questions / not yet done

1. **College admit proof** — waiting on user to send acceptance emails or portal screenshots (school name + name visible, redact IDs). Once received: add to the founder/track-record section or a dedicated proof strip, following the same "named, checkable claim" pattern used for the internship roles.
2. **SVS-specific testimonial** — does not exist yet, because SVS itself is a new venture (the 9-month track record is from the tutoring business, not SVS). Current page honestly frames the testimonial as tutoring-business retention proof, not an SVS result. Once the first founding-cohort student finishes, get a real quote/testimonial from them or their parent and add it — this is the single biggest remaining trust gap that copy alone can't fix.
3. **Live deployment not verified** — changes are pushed to GitHub `main`. Whether the production site (referenced elsewhere as `excalibur-edu.vercel.app`, path `/svs`) auto-redeploys from this branch has never been checked in this workstream. Verify before telling the user the live site reflects these changes.
4. Founder video/intro clip — user said feasible ("yes, can record a short intro video") but not yet recorded or embedded.

## Working setup

- Repo cloned locally at `/private/tmp/claude-501/-Users-sohamjani/96245759-22bf-411a-8330-5b6b02ad2fd3/scratchpad/Excalibur-Enterprises` (a scratchpad path — ephemeral, may not exist in a future session; re-clone from GitHub if gone).
- Founder photo already added at `svs/assets/soham-jani.jpeg`.
- Git identity on commits shows local machine defaults (name/email auto-detected), not explicitly configured — commits still succeed, this is just an informational warning, not an error.
- User's standing preferences (see assistant's own memory, not this repo): use browserclaw for all web/browser interaction (not WebFetch/WebSearch); keep token usage efficient; never fabricate proof, testimonials, or numbers — ask for real data instead.

## Immediate next step if resuming

Ask the user (via AskUserQuestion or plain question) whether the college-admit proof is ready to send. If yes, ingest it the same way the LinkedIn doc was ingested (browserclaw screenshot/read of whatever doc or images they share), then add a proof line/section for it and push a new commit. Do not invent numbers, quotes, or screenshots — every claim added to this page must trace back to something the user actually provided.
