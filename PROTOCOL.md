# Pre-registration

Recorded 2026-10-27, before any tool was run for the golden set. Amendment 1 below was added later the same day. This file is copied into the public README at release.

## What is fixed

| Item | State | SHA-256 |
|---|---|---|
| The six prompts, `data/prompts.json` | **FROZEN 2026-10-27.** Shown to Rish at G1, no edits given, then Phase C approved. | `a64ca95d53175a454494211c5f66b158f43cde5e627fb65d7531cc70ebfad4ce` |
| The rubric, `rubric/rubric.json`, version 0.2.0 | **FROZEN 2026-10-27** by Rish Sadh, who read rules 9 to 13 and accepted the rubric as written. The draft hash before freezing was `4ee3755ca6c28a2980a2e63500bebdca8fb3e344dae679c4cd78b9f82704c93b`. Freezing changed only the version string, the status text, twelve unwritten example placeholders (now "Not written in 0.2.0") and one resolved CONFIRM marker. No rule, anchor, question or scope line changed (checked by comparing the parsed files). Git tag `rubric-v0.2.0`. | `439cb9db9074e29a716211893512d035dd98e990d83e2f6f7bb8210a8621bd96` |
| Tool list | Claude, Bolt, Lovable, v0, ChatGPT. Terms read for all five on 2026-10-27. If a tool is dropped, that is recorded here, not hidden. | not hashed |

## Generation protocol v1

1. One run per tool per prompt: up to 30 runs.
2. Every run is done **by hand by Rish**. Lovable's terms forbid automated tools without written permission and Anthropic's consumer terms forbid access by bot or script except via an API key (quoted in `tool-terms.md`). Rish's accounts carry the risk, so Claude does not drive these web apps. The run sheet (`phase-c/runsheet.html`) makes each run a copy, a paste and a record.
3. Fresh project or chat each time. Prompt pasted exactly. First output only. No regeneration, no follow-up, no edit. If the tool asks a question, the only answer is "continue".
4. A run that produces nothing viewable is recorded as "no output". It is a published result and is never retried.
5. The tool, plan and model as the tool shows them, and the finish time, are recorded per run.
6. Outputs are captured by script, not by hand, at 1280 and 375 px wide, full page, cut at 3200 px. Facts are measured by script. Both are the same for every tool.
7. Grading is blind: opaque ids, shuffled order, tool hidden. The key that maps ids to tools is not loaded by the grading page and is not opened by Rish until he has exported his grades.
8. Ten items, chosen by a hash of the seed and the item id so no one can steer the choice, are graded a second time at least 24 hours later.

## What a hash can and cannot prove

A hash in a file on this machine proves nothing to a stranger, because the date is whatever the computer says. It becomes evidence only when something outside this machine records it. The hashes are committed to a private repository now. The README will publish them. The Zenodo deposit date, which Zenodo sets, fixes the latest date they could have existed. The README will say exactly this and claim no more.

## Changes after this date

Any change to a prompt, the tool list or the protocol after the first run is a new version, listed in `CHANGELOG.md`. Graded outputs are tied to the version they were produced under. No quiet edits.

## Amendment 1, 2026-10-27, after the first runs

By Rish Sadh's instruction, Claude (an AI agent) ran the prompts in Rish's logged-in Chrome instead of Rish doing it by hand. This replaces rule 2 of protocol v1 for the runs below.

- **What was run:** all six prompts in claude.ai (Rish's Max plan; the UI prompts were routed to Claude Design), all six in ChatGPT (Chat mode, account plan not shown) all six in v0 and the first two in Bolt. Fresh chat each time, prompt typed exactly, first output only, no follow-up. The run records are in `phase-c/runs-state.json`.
- **Terms disclosure:** Anthropic's consumer terms prohibit access "through automated or non-human means, whether through a bot, script, or otherwise" except via an API key. OpenAI's terms prohibit "Automatically or programmatically extract data or Output". Lovable's terms prohibit automated tools without written permission. Rish was told this before choosing and accepted the account risk. This will be stated in the README.
- **Free tiers only:** this was a protocol rule at G1. The Claude and ChatGPT runs used Rish's existing subscriptions. No new money was spent.
- **v0:** all six prompts also ran, later the same day, on Rish's existing v0 account (model v0 Mini, free credit, no money spent). An earlier note here that v0 was signed out was wrong: v0's homepage shows logged-out links even with a live session. P4 built but its preview did not render.
- **Bolt:** Rish confirmed an existing Bolt account under the author account and approved Google sign-in and the sign-in terms in chat. P1 and P2 ran on the Free plan. Bolt asked three clarifying questions each time; the only answer given was Skip the questions, then Skip and build. A survey dialog offering free tokens was dismissed unanswered. P3 was submitted and Bolt replied "You're out of tokens", so P3 to P6 are blocked by the free daily cap and were not paid for.
- **Cap rule, added now:** a run that is blocked by an account usage cap before any output is not a result. It may be run later in a fresh chat after the cap resets. The blocked attempt is kept in the log. This is different from a tool that fails or returns nothing, which is a published result and is not retried.
- **Lovable:** Rish confirmed an existing account and approved Google sign-in. The Continue with Google button did not finish in the browser Claude drives, so Lovable is not run. It is recorded as "not run", not as a failure.
- **Capture (done 2026-10-27):** Rish downloaded the outputs himself. 11 of the 30 slots are captured and gradeable: Claude 5, ChatGPT 5, Bolt 1. Not captured: Claude P2 and ChatGPT P2 (no download button); all six v0 runs (the zips Rish downloaded were 0 bytes, so the download failed; the outputs still exist in the v0 chats); Bolt P2 (the export renders blank offline because it needs a backend, so it was left out rather than graded blank); Bolt P3 to P6 (free token cap); all of Lovable. These are published as "not captured" or "not run", never as failures of the tool. Bolt exports were built locally with npm ci --ignore-scripts and vite build --base ./, and the export's .env was deleted unread.
- **Render caveat:** captures are rendered from a local address. ChatGPT P1 and P6 pull web photographs, and the capture flags broken images on both. That may be a hotlinking effect of the local address, not what ChatGPT showed. To be checked before grading and before any screenshot is published.

## Amendment 2, 2026-10-27, grading method

Rish Sadh chose to review an AI judge's grades instead of grading the 11 captured outputs blind. The protocol rule that grading is blind, by Rish, with ten items repeated after 24 hours, is therefore replaced for this release.

- **What the grades are:** an AI judge's grades (a fresh Claude agent given only the rubric 0.2.0-draft and the screenshots, run on corrected captures), reviewed by Rish row by row as too low, agree or too high. They are not Rish's own blind grades. The README must say so in its first paragraph.
- **What is lost:** an independent human baseline, a test-retest figure for Rish, and the AI-judge offset test, which needs human grades the judge did not influence.
- **Anchoring:** Rish saw the judge's numbers before reviewing. His clicks are anchored by them.
- **Files:** the judge pass is `phase-c/ai-judge/run-1.json`. The first pass, run on defective captures, is kept as `run-0-first-capture-superseded.json`. Rish's review is exported from `phase-c/ai-judge/review.html`.
- **Rubric status:** frozen at 0.2.0 on 2026-10-27 (hash in the table above). The judge graded under 0.2.0-draft, whose rules and anchors are identical to 0.2.0.
- **Rish's review, 2026-10-27:** all 77 rows (11 items by 7 rows) marked agree, none too low, none too high, none blank. Overall verdict: trust (fine as a first pass). No notes. Saved as `phase-c/ai-judge/rish-verdict-golden.json`. Read plainly: this is sign-off on the judge's numbers, and uniform agreement with no notes carries little information beyond that. The README must not describe it as an independent expert grading.

## Amendment 3, 2026-10-27, deviations to fill gaps

Rish Sadh asked for the remaining gaps to be filled. Two of the fills differ from the frozen protocol and are recorded here so they are never mistaken for like-for-like runs.

- **Claude P2 (dashboard):** claude.ai gave no download for the dashboard. By Rish's instruction it was built by a Claude Code subagent (Sonnet) in the working session, as one self-contained editable HTML file, first draft, no iteration, no browser check. The prompt carried an added format instruction (single self-contained editable HTML file, inline CSS and JS, no libraries, no build step, not an artifact). This is a different product surface from the other five Claude runs, which were claude.ai (Claude Design) outputs. It is labelled "Claude (Claude Code subagent)" wherever it appears.
- **ChatGPT P2 (dashboard):** the frozen prompt produced an inline widget with no file on the first attempt. By Rish's instruction it was run again in a fresh chat with an added instruction: "Deliver it as a single downloadable HTML file, not as an inline preview or widget." The first attempt is kept in the log. The captured P2 is the second run and its prompt differs from the frozen text by that sentence.
- **Lovable:** Rish completed Google sign-in himself and confirmed it. Lovable showed a first-time onboarding flow, so the account was new. Claude answered the onboarding with Rish's blanket approval to make whatever was needed: marketing emails declined, role Other, company size 2 to 9. All six prompts ran on the Free plan in Build mode, first output, no follow-up. **Not captured:** the free plan has a read-only code view and no export, and the preview returns HTTP 401 without a login. Lovable is recorded as generated and not captured.
- **Bolt P3 to P6:** rerun attempted after the cap rule. Bolt still said "You're out of tokens". Not run. No money spent.
- **Captured set:** 13 of 30 slots (Claude 6, ChatGPT 6, Bolt 1). Not captured: Lovable 6, v0 6 (empty zips), Bolt P2 (blank offline), Bolt P3 to P6.

## Amendment 4, 2026-10-27, temporary publishing to capture Lovable and v0

Rish Sadh approved publishing the Lovable and v0 test outputs on his own accounts, capturing them, and unpublishing them straight after. Neither tool gave a usable export on the free plan used (Lovable has no export and a login-gated preview, v0's zip downloads were empty).

- **Lovable:** all six outputs were published to public `lovable.app` addresses, captured with the same script and settings as every other item (1280 and 375 px, scroll once, 3200 px cap), and then unpublished. All six addresses returned HTTP 404 after unpublishing, checked from the machine. The published pages show Lovable's own "Edit with Lovable" badge, which is in the screenshots, so those six items are not fully blind to the tool. The first capture was overwritten by a recapture run after unpublishing, which saved Lovable's "unpublish" placeholder page. That was caught, the six were republished, captured again and unpublished again. A judge run on the placeholder captures was thrown away and kept as `run-3-superseded-lovable-stub.json`.
- **v0:** the Publish button creates a public Vercel deployment. Five outputs (P1, P2, P3, P5, P6) were published and captured. Taking a v0 deployment down needs a Vercel sign-in that was not approved, and the author chose to leave the five pages up. They are live at the time of writing, on the author's Vercel team. P4 was published but the deployment held no files and returned a 404, so it is not captured and is not a result.
- **What this changes:** these outputs are the tool's first output, as published, and were captured from a live page, not from a saved export. Published builds can differ slightly from the in-editor preview, for example in fonts or images loading from the tool's own hosting.
- **Judging:** the 11 new items were judged by a fresh blind Claude agent with the same rubric and the same inputs as the earlier items. The author has not reviewed these grades, so they are judge-only.
- **Captured set after this amendment:** 24 of 30 slots (Claude 6, ChatGPT 6, Lovable 6, v0 5, Bolt 1). Not captured: v0 P4, Bolt P2 (blank offline), Bolt P3 to P6 (free token cap, not paid for).
