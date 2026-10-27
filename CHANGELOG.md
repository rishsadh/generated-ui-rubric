# Changelog

Rubric versions are listed here. A change after a version is frozen is a new version. **0.2.0 is frozen.**

## Release v0.2.1, 2026-10-27

Docs and metadata only. The rubric (0.2.0) and the prompts are unchanged, and both hashes are the same as in v0.2.0. Added the DOI, and corrected the wording that said all grades were reviewed by the author: 11 of the 24 were reviewed and 13 were not. The v0.2.0 Zenodo record carried the older wording, which is why this release exists.

## 0.2.0 (frozen), 2026-10-27

Frozen by Rish Sadh after reading rules 9 to 13. SHA-256 of `rubric/rubric.json`: `439cb9db9074e29a716211893512d035dd98e990d83e2f6f7bb8210a8621bd96`. Git tag `rubric-v0.2.0` (its commit message omitted the hash by a mistake in my command; the tag content matches the hash). Compared with 0.2.0-draft, only these changed: the version string, the status text, the twelve unwritten good and bad example placeholders (now "Not written in 0.2.0"), and one resolved CONFIRM marker in the measured-facts note. No rule, anchor, question, look-for list, scope or crosswalk line changed.

## Phase C, 2026-10-27

- Amendment 3: Lovable run (6, not capturable on the free plan); Claude P2 and ChatGPT P2 filled by deviation; captured set is now 13 of 30.
- Amendment 1: Claude ran Claude and ChatGPT prompts in Rish's Chrome, 20 of 30 runs (Claude 6, ChatGPT 6, v0 6, Bolt 2). See notes/PRE-REGISTRATION.md.
- Capture done: 11 of 30 slots captured and ready to grade; manifest and key built. See RESUME.md.
- Capture fixed: scroll once before shooting, skip SVG text in contrast. Screenshots retaken. AI-judge pass added. Amendment 2: Rish reviews the judge's grades instead of grading blind.
- Prompts frozen. Hash in notes/PRE-REGISTRATION.md.
- Generation protocol v1: all runs by hand, because Lovable and Anthropic terms forbid automated access.
- Run sheet, golden-set capture script and shared measurement code added.


## 0.2.0-draft, 2026-10-27

Applied at Rish's instruction from the proposals in `notes/PILOT-RESULT.md`. They come from one blind AI-judge run and Rish's quick review of it. They are Claude's drafting, not Rish's grading judgement, and stay proposals until he freezes the rubric.

- Rule 9. A page with no deliberate design choices grades 1 on D1, D2 and D3, and 2 on D4 if contrast passes and nothing clashes.
- Rule 10. Stand-in imagery (flat shapes, gradient blocks or grey boxes where the brief calls for pictures) caps D6 at 3 and does not lower H. Abstract shapes that are plainly the design are not stand-ins.
- Rule 11. If the 375 px view has content off the side of the screen or unreadable text, H is at most 3.
- Rule 12. Layout faults are graded in D2 only. D6 does not penalise them again.
- Rule 13. H assumes real images and copy are dropped in. Missing assets lower D6 only.
- H anchor 3 reworded from "About a day of fixes" to a day of design fixes, with real images and copy assumed.
- D6 look-for list now names stand-in imagery.
- Screenshot cap raised from 2400 px to 3200 px at 1280 wide, because the cap hid the related-stories block on one fixture.
- Measured facts: the lowest text contrast now names the element it belongs to. Code change in `scripts/capture.cjs`, no rubric effect.

## 0.1.0-draft, 2026-10-27

First draft. Holistic grade plus six dimensions with anchors at 1, 3 and 5.

## Phase C update, 2026-10-27 (late)

- Amendment 4: Lovable (6) and v0 (5) captured from temporarily published pages. Captured set is 24 of 30. Eleven items are judge-only.
- A capture run after unpublishing saved Lovable's placeholder page. Caught, republished, recaptured, judged again. The first judge pass on it was discarded.
