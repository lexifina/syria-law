# How this repository was made (Syria)

This file is written by the build on 2026-10-28, the day the source data was retrieved.

## Sources

| Source | Address | Retrieved | Licence |
| --- | --- | --- | --- |
| People's Assembly of the Syrian Arab Republic, 'الدستور السوري' page, via Internet Archive | <http://parliament.gov.sy/arabic/index.php?node=5518&cat=423&> | 2026-10-28 | Official legislative text (no licence stated); Internet Archive captures 20150428001050 and 20241207201658 |

Every word of law in this repository comes from these sources. Lexifina reads them and records each act's dated versions, and the laws that made each change, in one corpus file. This repository is built from that file.

## What is in it

| Act | Title | Versions | Span |
| --- | --- | ---: | --- |
| `constitution-2012` | دستور الجمهورية العربية السورية 2012 | 1 | 2012-02-27 to 2012-02-27 |

The build made 1 commits:

| Commits | Kind |
| ---: | --- |
| 1 | first version of an act |
| 0 | one law on its in-force day |
| 0 | changes no amendment note explains, credited to the publisher |

Other counts:
- 0 commits on the branch `future`: laws not yet in force on 2026-10-28.
- 0 commits dated 1 January 1970: in force before 1970, with the real day in their `In-force` trailer.
- 1 laws in the record.
- 1 tags.

## Dates

Each commit is dated at noon (Asia/Damascus) on the day the change took effect. The other dates, enacted and published, are trailers.

When a law gives no date of its own, the default rule applies: Each text names its own in-force day; Decree 94 of 2012 art. 1: the Constitution is in force from 27 February 2012 http://parliament.gov.sy/arabic/index.php?node=5518&cat=423&

## How the history is built

`tools/build.py` turns the corpus into this history in one pass: one commit per law, on the day it took effect. The same corpus always gives the same commit hashes. `tools/check_repo.py` reads every version back from git and compares it with the corpus. `tools/on.py` shows the law as it stood on any date. The corpus format is described in `tools/SCHEMA.md`.

- Corpus: sha256 `be5294c9296e66ab6555765b1c8684450911eb55a05708ab2fb450edb13b7777` (90960 bytes).
- Builder blob hashes (`git hash-object`): `build.py` `a4faa25af85facb64b956b372f6b528aafdd7ec1`, `check.py` `3e59cb6f05eccb94a9ec14431a7f6781221e83ef`, `on.py` `644a6c0857fbcc72562032b58d57aa113fee0641`.
- Python 3.12.10; git version 2.46.0.windows.1.

## Checks

Not yet run for this build.

No second build of this corpus has been compared yet.

## Decisions made by hand

- Phase 1 Constitution: the 2012 text from the People's Assembly page, read from the Internet Archive capture of 7 December 2024 (the last before 8 December 2024); the 28 April 2015 capture was compared: 0 units differ (none).
- first_law is null: the site gives no amendment history, so the one version is "oldest version available", credited to the publisher and dated 27 February 2012 from Decree 94 of 2012 art. 1 as printed on the page.
- Part and chapter headings (الباب, الفصل) and the printed index are dropped; the preamble is its own unit; the uploader line after the text is dropped.
- Not yet modelled: the end of the 2012 Constitution in 2025 and the Constitutional Declaration of 13 March 2025 (no official text fetched yet).

## What AI did and did not do

The scripts that read the sources and build this repository were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- Claude Code (claude-opus-5-5) wrote Lexifina's code; no model wrote or edited legal text.
