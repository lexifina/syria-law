# Structure of syria-law

Folder names are in Arabic, the language people search Syrian law in. Years and numbers use Western digits.
No folder holds more than 1,000 entries.

| Folder | What | One file is |
| --- | --- | --- |
| `الدستور-2012/` | The Constitution of 2012 | one article (`art-001.md`) |
| `الإعلان-الدستوري-2025/` | The Constitutional Declaration of 13 March 2025 | one article |
| `التشريعات/<السنة>/` | Laws, legislative decrees and decrees | one instrument (`<النوع>-<الرقم>.md`, e.g. `مرسوم-تشريعي-54.md`, `قانون-59.md`) |
| `data/`, `tools/` | Tables, charts and the tools to read the history | |

## Versions and dates

- One commit per instrument, in the order they took effect.
- The author date is 12:00 Damascus time on the in-force day the instrument's own clause gives (its issue day for
  "من تاريخ صدوره", its publication day for "من تاريخ نشره", or a stated day or delay). Before 1970 the date is
  1970-01-01 and the real day starts the subject.
- Trailers on every commit: `Kind:` (law, legislative-decree, decree, layout, documentation), `In-force:`,
  `In-force-basis:` (the clause and field the day comes from) and `Source:`.
- An instrument whose in-force day cannot be read is held, not committed.

## Sources

- The People's Assembly legislation database (parliament.gov.sy, node=201). The host no longer resolves (it is gone,
  not blocking), so the text is read from Internet Archive copies of its pages; each commit names the capture
  (`Source-status: Internet Archive copy of parliament.gov.sy`).
- The 2025 Constitutional Declaration from an official Syrian publication.

`constitution-2012/` was renamed `الدستور-2012/` on 2026-11-26 (a rename only; no text changed).
