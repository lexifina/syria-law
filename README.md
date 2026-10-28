# Syria: law history in git

The law of Syria (SY) as a git history: one file per provision, one commit per law on the day it took effect, and the law that made the change as the commit author. It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law), which places it at `sy/`.

**First build, deliberately small.** Language: Arabic (the official language), so the text is right-to-left.

| Folder | Text | Versions | History |
| --- | --- | ---: | --- |
| `constitution-2012/` | Constitution of the Syrian Arab Republic, 2012 (preamble and 157 articles) | 1 | Oldest version available: the text published by the People's Assembly, in force from 27 February 2012 (Decree 94 of 2012) |

**This constitution is no longer in force.** After the fall of the previous government on 8 December 2024, the 2012 Constitution was replaced in 2025: the Constitutional Declaration of 13 March 2025 set out the transitional order. This repository records the 2012 text as the last constitution the People's Assembly published, with its in-force date. The 2012 text is read from Internet Archive captures of the People's Assembly page (28 April 2015 and 7 December 2024, the last before 8 December 2024); the two captures give the same words.

**Why only this.** The People's Assembly site does not answer from where this was built, so the text could not be compared with the live page, and no other official Syrian source with plain text of the laws was found. No dated past versions exist online for the 2012 text.

**Source:** [People's Assembly of the Syrian Arab Republic](http://parliament.gov.sy/arabic/index.php?node=5518&cat=423&), official, read through the Internet Archive, retrieved 28 October 2026. See `LICENSE` and `REPRODUCE.md`.

Dates are the day the change took effect. This repository is not legal advice; for anything that matters, read the original.
