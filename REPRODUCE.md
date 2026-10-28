# How this repository was made (Syria)

This file is written by the build on 2026-10-28, the day the source data was retrieved. Everything below is enough to rebuild this repository hash for hash.

## Sources

| Source | Address | Retrieved | Requests | Licence |
| --- | --- | --- | ---: | --- |
| People's Assembly of the Syrian Arab Republic, 'الدستور السوري' page, via Internet Archive | <http://parliament.gov.sy/arabic/index.php?node=5518&cat=423&> | 2026-10-28 | 2 | Official legislative text (no licence stated); Internet Archive captures 20150428001050 and 20241207201658 |

Every response is cached by the sha256 of its URL, and the table above lists every source with its retrieval date. Lexifina keeps its fetch scripts privately; `tools/parse.py` reads only the cache and writes `corpus.json`, so the same cache always gives the same corpus.

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

## Commands, in order

```sh
# fill the cache from the sources listed above (network; Lexifina's fetch scripts are kept privately)
python -X utf8 tools/parse.py                  # cache -> corpus.json (no network)
python -X utf8 tools/build.py <folder> --repo <empty folder> --docs-date 2026-10-28
python -X utf8 tools/check_repo.py <repo> --corpus <folder>/corpus.json --write
python -X utf8 tools/build.py <folder> --repo <another empty folder> --docs-date 2026-10-28 --compare <repo>
```

In the main Lexifina repository these files live as follows:
- `fetch.py`, `parse.py` and `repo/`: in `scripts/syria-law/`.
- `build.py`, `check_repo.py` (`check.py` there) and `on.py`: in `scripts/gitlaw_common/`, with the corpus format in `SCHEMA.md`.

## Exact inputs

- `corpus.json` sha256 `18811ecf5f391dfe10bc4d14e1b16c4ca8cf35486d222ae507e6cf3da93040ea` (90095 bytes)
- Script blob hashes (`git hash-object`):

| Script | Blob |
| --- | --- |
| build.py | `2bfc4ac9df193a7be844556d7f69cdb9d93ec3f2` |
| check.py | `cd346c7ff9996d450240e3bab52bcae03b2bc865` |
| on.py | `644a6c0857fbcc72562032b58d57aa113fee0641` |
| fetch.py | `30ca3f332afc18b18d655774ea110e611a87220b` |
| parse.py | `b4d3c173425183c42ab18dbe20e2b6c7ee479bcd` |

- Tools:
  - Python 3.14.0
  - git version 2.52.0.windows.1
  - curl 8.21.0 (Windows) libcurl/8.21.0 Schannel zlib/1.3.2 WinIDN WinLDAP

## Checks

1 versions of 1 acts read back from git on the day each took effect and on the day before: 0 mismatches. Trailers: 0 commits whose trailers git cannot parse. Health: 0 merge commits on main, 0 commit dates that go backwards, 0 commits dated after the build.

Not yet run for this build.

These results are from the check run on the build before this one, from the same corpus.

## Decisions made by hand

- Phase 1 Constitution: the 2012 text from the People's Assembly page, read from the Internet Archive capture of 7 December 2024 (the last before 8 December 2024); the 28 April 2015 capture was compared: 0 units differ (none).
- first_law is null: the site gives no amendment history, so the one version is "oldest version available", credited to the publisher and dated 27 February 2012 from Decree 94 of 2012 art. 1 as printed on the page.
- Part and chapter headings (الباب, الفصل) and the printed index are dropped; the preamble is its own unit; the uploader line after the text is dropped.
- Not yet modelled: the end of the 2012 Constitution in 2025 and the Constitutional Declaration of 13 March 2025 (no official text fetched yet).

## What AI did and did not do

The fetch, parse and check scripts were written by Claude Code running Claude Opus 5.5 (`claude-opus-5-5`) under Lexifina's direction.

No model wrote, translated or corrected legal text. No model runs at build time. Every word of law in this repository comes from the official sources above, through code that anyone can rerun.

The commit messages are written by `build.py` from the source data.

Model use at data-build time:
- Claude Code (claude-opus-5-5) wrote fetch.py and parse.py; no model wrote or edited legal text.
