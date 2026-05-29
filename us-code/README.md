# US Code — Federal Statutes

## What is the US Code?

The United States Code (USC) is the official codification of the general and permanent federal statutes of the United States. It is organized into 54 titles, each covering a broad subject area.

Examples:
- Title 1: General Provisions
- Title 10: Armed Forces
- Title 26: Internal Revenue Code
- Title 42: Public Health and Welfare
- Title 51: National and Commercial Space Programs

## Integration Approach

**We use git submodule referencing rather than duplicating the content.**

The full US Code already exists as a git repository maintained by [nickvido](https://github.com/nickvido/us-code). Rather than copy 50,000+ files, we reference that work.

### Rationale

Three options were evaluated:

| Option | Pros | Cons |
|--------|------|------|
| Fork + restructure | Full control, can add annotations | Enormous maintenance burden; USC changes frequently |
| Submodule reference | Stays current, clean integration | Requires separate clone; GitHub doesn't render submodule contents |
| README reference only | Lightweight, honest about scope | No actual content in this repo |

**Decision: Reference approach.** The primary value of this repo is the constitutional layer (amendments as PRs) and SCOTUS context — not duplicating the already-available USC. Adding a submodule pointing to nickvido/us-code is the cleanest integration.

## Official Sources

- **GovInfo bulk download:** https://www.govinfo.gov/bulkdata/USCODE — Official government source, updated annually
- **nickvido/us-code:** https://github.com/nickvido/us-code — Full USC as a git repo (plain text)
- **Cornell LII:** https://www.law.cornell.edu/uscode/text — Hyperlinked, searchable online version
- **Office of the Law Revision Counsel:** https://uscode.house.gov/ — Official online USC with search

## Proposed Structure (future)

If individual titles are added to this repo, they would be organized as:

```
us-code/
├── README.md          # This file
├── title-01/          # General Provisions
├── title-10/          # Armed Forces
├── title-26/          # Internal Revenue Code (tax law)
├── title-42/          # Public Health and Welfare
└── ...
```

Each file would be a markdown version of the corresponding USC section, with annotations linking to relevant SCOTUS cases in `../supreme-court/landmark-cases/`.

## The PR Metaphor for Legislation

In the full vision of this repo, proposed legislation would appear as open Pull Requests. Key bills that became law would be tracked as merged PRs. This is the most ambitious layer of the project — for now, see the [README](../README.md) for the planned roadmap.
