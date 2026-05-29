# 🇺🇸 us-laws — America as Code

> The US political and legal system, modeled as a git repository.

## The Concept

What if the laws of the United States were managed like a software project?

- The **Constitution** = the initial commit. The founding architecture.
- The **Bill of Rights** = the first big merged PR. Ten amendments bundled together, ratified 1791.
- Each subsequent **Amendment** = a merged PR with historical context in the PR body.
- **Landmark Supreme Court rulings** = comments/annotations that reinterpret the code without changing it.
- **Current federal statutes** = files in the repo, organized by title.
- **Proposed legislation** = open PRs, debated and amended before merging (or closed without merge).

This isn't satire. It's a serious attempt to make the structure of American law navigable, transparent, and historically contextualized using the most powerful version-control metaphor most people already understand.

## Why This Matters

The US legal system is roughly 200+ years of accumulated decisions, amendments, interpretations, and statutes. It's extraordinarily hard to understand how we got here from there. Git's diff, log, and PR history make that evolution visible in a way no law school textbook does.

Prior art:
- [`anthonygarvan/theconstitution`](https://github.com/anthonygarvan/theconstitution) — Constitution as commits
- [`legalize-dev/legalize`](https://github.com/legalize-dev/legalize) — 30+ countries as markdown
- [`nickvido/us-code`](https://github.com/nickvido/us-code) — US Code as a repo

None of these implement the full PR metaphor for proposed bills, or combine all layers (Constitution → Amendments → SCOTUS → Statutes → Proposed Bills) in one place.

## Repository Structure

```
us-laws/
├── README.md                          # You are here
├── constitution/
│   ├── constitution.md                # Original Constitution (without amendments)
│   ├── bill-of-rights.md              # Amendments 1–10 (ratified together, 1791)
│   └── amendments/
│       ├── amendment-11.md            # Judicial limits (1795)
│       ├── amendment-12.md            # Electoral College reform (1804)
│       ├── ...
│       └── amendment-27.md            # Congressional pay (1992)
├── supreme-court/
│   └── landmark-cases/
│       ├── 1803-marbury-v-madison.md
│       ├── 1857-dred-scott-v-sandford.md
│       └── ...  (~200–400 cases)
└── us-code/
    └── README.md                      # Reference to nickvido/us-code + integration notes
```

## The Layers

| Layer | Metaphor | Status |
|-------|----------|--------|
| Constitution (original) | Initial commit | ✅ Done |
| Bill of Rights (Amendments 1–10) | First merged PR | ✅ Done |
| Amendments 11–27 | Merged PRs | ✅ Done |
| Landmark SCOTUS rulings | Interpretive annotations | 🔄 In progress |
| US Code (federal statutes) | Main codebase files | 🔄 Referenced |
| Proposed legislation | Open PRs | 📋 Planned |

## Data Sources

All content is public domain:
- Constitution text: [archives.gov](https://www.archives.gov/founding-docs/constitution-transcript)
- Amendment text: [archives.gov](https://www.archives.gov/founding-docs/amendments-11-27)
- SCOTUS cases: [CourtListener](https://www.courtlistener.com/), [Oyez.org](https://www.oyez.org/)
- US Code: [GovInfo bulk data](https://www.govinfo.gov/bulkdata/USCODE), [`nickvido/us-code`](https://github.com/nickvido/us-code)

## Contributing

See something wrong? Open a PR. The irony of amending a repo about amendments is not lost on us.

## License

All legal text is US government public domain. Repository structure, commentary, and original writing © Travis Millet, released under MIT.
