# literature-note

A [Claude Code skill](https://code.claude.com/docs/en/skills) that turns a paper, report, book
chapter or press release into a structured literature note, saved as one note per source in the
`Research` folder of an Obsidian-based writing vault (built for [Obsitex](https://www.obsitex.com/)
projects, but not dependent on it).

Built with [skill-creator](https://github.com/anthropics/skills), Anthropic's official skill for
building skills.

## Why

A literature note is a working document: you quote and cite from it later without reopening the
source. That makes accuracy more important than completeness. This skill enforces a fixed template
and a few hard rules so that every note stays reliable enough to cite from directly:

- Quotes are copied word for word, always with a page number, never guessed.
- Summary sections and quotes are kept strictly apart, so you can always tell whose words you're
  reading.
- Nothing is invented. If a claim, number or page isn't in the source, the note says so instead of
  filling the gap.
- Source quality (peer-reviewed, consultancy report, press release, ...) is rated and justified,
  not just filed away.

## Install

Copy `SKILL.md` into `~/.claude/skills/literature-note/` (or your project's `.claude/skills/`
folder).

## Use

Point Claude at a PDF, DOI, URL or pasted text of a source, e.g.:

```
Make a literature note from this paper for my thesis: <file or link>
```

The skill also triggers on phrasing like "summarise this", "log this source" or "what does this
paper say and can I use it", without needing the words "literature note".

## Template

Every note follows the same structure: bibliographic facts, source quality rating, research
question, method, findings, limitations, verbatim quotes with page numbers, how the source fits
your own paper, and an open-questions checklist to verify before citing. The full template and
rules are in [SKILL.md](SKILL.md).

## Evals

[`evals/evals.json`](evals/evals.json) has two test cases (one source with page numbers, one
without) checking that the skill follows the template and never guesses a page number.

## Status

I built this for my own workflow, to match my personal literature note template exactly. It's
intentionally simple and only checked against the two eval cases and my own use, so there's
plenty of room to make it more robust (better handling of edge cases, more source types, more
tests). Feel free to fork it and adjust the template or rules to your own needs.
