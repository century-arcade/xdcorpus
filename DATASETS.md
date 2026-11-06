# Datasets

*Draft, November 2026. Marked **[practice]** where it describes what we
already publish, **[proposed]** where it is new.*

## Purpose

Most puzzles in the corpus are under copyright, and we do not publish them
(see [ACCESS.md](ACCESS.md)). Much research does not need whole puzzles: it
needs the words, the clues, who edited what and when. We publish data
derived from the corpus so that this research can happen without anyone
having to ask, and without redistributing anyone's puzzles.

The principle behind every public dataset: **nothing we publish lets a
copyrighted puzzle be rebuilt**, alone or combined with our other public
data.

## Three tiers

### (a) Public full content

Complete puzzles that are out of copyright:

- puzzles published before 1929, which are in the public domain in the
  United States; **[proposed]**
- the 5,688 puzzles published before 1965 (5,633 from the New York Times,
  1942 to 1964, with the 1924 Simon & Schuster books and some early
  newspaper puzzles), which we believe are in the public domain because
  their copyrights were not renewed, published as the
  `puzzles-pre1965` release of
  [century-arcade/xd](https://github.com/century-arcade/xd/releases);
  **[practice]**
- puzzles from *Judge* magazine digitized by the
  [Every Puzzle Project](https://github.com/EveryPuzzleProject).
  **[proposed]**

Anyone can download them, from GitHub releases and Hugging Face.

### (b) Public derived data

- **Clues and answers** (`clues.tsv` in `xd-clues.zip`): one row per clue,
  with publication, year, answer and clue. **[practice]**
- **Puzzle metadata** (`xd-metadata.zip`): `puzzles.tsv` (identifier, date,
  size, title, constructor, editor, copyright line), `stats.tsv` (puzzle
  counts by publication, year and weekday) and `similar.tsv` (for each
  puzzle, how much of its grid and clues match earlier puzzles).
  **[practice]**
- **Answer lexicon by year**: each answer with its number of uses per
  publication-year. **[proposed]**
- **Grid statistics**: size, block count, word count and word lengths,
  without the grid itself. **[proposed]**

Anyone can download them, today from [xd.saul.pw/data](https://xd.saul.pw/data),
and from Hugging Face once it is set up.

### (c) Gated

Full modern puzzles, and researcher samples drawn from them (see "Samples"
in [ACCESS.md](ACCESS.md)). These are published on Hugging Face as a gated
dataset: each person asks, a maintainer approves them by name, and the
[ACCESS.md](ACCESS.md) terms apply. This is the same process as a request by
email, with a form; approval is personal and is recorded in the same way.
**[proposed]**

## Rules for derived data

Every tier (b) dataset follows these rules. **[proposed]** except where
marked.

- **No grids, no clue numbers.** A clue row does not say where its answer
  sits in a grid, or which clue it was. **[practice]**
- **Year, not date.** Clue rows carry the year of publication and nothing
  finer. **[practice]**
- **Rows are reordered within each publication-year.** The order of a
  puzzle's clues does not survive; today the rows of each publication-year
  are sorted by answer and clue. **[practice]**
- **Contest puzzles with redacted grids are left out.** Their clues are not
  published, so a contest is not spoiled before its answers are. **[practice]**
- **A minimum cell size.** A publication-year with fewer than 5 puzzles is
  too small to hide which clue came from which puzzle. Its rows are merged
  into a coarser cell (the publication's decade) or dropped. The threshold
  of 5 is a proposal for the maintainers to settle.
- **A coverage table.** Coverage is very uneven: some publications are
  complete for decades, others are a handful of puzzles. Every dataset card
  carries a table of puzzle counts by publication and decade, so users do not
  mistake the corpus for a sample of all crosswords.

Metadata in `puzzles.tsv` is per puzzle and carries full dates; it contains
no clues, answers or grids beyond the first across and down answers used as
a grid hash. **[practice]**

## Where and how

- **Hugging Face** is the primary venue, under one organization (name to be
  decided; we propose `xdcorpus`). It holds tier (a), tier (b) and the gated
  tier (c). **[proposed]**
- **Snapshots, not streams.** Hugging Face datasets are versioned snapshots,
  published quarterly, not rebuilt nightly, so that a result can name the
  version it used. **[proposed]**
- **Zenodo** holds one record for the corpus as a whole, with a DOI for
  citing it, pointing at the corpus page. **[proposed]**
- **GitHub releases** keep the public-domain puzzle sets, as they do now.
  **[practice]**
- **Kaggle**, later, only as a mirror of tier (b). **[proposed]**

Every dataset card states the terms in one paragraph, links to this document
and to [ACCESS.md](ACCESS.md), says how to cite the corpus (see
[README.md](README.md#citing)), and carries the coverage table.
**[proposed]**

## Publishers and constructors

Publishers and constructors can ask for their puzzles to be removed from
tier (a) or tier (c), as described in [CONTRIBUTING.md](CONTRIBUTING.md).
The puzzles are removed from the next snapshot, and gated users are asked to
delete their copies.

A tier (b) row cannot be traced to one puzzle, so there is nothing
puzzle-level to remove. A publication can still ask to be left out of
future snapshots, and we will do so. Snapshots already published stay as
they are. **[proposed]**

## Review

This policy is reviewed once a year with the other policies and the
preservation assessment. Changes are logged in [DECISIONS.md](DECISIONS.md).
