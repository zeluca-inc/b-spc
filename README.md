# Benefits Statistical Process Control (B-SPC) Standard

**Version 2.6 · 1 October 2026 · License: CC BY 4.0**

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22926248.svg)](https://doi.org/10.5281/zenodo.22926248)

An open standard for measuring, charting and attributing payment and procedural error in government benefit programs — SNAP first, and Medicaid MEQC/PERM, TANF and CCDF where the same integrated workforce and income rules apply. It specifies how a benefit agency, an auditor, a researcher or a vendor should measure error where it enters a process, chart it so that noise is not mistaken for signal, and attribute movement to a cause. From v2.6 it also specifies how that work is expressed in the two bills a state now pays (the benefit cost-share and the administrative bill), how credit for it is divided in error dollars, and how the staff capacity behind it is measured before anything scales. It is written to be applied without any particular software.

The standard governs management measurement between official quality-control cycles. It does not replace, re-estimate or predict the official payment error rate; targets, projections and nowcasts it permits are labeled PROJECTED.

## Contents of this repository

| File | What it is |
|---|---|
| `B-SPC_Standard_v2.6.md` | The standard, full text (source of record) |
| `B-SPC_Standard_v2.6.pdf` | The same text, typeset (11 pages) |
| `archive/v2.3/` | The previous release (v2.3, September 2026), unchanged |
| `companion/Seventh_Element_v1.1.pdf` | Companion one-pager: what "how the State will measure the effectiveness of the corrective action" (7 CFR 275.17) looks like when it is answered with a number |
| `CHANGELOG.md` | What changed in each release |
| `CITATION.cff` | Citation metadata |
| `LICENSE` | Creative Commons Attribution 4.0 International |

The canonical web page is <https://zeluca.com/b-spc>.

## Cite as

**Zeluca Inc. (2026). *Benefits Statistical Process Control (B-SPC) Standard*, v2.6. Zenodo. https://doi.org/10.5281/zenodo.22926248. Also at https://zeluca.com/b-spc. Licensed CC BY 4.0.**

The DOI above is the concept DOI: it always resolves to the latest version. Each release also has its own version DOI, listed on the Zenodo record: v2.6 is https://doi.org/10.5281/zenodo.23072821 and v2.3 is https://doi.org/10.5281/zenodo.22926249.

## License

The standard is free to use, adapt, cite and improve under the [Creative Commons Attribution 4.0 International license](https://creativecommons.org/licenses/by/4.0/). Attribution to Zeluca Inc. is the only condition.

## Corrections and field experience

Disagreement is requested. Open an issue in this repository or write to hamid.nouri@zeluca.com. The next revision is expected after the method has been used in a state across one full QC cycle.

## Revisions

| Version | Date | Notes |
|---|---|---|
| 2.6 | 1 October 2026 | Current. Supersedes v2.3; numbered to match the AGBER methodology v2.6 it accompanies (no v2.4 or v2.5 of the standard was issued). Adds the two bills, attribution in error dollars with the rate bridge, the scale-readiness card, capacity and process-efficiency measures, indicator validation, target and projection rules, limit-setting discipline, figure statuses, the year-and-source rule, eight conformance rows and their applicability at Phase 0. See `CHANGELOG.md`. |
| 2.3 | September 2026 | Supersedes v2.2: adds the tri-mandate, regime subgrouping, measurement-system requirements, capacity-to-timeliness rule, circuit-breaker and parity clauses. In `archive/v2.3/`. |

When I checked GitHub just now, the README was still the v2.3 version and there was no archive folder yet. GitHub can take a minute to show new commits, so after your commit, check that:

the README shows "Version 2.6" and the DOI badge;
archive/v2.3/ contains both v2.3 files;
CITATION.cff has the doi: "10.5281/zenodo.22926248" line.

When those are right, publish the v2.6.0 release. Use the v2.6 section of CHANGELOG.md as the release notes and attach the PDF.
