---
name: literature-note
description: Turn a paper, report, book chapter or press release into a structured literature note (one note per source) saved in the Research folder of the user's Obsidian thesis vault, using a fixed template with source quality rating, verbatim quotes with page numbers, and sections on how the source fits the user's paper. Use this whenever the user shares or points to a PDF, DOI, URL or pasted text of a source and wants it summarised, excerpted, "noted", "logged", added to their research/literature, or asks "what does this paper say and can I use it" — even if they don't say "literature note".
---

# Literature note

Turn one source into one literature note in the vault's `Research` folder. The note is a working document for writing a paper: the user will later quote from it and cite from it without reopening the source. That is why accuracy matters more than completeness. A missing finding costs the user a few minutes; an invented finding or a misquoted sentence can end up in a submitted paper.

## Where things go

- **Research folder:** the `Research` folder in the current project (vault) root, e.g. `<your project folder>/Research`. If there's no such folder, ask before creating one elsewhere.

- **Filename:** `author-year-short-title.md`, lowercase kebab-case, first author's surname only (e.g. `hughes-2011-70-percent-change-failure.md`). If a file with that name already exists, show the user and ask whether to update it or save under a new name. Never overwrite silently.
- **Paper context:** before filling in the "my paper" sections, skim what the paper is about: `Manuscript/` (Introduction, Literature Review, Abstract) and other notes in `Research/`. If the manuscript is still mostly template text, say so in those sections rather than guessing at a research question the user hasn't written down.

## Workflow

1. **Get the full text.** Read the PDF/file/URL the user gives you. For PDFs longer than 20 pages, read in page ranges until you've covered the whole thing. If you can only reach part of the source (abstract only, paywall, press release instead of the full report), carry on but say so in **Source Quality** and in **Open questions / to verify**. Every section of the note is then limited to what you actually read.
2. **Identify the bibliographic facts** from the source itself (title page, header, imprint, DOI). Don't fill gaps from memory: if the year, issue or pages aren't in the document, write `[not stated in source]` and add it to the to-verify list.
3. **Collect quotes while reading**, copying them character for character together with their page number (see rules below).
4. **Write the note** using the template exactly.
5. **Save** it and tell the user the file path, plus anything you couldn't access or verify.

## Template

Use exactly this structure: same headings, same order, same bold labels. Don't add, rename or drop sections. If a section has nothing to say (e.g. no limitations stated), keep the heading and write so, e.g. "The authors don't discuss limitations. My own observations: ..."

```markdown
# <Author> (<Year>): <Short title>

**Source:** full reference + link
**Type:** peer-reviewed / consultancy report / book / press release
**Source Quality:** high / medium / low — brief justification

## Research question
## Method and data
## Key findings
## Limitations
## Quotes
> "exact quote" (p. X)

## How I can use it in my paper
## Open questions / to verify
## Relevance for my paper
```

Filling it in:

- **Title line:** `<Author>` is the surname of the first author, with `& Surname` for two authors and `et al.` for three or more; for an organisation without named authors, the organisation (e.g. `McKinsey & Company`). Short title: a few words.
- **Source:** a full APA 7 reference, with the DOI as `https://doi.org/...` or the URL.
- **Type:** pick one of the four. If none fits (working paper, thesis, government report), use the nearest one and add the real type in brackets, e.g. `consultancy report (industry white paper)`.
- **Source Quality:** written as `high — ...`, `medium — ...` or `low — ...` (the rating, an em dash, then one sentence on why). Consider peer review, transparency of method, sample size, conflict of interest (e.g. a consultancy selling transformation services), and whether you read the full text.
- **Research question / Method and data / Key findings / Limitations:** your own summary in your own words. Prefer bullet points. Include numbers (sample size, percentages, time period) where the source gives them, since those are what the user will cite. For Limitations, keep the authors' stated limitations apart from your own critique, e.g. "Stated by authors: ..." and "My assessment: ...".
- **Quotes:** 3–6 quotes that the user might actually use: key findings, definitions, strong claims.
- **How I can use it in my paper:** concrete uses, e.g. "supports the claim in the introduction that...", "counter-evidence to...", "definition of X for section Y".
- **Open questions / to verify:** a checklist (`- [ ]`) of what the user should check before citing: parts you couldn't access, missing bibliographic details, claims the source makes without evidence, secondary citations the source relies on.
- **Relevance for my paper:** a rating (high / medium / low) and one or two sentences on why.

## Rules on quotes and summaries

These rules exist because the user will copy quotes from this note straight into the paper.

**Quotes are word for word.** Copy the exact wording, spelling (including British/American spelling), capitalisation and punctuation of the source. Don't fix typos, don't join sentences from different places, don't shorten without marking it. Mark an omission with `[...]` and your own insertion with `[square brackets]`. If PDF extraction garbles the text (broken hyphenation, ligatures, missing characters) and you can't be sure of the exact wording, leave the quote out, or include it and flag it in Open questions ("check wording against the PDF").

**Every quote gets a page number, and page numbers are never guessed.**
- Use the page number printed on the page (e.g. journal pagination `p. 455`), not the PDF viewer's page count. If they differ, use the printed one.
- Quotes that run across pages: `(pp. 455–456)`.
- If the source has no page numbers (web pages, HTML reports, many press releases), write `(no page number)`, adding the section heading where there is one to help find it again: `(no page number; section "Key findings")`.
- If you can't tell which page a passage is on (e.g. text extracted without page breaks), write `(page number unclear)` and add it to Open questions. Don't estimate.

**Keep quotes and summary apart.** Quotation marks appear only in the Quotes section and only around the source's exact words. The other sections are your paraphrase and contain no quotation marks around source text, so the user can always tell whose words they're reading. When you need to name one of the source's own terms elsewhere (e.g. *automation leaders*), put it in italics rather than quotation marks. If a paraphrase closely follows one passage, add its page in brackets, e.g. `(p. 457)`, but still in your own words.

**Never invent anything.** Every finding, number, method detail and limitation in the note must be in the source you read. Don't add findings you remember from elsewhere about this paper or topic, don't round or recalculate numbers without saying so, and don't turn a hedged claim ("may be associated with") into a firm one ("causes"). Your own interpretation belongs in "How I can use it", "Relevance", or clearly labelled as "My assessment:". If you're unsure whether the source really says something, leave it out or put it in Open questions.
