# Generated-UI design rubric

A written, anchored rubric for the visual design of user interfaces that AI tools generate from a prompt, six frozen prompts, and one set of grades. **The grades are an AI judge's. The author reviewed 11 of the 24 and agreed with all of them; the other 13 are not reviewed. They are not independent expert grades.** The set is **24 of 30 planned slots**. It grades visual design only, and it does not rank the tools.

## Why it exists

UI-Bench (arXiv 2508.20410) asks designers one question, "Which project would you be more likely to deliver to a client?", and says it captures holistic judgement "without a rigid rubric". TASTE (arXiv 2605.20731) has nine named criteria, for AI-generated graphic design such as logos and posters. FlowEval (arXiv 2605.04165v1) grades interaction flows and says it "focuses primarily on task support". Design Theater (arXiv 2607.22928) says its metrics "do not capture aesthetic judgment". This rubric is an attempt at the missing piece: a written rubric with anchored levels for the visual craft of generated, coded interfaces. Quotes were read from the papers' own pages on 2026-10-27.

## The rubric (version 0.2.0, frozen 2026-10-27)

Whole numbers 1 to 5, with anchors at 1, 3 and 5. Give the holistic grade first, then the six dimensions. Full text with anchors and thirteen rules: [rubric/RUBRIC.md](rubric/RUBRIC.md).

| | Name | Question |
|---|---|---|
| H | Client-ready | Would you deliver this to a client as it stands? |
| D1 | Hierarchy | Where does the eye go first, second and third, and does that order match what the page is for? |
| D2 | Layout and spacing | Are alignment, grid, spacing and density consistent, at both widths? |
| D3 | Typography | Do scale, weight, pairing, line length and line spacing make the text easy and pleasant to read? |
| D4 | Colour and contrast | Is the palette cohesive and restrained, does colour have a job, and is text legible against its background? |
| D5 | Brief fit and distinctiveness | Does it look made for this brief, or for any brief? |
| D6 | Finish | How complete and consistent is it in the small things: content, imagery, icons, components, edges? |

SHA-256 of `rubric/rubric.json`: `439cb9db9074e29a716211893512d035dd98e990d83e2f6f7bb8210a8621bd96`. SHA-256 of `data/prompts.json`: `a64ca95d53175a454494211c5f66b158f43cde5e627fb65d7531cc70ebfad4ce`. A hash on a laptop proves nothing to a stranger by itself. It becomes evidence when something outside the author's machine records it, and the date of this repository's first release is the latest date it could have existed.

## The grades

Seven rows per item, as the judge gave them. A dash means the judge could not tell. There are no tool averages and no ranking on purpose: the set is too small and the grades are one judge's.

| Prompt | Tool | H | D1 | D2 | D3 | D4 | D5 | D6 | Author reviewed |
|---|---|---|---|---|---|---|---|---|---|
| P1 marketing page | Bolt | 3 | 4 | 3 | 4 | 3 | 4 | 3 | yes |
| P1 marketing page | ChatGPT | 4 | 4 | 4 | 4 | 3 | 4 | 4 | yes |
| P1 marketing page | Claude | 4 | 4 | 4 | 4 | 4 | 4 | 3 | yes |
| P1 marketing page | Lovable | 4 | 4 | 4 | 4 | 4 | 3 | 4 | no |
| P1 marketing page | v0 | 4 | 4 | 4 | 4 | 4 | 4 | 3 | no |
| P2 dashboard | ChatGPT | 3 | 3 | 2 | 4 | 3 | 3 | 3 | no |
| P2 dashboard | Claude (Claude Code subagent) | 4 | 4 | 3 | 3 | 4 | 4 | 4 | no |
| P2 dashboard | Lovable | 4 | 4 | 3 | 4 | 3 | 3 | 3 | no |
| P2 dashboard | v0 | 4 | 4 | 4 | 3 | 3 | 3 | 4 | no |
| P3 product page | ChatGPT | 4 | 4 | 3 | 4 | 3 | 4 | 4 | yes |
| P3 product page | Claude | 3 | 4 | 4 | 4 | 3 | 3 | 2 | yes |
| P3 product page | Lovable | 4 | 4 | 4 | 4 | 4 | 4 | 4 | no |
| P3 product page | v0 | 4 | 4 | 4 | 4 | 4 | 3 | 4 | no |
| P4 pricing page | ChatGPT | 3 | 4 | 3 | 4 | 4 | 3 | 4 | yes |
| P4 pricing page | Claude | 4 | 4 | 4 | 4 | 4 | 3 | 4 | yes |
| P4 pricing page | Lovable | 3 | 4 | 2 | 4 | 4 | 3 | 4 | no |
| P5 portfolio | ChatGPT | 3 | 4 | 3 | 4 | 4 | 4 | 3 | yes |
| P5 portfolio | Claude | 3 | 4 | 4 | 4 | 4 | 4 | 2 | yes |
| P5 portfolio | Lovable | 4 | 4 | 3 | 4 | 4 | 4 | 4 | no |
| P5 portfolio | v0 | 4 | 4 | 4 | 5 | 4 | 4 | 4 | no |
| P6 editorial article | ChatGPT | 4 | 5 | 4 | 5 | 4 | 4 | 4 | yes |
| P6 editorial article | Claude | 4 | 4 | 4 | 5 | 4 | 4 | 2 | yes |
| P6 editorial article | Lovable | 4 | 4 | 4 | 5 | 4 | 4 | 4 | no |
| P6 editorial article | v0 | 4 | 4 | 4 | 3 | 3 | 4 | 4 | no |

Data, reasons, measured facts (font counts, lowest contrast, overflow at 375 px, defect flags) and per-item notes: [data/grades.json](data/grades.json). The six prompts: [data/prompts.json](data/prompts.json).

## What was not captured

- **v0** (1 slot): P4 was published for capture, but the deployment held no files and returned a 404. Nothing could be captured.
- **Bolt** (5 slots): P2 renders blank offline because it needs a backend. P3 to P6 were blocked by the free token cap and were not paid for.

## How it was made, and what to distrust

- The prompts were frozen before any run. Each was typed into a fresh chat or project, the first output was taken, and there was no follow-up. Where a tool asked clarifying questions (Bolt), the only answer was to skip them.
- **The runs were done by an AI agent driving the author's logged-in browser, not by hand.** Anthropic's consumer terms, OpenAI's terms and Lovable's terms prohibit automated access. The author chose this and carries the account risk.
- Lovable and v0 gave no usable export on the free plans used, so the author published those outputs on his own accounts for a short time, they were captured from the public pages, and the Lovable pages were then taken down. The v0 pages were left up. The published Lovable pages carry a small "Edit with Lovable" badge, so those six items are not fully blind to the tool. This is Amendment 4 in [PROTOCOL.md](PROTOCOL.md).
- Claude P2 and ChatGPT P2 deviate from the frozen protocol, in ways recorded in [PROTOCOL.md](PROTOCOL.md) (Amendment 3) and in the data.
- The Claude runs on claude.ai were routed by the product to Claude Design. That is a different surface from plain chat.
- The judge was a fresh Claude agent given only the rubric and the screenshots. The author saw its numbers before reviewing them, so his agreement is anchored. Uniform agreement with no notes is sign-off, not an independent grading. Two judge passes were thrown away: one ran on screenshots with two capture defects, and one graded Lovable's "unpublished" placeholder page by mistake. The grades cluster at 3 and 4, so a one-point difference between two items is within what the judge itself marked unsure.
- Screenshots are not published. Several outputs include third-party photographs, and the author could not clear them. Everything here is reproducible from the prompts, the tool and the date, and the outputs change over time.
- The author is a design studio owner. The studio sells design and AI-search work. This rubric sells nothing.

## What this is not

Not a benchmark, a leaderboard or a scorer. Not a claim about which tool is best. Not a dataset to train on: some tools' terms restrict using their output to train competing models, and nothing here is offered for that.

## Cite

```
Rish Sadh, "Generated-UI design rubric", version 0.2.0, 2026. https://github.com/rishsadh/generated-ui-rubric. Rubric and data CC BY 4.0.
```

`CITATION.cff` carries the same. DOI for all versions: [10.5281/zenodo.23689021](https://doi.org/10.5281/zenodo.23689021). This release (v0.2.0): [10.5281/zenodo.23689022](https://doi.org/10.5281/zenodo.23689022).

## Licence

Rubric text, prompts, grades and notes: CC BY 4.0. Code in `scripts/`: MIT. Nothing here claims rights in any tool's output. See [LICENSE](LICENSE).
