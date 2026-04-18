# IIOC Person Explorer

Interactive search across **6,289 presentations** at 20 editions of the International Industrial Organization Conference (2006-2026, excluding the cancelled 2020 edition). **4,669 indexed names** (presenters, discussants, coauthors).

Type a first or last name, pick from the autocomplete list, and see every appearance of that person broken into three disjoint groups:

- **Presented** - person is the listed presenting author
- **Discussed** - person served as a formal discussant
- **Co-authored (did not present)** - person is a coauthor on a paper someone else presented

Click any paper to reveal the publication outcome (journal, year, citations, DOI) matched from the OpenAlex snapshot plus Crossref live lookup.

## How to open

- **Online:** https://aljoschaj.github.io/iioc-explorer/
- **Offline:** download `index.html` and double-click. Works with no server or internet.

## Rebuild after data changes

```
py Code/22_author_rematch.py       # refresh matches from local parquet (author-verified)
py Code/23_crossref_supplement.py  # supplement with Crossref for recent papers
py Code/21_build_explorer.py       # rebuild the HTML
cd Tool && git add . && git commit -m "Refresh data" && git push
```

## Match quality notes

- Matching requires the IIOC presenter (or a coauthor) to actually appear as an author on the OpenAlex or Crossref publication record. Title similarity alone never matches.
- Field restricted to econ / business / social / decision sciences; medical, chemical, and clinical journals are excluded.
- A grey "-" badge means no verified match; yellow "WP" means a working-paper repository (NBER, SSRN, arXiv...); green "J" means a peer-reviewed journal article.

Source programs: IIOC on Editorial Express. Publication data: OpenAlex + Crossref.
