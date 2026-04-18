# IIOC Person Explorer

Interactive search tool for the International Industrial Organization Conference programs, 2006-2026 (excluding the cancelled 2020 edition). Covers **6,289 presentations** across **20 editions**, with **4,669 indexed names** (presenters, discussants, and coauthors).

Type any name — first or last — and see every appearance of that person, split into three disjoint groups:

- **Presented** — the person is the listed presenting author
- **Discussed** — the person served as a formal discussant
- **Co-authored (did not present)** — the person is a coauthor on a paper someone else presented

Click any paper to reveal the publication outcome (journal, year, citations, DOI where available), matched against the OpenAlex bibliometric database.

## How to open

- **Online:** visit the GitHub Pages URL (see repository settings).
- **Offline:** download and double-click `index.html`. Works in any modern browser with no server and no internet connection.

## Rebuilding

From the project root:

```
py Code/21_build_explorer.py
```

Rewrites `Tool/iioc_explorer.html` and `Tool/index.html` from `Data/enriched/iioc_final.csv`.

## Source

Built from IIOC programs hosted on Editorial Express. Publication outcomes matched to OpenAlex.
