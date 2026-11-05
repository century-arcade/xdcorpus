# The xd Crossword Corpus

The xd Crossword Corpus is a collection of more than 160,000 published crosswords
from over 160 publications (as of November 2026), from 1913 to today, kept in a plain-text format for
research and preservation. Every puzzle is stored as one [`.xd` file](https://github.com/century-arcade/xdformat)
holding its grid, clues, answers and publication details, together with a record
of where it came from.

The corpus is maintained by Saul Pwanson and Alex DeJarnatt as a volunteer
project of [Century Arcade](https://github.com/century-arcade).

## Explore

- [The Cross(word) Reference](https://crosswordreference.com): browse and search puzzles,
  clues and answers across the corpus.
- [xd.saul.pw](https://xd.saul.pw): statistics, reports and corpus-wide analyses,
  rebuilt nightly.

## Use the corpus

Many of the puzzles are still under copyright by their publishers and constructors, so the corpus
itself is not public. It is available for research, in forms ranging from
aggregate statistics to derived datasets to the full collection. See
[ACCESS.md](ACCESS.md) for what data is available, how to ask, and the terms of use.

## Contribute puzzles

We welcome puzzles from any publication that meets the collection scope in
[COLLECTION.md](COLLECTION.md): American-style crosswords, made by a person,
part of a published series. If you edit, construct or publish crosswords,
[CONTRIBUTING.md](CONTRIBUTING.md) says what we do with puzzles we are given,
who can see them, and what to send. Send puzzles, or questions, to
xd@saul.pw. Volunteers who want to convert and submit puzzles themselves
are welcome too; see the end of that page.

## Policies

- [CONTRIBUTING.md](CONTRIBUTING.md): what happens to puzzles you give us,
  and what to send.
- [COLLECTION.md](COLLECTION.md): what the corpus collects.
- [EDITORIAL.md](EDITORIAL.md): what a corpus puzzle contains and how it is
  represented.
- [ACCESS.md](ACCESS.md): who may use the corpus, how, and on what terms.
- [PRESERVATION.md](PRESERVATION.md): how the corpus is kept, and what we
  commit to.
- [GOVERNANCE.md](GOVERNANCE.md): who maintains the corpus and how decisions are
  made.
- [DECISIONS.md](DECISIONS.md): a dated log of decisions.
- [assessments/](assessments/): yearly self-assessments of the project's
  preservation capability.

## The parts

| | |
|---|---|
| [xdformat](https://github.com/century-arcade/xdformat) | The `.xd` file format specification, and converters from `.puz` and `.ipuz`. |
| [xd](https://github.com/century-arcade/xd) | The pipeline that imports, checks and analyzes the corpus, and builds xd.saul.pw. |
| The corpus | The corpus itself: a private repository, with the provenance of every puzzle. Access on request. |
| [The Cross(word) Reference](https://crosswordreference.com) | Browsing and search. |
| [Every Puzzle Project](https://github.com/EveryPuzzleProject) | A sister project digitizing historical crosswords from scans, which feeds the corpus. |

## Citing

If you publish research or results that use the corpus, please cite it:

> Pwanson, Saul and DeJarnatt, Alex. (2026). *The xd Crossword Corpus.*
> Century Arcade. https://github.com/century-arcade/xdcorpus

Use the year the corpus was accessed. Earlier work cited it as
"Pwanson, Saul. (2019). xd Crossword Corpus. http://xd.saul.pw"; that is the
same corpus.

## Contact

Open an issue in this repository, or find us on the Crossword Discord.


## Acknowledgments

We owe a debt of gratitude to:

- Barry Haldiman, for his diligent collection of thousands of puzzles from the 2000s and 2010s
- David Steinberg and the [Pre-Shortzian Puzzle Project (PSPP)](https://www.preshortzianpuzzleproject.com/), for inspiration
- Parker Higgins, for developing and maintaining [xword-dl](https://github.com/thisisparker/xword-dl), which has been indispensable for collection
- The hundreds of editors and thousands of constructors who delight us with their creations.
- [Arthur Wynne](https://tcampbell.substack.com/p/arthur-wynne), for kicking the whole thing off on December 21, 1913.
