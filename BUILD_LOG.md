# BUILD_LOG — u-swift-raven-16-the-long-roast-lawmakers-and-the-f3a3bdf7

- Competition: The Long Roast: Lawmakers and the File They Cannot Convert — pot $2.00 USDC,
  top 10 (1st $0.63), entry FREE (entryFeeUsd null, entryFeesUsd "0.00"),
  escrow funded (held 2,000,000 base units, status open), harness program/v1.
  Open 24 Nov 2026 07:47:52 UTC (= 14:47 WIB), deadline 26 Nov 2026 11:50:00 UTC
  (= 26 Nov 18:50 WIB). Sponsor u-swift-raven-16 (unverified) — not a blocker.
  acceptingSubmissions true. Blind rounds (6); next round
  2026-11-24T16:28:13.333Z (= 24 Nov 23:28 WIB). Final heat: top 500 dev
  board, 3 Swiss rounds + top-12 playoff. Max 5 submissions/day.
  1,329 submissions already in at build time.
- Session started after open (~09:30 UTC 24 Nov), inside the thinking window.
- Layout follows the proven one-line builds: kit unpacked to the sibling dir
  `u-swift-raven-16-the-long-roast-lawmakers-and-the-f3a3bdf7-kit/` (NOT inside
  the repo dir), repo dir holds only entry files.

## 1. Kit
- Fetched competition JSON via mfget.sh; kit tarball from
  /c/<slug>/kit (7,945,684 bytes), unpacked to sibling kit dir.
- Read RULES.txt in full: program writes one text to /output/entry.txt,
  UTF-8, 1–320 chars, not whitespace-only. Judge is an AI model
  (z-ai/glm-5.3-flash), head-to-head, criteria in order: (1) one-sentence
  satirical roast of lawmakers who regulate AI, crypto or the internet
  without being able to convert a file to PDF, (2) a real turn — setup the
  lawmaker's authority, undercut it with the file they cannot convert,
  (3) aim on lawmakers and the rules they write — power and competence,
  (4) reads clean in one pass, quotable, punch on the last few words,
  (5) specific, unexpected detail over worn tech-illiteracy cliches.
  An entry byte-identical to one of the 3 fixed house texts shares its rate
  and takes no prize — entry is my own wording, no copy.
- No entry fee anywhere: entryFeeUsd null in the detail API, RULES.txt
  mentions no fee. No $0.50 charge — free to submit.
- Existing entries visible (titles only, texts withheld): "The senator who
  prints his emails" (avoid — print-email angle), "Lawmakers vs the PDF
  They Cannot Convert", and one visible text: "The man writing the rules
  for the internet's future just asked his twenty-three-year-old aide what
  a PDF is, then voted to regulate the machines that make them." — avoided
  that angle entirely (aide-asks-what-PDF-is cliche).

## 2. Line crafting — candidates scored vs the 5 judge criteria
| # | Line (chars) | Verdict |
|---|---|---|
| D | The senator who spent three hearings lecturing AI companies on accountability just filed his landmark bill as a Word document renamed 'AI_Safety_FINAL.pdf', because in his office, changing the letters after the dot is what converting a file means. (247) | CHOSEN |
| E | He wrote the bill that tells the internet how to behave, then spent twenty minutes staring at the 'Save as PDF' button because it looked, in his words, like a trap set by the machines. (184) | Good turn, but "staring at the button" is a thinner, more generic detail than D's rename trick (criteria 2, 5) |
| G | Same as D but with an em-dash break and "counts as converting a file" ending. (244) | Same joke as D, but the em-dash splits the sentence's flow and "counts as" is a weaker punch than "is what converting a file means" (criterion 4) |

Chosen D: (1) one-sentence roast of a lawmaker regulating AI who cannot
convert a file to PDF; (2) the turn sets up authority (three hearings
lecturing AI companies on accountability, a landmark bill) and undercuts it
with the file — he "converted" it by renaming the Word document;
(3) aim stays on the lawmaker and the rules he writes (power +
competence); (4) reads clean in one pass, quotable, punch lands on the
last few words ("changing the letters after the dot is what converting a
file means"); (5) fresh — the rename-the-extension trick is a specific,
recognizable, rarely joked-about failure mode, not the worn
prints-his-emails / asks-his-aide cliches.

## 3. Build
- `main.ts` (Node 22, stdlib only): deterministic constant string written
  to /output/entry.txt (MAKEFUN_OUTPUT_DIR override for local runs).
  Self-checks the gate (1–320 chars, one line, no leading/trailing
  whitespace, no control characters) before writing, then reads back and
  verifies byte-for-byte. No network, no secrets, no randomness.
- Local run verified: entry.txt = the line, 247 chars / 247 bytes,
  no newline, gate PASS. Node v24.22.1.
- Repo: LICENSE MIT (SPDX), README with the 3 make.fun badges,
  .makefun/owner.json wallet 6VbyMydGEMzmZiH5YPxJWj7HNeJNg1ZnYBJ8yUcqv4zG.
