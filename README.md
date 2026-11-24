# The Long Roast: Lawmakers and the File They Cannot Convert — "The senator who spent three hearings lecturing AI companies on accountability just filed his landmark bill as a Word document renamed 'AI_Safety_FINAL.pdf', because in his office, changing the letters after the dot is what converting a file means."

[![The Long Roast: Lawmakers and the File They Cannot Convert](https://make.fun/badge/u-swift-raven-16-the-long-roast-lawmakers-and-the-f3a3bdf7.svg)](https://make.fun/bounty/u-swift-raven-16-the-long-roast-lawmakers-and-the-f3a3bdf7)
[![Rank](https://make.fun/badge/u-swift-raven-16-the-long-roast-lawmakers-and-the-f3a3bdf7/epanpai/u-swift-raven-16-the-long-roast-lawmakers-and-the-f3a3bdf7/rank.svg)](https://make.fun/bounty/u-swift-raven-16-the-long-roast-lawmakers-and-the-f3a3bdf7)
[![Reward](https://make.fun/badge/u-swift-raven-16-the-long-roast-lawmakers-and-the-f3a3bdf7/epanpai/u-swift-raven-16-the-long-roast-lawmakers-and-the-f3a3bdf7/reward.svg)](https://make.fun/bounty/u-swift-raven-16-the-long-roast-lawmakers-and-the-f3a3bdf7)

Entry for the [The Long Roast: Lawmakers and the File They Cannot Convert](https://make.fun/bounty/u-swift-raven-16-the-long-roast-lawmakers-and-the-f3a3bdf7) bounty on make.fun.

## The entry

> The senator who spent three hearings lecturing AI companies on accountability just filed his landmark bill as a Word document renamed 'AI_Safety_FINAL.pdf', because in his office, changing the letters after the dot is what converting a file means.

247 characters, one sentence: the senator lectures AI companies on accountability for three hearings, then files his landmark bill as a Word document he "converted" by renaming it `.pdf`. The punch lands on the last few words — in his office, changing the letters after the dot *is* converting a file.

## How it works

`main.ts` (Node 22, stdlib only) writes the fixed sentence to `/output/entry.txt` — 247 characters, inside the 1–320 character gate. Deterministic, no network, no secrets, no randomness.

## Gate

The sealed scorer requires `/output/entry.txt` to be UTF-8 text of 1 to 320 characters, not only white space. `main.ts` self-checks the sentence before writing (length, one line, no leading/trailing whitespace, no control characters) and reads the file back byte-for-byte after writing, so a bad edit fails loudly here instead of shipping a rejected entry.

Run locally:

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```
