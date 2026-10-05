# Changelog

This file records revisions of the **NODA Methodology** (Network Operational Domain Assessment), the open, versioned scoring specification behind [NODA Check](https://noda.marinadns.io/). It mirrors Appendix C (Revision History) of the specification.

Versioning follows the policy in Section 12 of the specification (SemVer):

- **MAJOR**: a change to the axis model, the Category set, the Composite Formula, or any published property of an existing Check.
- **MINOR**: a new Check is added.
- **PATCH**: editorial changes only, with zero impact on any score.

Reports record the methodology version that produced them. A Report is permanent and always renders under the rules of the version it records (Section 11).

| Version | Specification | PDF |
|---|---|---|
| 1.0.1 (current) | [noda.marinadns.io/methodology](https://noda.marinadns.io/methodology) | [NODA Methodology v1.0.1.pdf](https://noda.marinadns.io/methodology/NODA-Methodology-v1.0.1.pdf) |
| 1.0 (archived) | [noda.marinadns.io/methodology/v1.0](https://noda.marinadns.io/methodology/v1.0) | [NODA Methodology v1.0.pdf](https://noda.marinadns.io/methodology/NODA-Methodology-v1.0.pdf) |

---

## [1.0.1] — 2026-10-05 — PATCH

**Scoring impact: none.** No Check property, compliance value, or Composite Score changed. Reports issued under NODA-v1.0 remain valid and give the same scores under v1.0.1. New Reports record `NODA-v1.0.1` from 2026-10-05.

This revision fixes passages where the prose did not match the Composite Formula (Section 6.1) or the behaviour of the reference implementation. Where they disagreed, the formula was kept and the prose was corrected, because every published Report was computed under the formula.

| Section | Change | Reason |
|---|---|---|
| 6.1 | States the rounding rule: multiply by 100, round half away from zero. Defines the Unscored case. | The rule was applied but never written down, which made independent reproduction harder (Section 5.1). |
| 6.2 | Drops the "same Category" condition on the baseline Check and states why Health gets 30%. | NS Different Subnets and ASN Diversity, whose baseline Check is in CAT-INFRA, did not meet the rule as written. |
| 6.3 | Corrects the claim that excluding a Conditional Check does not reduce its Category's weight. | Weights apply per Check, so an exclusion reduces the Category's effective share. The formula is unchanged. |
| 6.3 | Discloses two existing behaviours: the DKIM Record Check can raise a score but never lower it, and the Blacklist Check returns Informational when no MX record exists. | Both behaviours were already in effect but undocumented. |
| 6.4 (new) | Publishes the interpretation tiers used in Reports: Exceptional, Good, Needs Improvement, Poor, Critical. | Reports applied these tiers, and Appendix B referred to them, but the specification never defined them. |
| 7 | Clarifies that Category weights are per-Check multipliers. Adds Appendix D. Removes text written before release. | The old wording implied each Category held a fixed share of the score, which the formula does not produce. |
| 8 | Extends the S1 definition to Best-Practice-axis Checks and states how status maps to severity. | The S1 definition did not cover Critical Findings on Best-Practice-axis Checks, and the mapping was undocumented. |
| 10 | Clarifies that the RFC Adherence Ledger records each Check's normative basis and does not set status or severity. | Read literally, the old wording ruled out Critical or Warning Findings for Checks without a MUST/SHALL citation. |
| 12 | Moves Category weight adjustment from MINOR to MAJOR. Defines the MINOR rule in terms of published Check properties. States when Reports from different versions can be compared. | The old MINOR definition contradicted itself. The policy is now stricter, not looser. |
| 13 | Records that six Checks were added before first release. Discloses that DNSSEC signature presence and algorithm acceptability are scored separately. | The old wording implied that MINOR revisions had already happened under v1.0. |
| Appendix A | States the pass condition for DNSSEC Multi-Algorithm Signing. | The Check's title could be read as requiring more than one algorithm. |
| Appendix A | Adds an "RFC basis" column that publishes the RFC Adherence Ledger for every Check. | Section 10 said every Check carried this annotation, but none was published. |
| 13, 14 | Replaces RFC 8624 with RFC 9904, which obsoleted it in November 2025. Adds RFC 1034, RFC 7766 and RFC 9471 as Ledger sources. | RFC 8624 was already obsolete at first release. The new references support the Ledger entries. |
| Appendix B | Corrects the worked example's Best Practice tier from Needs Improvement to Poor. | Aligns the example with the tiers applied in Reports. |
| Appendix C (new) | Adds a revision history. | Keeps a record of every revision. |
| Appendix D (new, informative) | Adds tables of effective Category shares for two reference configurations. | Makes the per-Check weighting in Section 7 easy to see. |
| Header | Standard ID NODA-v1.0.1. Status: First Release, Revision 1. Obsoletes: NODA-v1.0. | Version bookkeeping. |

## [1.0] — 2026-08-09 — First Release

First public release. Defines the dual-axis scoring model (Health and Best Practice), five weighted Categories, the severity taxonomy, Report requirements, the RFC Adherence Ledger, the historical-consistency and versioning policies, and a catalogue of 41 Checks: 37 scored and 4 Informational-Only.
