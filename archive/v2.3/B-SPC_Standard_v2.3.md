# Benefits Statistical Process Control (B-SPC) Standard

*Open standard · Version 2.3 · September 2026 · Published by Zeluca, Inc. · Licence: CC BY 4.0*

A standard for measuring, charting and attributing payment and procedural error in government benefit programs

This standard specifies how a benefit agency, an auditor, a researcher or a vendor should measure error where it enters a process, chart it so that noise is not mistaken for signal, and attribute movement to a cause. It is written to be applied without any particular software. Zeluca publishes it, holds its own products to it, and invites correction. Use, adapt and cite freely.

## 1. Scope and definitions

The standard applies to programs whose accuracy is measured by a sampled, dollar-weighted error rate — SNAP first, and Medicaid MEQC/PERM, TANF and CCDF where the same integrated workforce and income rules apply. It governs management measurement between official cycles; it does not replace, re-estimate or predict the official rate.

| **Term**                             | **Definition**                                                                                                                                                                               |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Handoff                              | The transfer of a work item between two named process nodes. The unit of measurement.                                                                                                        |
| Acceptance criterion                 | What a complete and correct work item must contain at a handoff, derived from policy with a citation. Where policy states none, the handoff is UNDEFINED and that is a finding.              |
| Percent complete-and-accurate (%C&A) | The share of items arriving at a node that the receiver can process without correction, addition or clarification. Measured by the receiver. The three failure modes are counted separately. |
| Escaped-defect rate                  | The share of items that passed a node's check and were later found in error. A lower bound on the defect rate at the handoff.                                                                |
| Critical-to-quality (CTQ) node       | A handoff selected by dollars × persistence × concentration; typically three to five per driver path.                                                                                        |
| Persistence                          | Expected months an error pays before detection. Enters severity as a multiplier.                                                                                                             |
| Regime                               | A period in which the process is operating under different rules or load — disaster program, mass change, system cutover, policy effective date — charted separately.                        |
| Tri-mandate                          | Payment error rate (PER), case and procedural error rate (CAPER) and application processing timeliness (APT) reported together; no one of them is published without the other two.           |

## 2. The three views and the evidence ladder

A process is known three independent ways: as-designed (policy and procedure, each node with a citation), as-practiced (observed at the desk and attested by the people who send and receive work), and as-executed (system event logs across every case). No single view is authoritative; where they disagree, the disagreement is the finding. The same measure climbs an evidence ladder as data matures: attested with a band → sampled with an interval → mined with stated log coverage. The definition never changes on the way up.

## 3. Basis tags and evidence grades (mandatory)

| **Tag / grade** | **Requirement**                                                                                                                             |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| SOURCED         | Retrieved from statute, regulation or manual, with citation and offset into the text.                                                       |
| DERIVED         | Computed by a stated rule or formula from other tagged values.                                                                              |
| ASSUMED         | A default in the absence of data, with owner and sensitivity bounds.                                                                        |
| ATTESTED        | Stated by a practitioner in a structured, recorded session; role and date recorded; reported as a band.                                     |
| SAMPLED         | Measured on an empirical sample; n, method and 95% Wilson interval stated; reviewer agreement demonstrated (§6).                            |
| MINED           | Computed from event logs; log coverage percentage stated.                                                                                   |
| Evidenced       | Two or more independent views agree; for an intervention, a design registered before rollout shows the effect at conventional significance. |
| Indicated       | One view plus documented judgement, or favourable movement still inside control limits.                                                     |
| Hypothesis      | Asserted; the data to test it is not held. Reported as such, never as a number to plan against.                                             |

Rule: no point estimate without an interval; no rate without its n and window; no rolled yield without the chain beneath it, and none while any handoff in the chain is Hypothesis or UNDEFINED.

## 4. The indicator specification (ten fields, versioned)

Every indicator, leading or lagging, is written to ten fields before its first value is recorded: identifier (IND-\[domain\]-\[number\]); name; definition; formula with explicit numerator and denominator; source system, report and field; owner (a named role); cadence and trigger; direction of good; linked driver and handoff; baseline value with date and the CUSUM shift target. Definitions are never amended in place: a change retires the identifier and opens a new one with a new baseline. The source is named specifically — "field X of weekly report Y produced by team Z," never "from the eligibility system."

## 5. The chart set

| **Chart**                          | **Use it for**                                              | **Specification**                                                                                                                                                                        |
|------------------------------------|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tri-mandate strip                  | PER, CAPER and APT side by side                             | Point estimate ± 1.96·SE for PER and CAPER; tier bands and points-to-next-tier on PER; 95% line and 30-day / 7-day split on APT; raw-vs-official badge; cadence stamp on each tile       |
| Shewhart p-chart                   | Small, similar-size subgroups (30–50-case node samples)     | 3σ limits from actual n; Nelson rules                                                                                                                                                    |
| Laney p′ chart                     | Variable or large n (monthly raw rate; mined node rates)    | z_i = (p_i − p̄)/√(p̄(1−p̄)/n_i); σ_z = mean moving range of z / 1.128; limits p̄ ± 3·σ_z·√(p̄(1−p̄)/n_i). Corrects over- and under-dispersion so alarms are shifts, not sample-size artifacts |
| XmR (individuals and moving range) | Error dollars per \$1,000 issued; persistence-weighted loss | Limits at mean ± 2.66·MR̄; MR limit 3.267·MR̄                                                                                                                                              |
| Tabular CUSUM                      | Weekly leading indicators                                   | Standardized z; k = half the shift of interest (default 0.5σ); h = 4–5σ; C⁺ and C⁻ tracked; shift target written in the indicator spec                                                   |
| Pareto with waterfall              | Error dollars by driver, addressable vs residual floor      | Dollar-weighted; tolerance shown as excluded but visible; over- and under-payment separate                                                                                               |
| Coverage matrix                    | Driver × initiative × indicator, with a capacity column     | Ownership is exclusive before movement is graded; shared indicators marked "not attributable"                                                                                            |
| Locked panels                      | Measures whose data does not yet exist                      | Shown, labelled, inert — never omitted                                                                                                                                                   |

### Special-cause detection (Nelson rules)

\(1\) one point beyond 3σ; (2) nine consecutive on one side of center; (3) six consecutive rising or falling; (4) fourteen alternating; (5) two of three beyond 2σ on one side; (6) four of five beyond 1σ on one side; (7) fifteen within 1σ (stratification); (8) eight consecutive beyond 1σ on both sides (mixture). A signal is reported with the rule that fired. Movement inside the limits with no rule firing is reported as common cause.

### Rational subgrouping and regimes

Caseloads under a different regime — disaster program (7 CFR 280), mass change, system cutover, policy effective date — are tagged and charted separately; a phase line marks every regime boundary and every intervention start. Commingling a two-week disaster surge with the baseline corrupts limits for months.

## 6. Measurement system requirements

- Before a sampled rate counts, two or three reviewers independently score 20–30 shared cases against the written criteria; agreement (Fleiss' kappa) must reach 0.75 (target 0.80). Disagreement is resolved by tightening the criterion, not by averaging.

- Samples are drawn from non-QC-sampled cases only, de-identified, reported in aggregate; 30–50 cases per node gives a proportion with a usable interval.

- Attestation is collected from both sides of a handoff (sender and receiver) and never averaged; the receiver's figure governs.

- Each component carries its own cadence stamp — per QC cycle, weekly, on change, on re-baseline, continuous. A single global "live" timestamp is prohibited.

## 7. Attribution

A claim that an intervention changed a rate requires a design registered before rollout: the unit of assignment (office, county, consortium, region), the assignment rule (staggered, matched or randomized), the primary indicator expected to move, the expected direction and rough size, and the observation window. At window close the effect is estimated (difference-in-differences, synthetic control, or interrupted time series on the indicator) and graded. Without a registered design, movement is reported as "correlation in time." Ownership of an indicator is exclusive before its movement is graded.

## 8. Capacity

No detection, review or check is deployed without a capacity plan. For each affected node: arrival rate, service rate, reviewer count; utilization held at or below 0.85; expected wait from the queue model solved so that the probability of breaching the 30-day (regular) or 7-day (expedited) processing standard stays under 5%. Work-in-process is reconciled to Little's Law from counts the agency already produces.

## 9. Automation and human decision

- Automation removes or mistake-proofs steps; it never determines eligibility, calculates a binding budget, or takes an adverse action. Certification is reserved to merit-system personnel (7 U.S.C. 2020(e)(6)(B)). A check may require an affirmative action; it never withholds a merit worker's authorization.

- Cognitive forcing is mandatory where an automated output is presented: visual diff of reported vs extracted values; affirmative checkpoints before a budget saves; structured override reasons; time-on-case telemetry with rapid approvals routed to second-party review.

- In-workflow assistants operate within written budgets: added latency per case (≤60 s), inline response (≤1.5 s), false-flag rate per module (≤5%), a biweekly cross-functional review of flags, actions and overrides, and a kill switch that is drilled.

- Presentation-layer automation (screen or terminal scraping) is used only where no API or event interface exists, and only behind a circuit breaker that detects failure within minutes, reroutes to the worker queue and alerts a supervisor.

- Equity: extraction accuracy, confidence and latency are tested for parity across language, document type and income type; targeting and routing models carry no demographic or geographic features.

## 10. Federal quality control firewall

Only post-transmission aggregate QC data enters management measurement. Cases pulled for the federal QC sample are never selected for review, correction, prioritization or automation before transmission; suppression is implemented so that no worker or office can infer which cases are sampled. Vendor discussion of any sampled case is documented and open to FNS. Contractors touching QC processes or policy training give FNS 30 days' notice with deliverables (Handbook 310 §154). Sub-threshold errors are excluded from the rate but reported for corrective action (§623). The tolerance threshold is indexed annually (\$57 FY2025, \$58 FY2026); it has not been eliminated.

## 11. Reporting to a corrective action plan

| **7 CFR 275.17 element**                          | **B-SPC component**                                                       |
|---------------------------------------------------|---------------------------------------------------------------------------|
| Description of each deficiency                    | Dollar-weighted driver attribution; CTQ nodes                             |
| Source through which detected                     | QC findings plus the process baseline for the mechanism                   |
| Magnitude and geographic extent                   | Dollar and persistence weighting; office-level cuts                       |
| Causal factors                                    | The handoff where the error enters; deviation-to-dollar link              |
| Actions, expected outcomes, target dates          | Initiative register with the addressable-vs-floor ceiling                 |
| Manner of monitoring and evaluating effectiveness | Leading indicators on control charts; registered designs; evidence grades |

Semiannual updates (1 May / 1 Nov) are exported from the register, not written from memory. CAPER above the national average and timeliness below 95% are reported in the same submission.

## 12. Conformance and independence

A product or engagement conforms to B-SPC when every published figure carries a basis tag and an interval, every movement claim carries a grade, the tri-mandate strip is present, charts use limits and rules as specified, the QC firewall holds, and every figure is exportable and independently recomputable from the agency's own data by any party the agency chooses — including one checking the publisher. Zeluca accepts no commissions, referral fees or reseller margins from any vendor whose work passes through a B-SPC evaluation it conducts, and applies the same evidence gates to components it builds. Corrections to this standard are welcome at methods@zeluca.com; a revision is issued with every full life cycle engagement completed in the field.

## 13. Worked example (illustrative figures)

A state with 1,050 completed QC reviews publishes 9.44% with a standard error of 1.24: the 95% interval is 7.0–11.9%, spanning three tiers. Its AC06 export ranks wages and salaries (311) first at \$5.3M of error dollars; AC03 timing shows 61% of those errors entered at the most recent action. The as-designed map places the income-determination handoff between "verification received" and "budget computed"; the acceptance criterion (SOURCED, state manual §24.14 and 7 CFR 273.9) requires a pay-period-complete stub set and a documented conversion factor. Mirror attestation gives 45–65% complete-and-accurate at that handoff (ATTESTED). A 50-case non-QC sample scored by three reviewers (κ = 0.81) gives 58% (SAMPLED, Wilson 95% CI 44–71%). The escaped-defect floor from AC03 is 9%. Severity: \$5.3M × an expected 4.2 months undetected; occurrence 0.42; detection 0.30 (a second-party review exists at 30% of cases) → the highest risk-priority number on the path. The registered design: a pre-authorization income check rolls out to the three largest county offices first, then the rest at week six; the primary indicator is "income cases with second-party review before authorization," expected up; window twelve weeks. At window close the CUSUM on that indicator fires at week seven for the early offices and not for the later ones, and the difference-in-differences estimate on the node yield is +11 points (CI +4 to +18): graded Evidenced. The monthly raw rate on the Laney p′ chart shows no special cause — expected, since the sample cannot resolve a change this size within the window, which the detectability calculator said in advance. The corrective action plan update reports the node yield, the indicator movement and the grade, and states that the official rate will not be able to confirm the effect until the next cycle.

## 14. Conformance checklist

| **\#** | **Requirement**                                                                                                                    | **Evidence of conformance**                      |
|--------|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| 1      | Every published figure carries a basis tag, its window and its n                                                                   | Figure metadata; sample of ten figures inspected |
| 2      | Every rate carries an interval; no rolled yield without its chain                                                                  | Chart set; %C&A report                           |
| 3      | Every movement claim carries a grade, and Evidenced claims cite a registered design                                                | Design register; attribution readouts            |
| 4      | Tri-mandate strip present wherever PER is shown                                                                                    | Board; CAP export                                |
| 5      | Charts use the specified limits and Nelson rules; signals name the rule                                                            | Chart configuration; alarm log                   |
| 6      | Rational subgrouping by regime; phase lines on every chart                                                                         | Regime calendar; charts                          |
| 7      | Indicator specifications complete in ten fields; changes retire and re-issue identifiers                                           | Indicator register with version history          |
| 8      | Reviewer agreement demonstrated before any sampled rate is published                                                               | Kappa report per sample cycle                    |
| 9      | Capacity plan on file for every review, check or detector before deployment                                                        | Queue model outputs; timeliness check            |
| 10     | No eligibility decision, binding budget or adverse action automated; cognitive forcing present; budgets and kill switch documented | Design review record; C-42; drill log            |
| 11     | QC firewall: aggregates only; sampled cases never selected or suppressed visibly; §154.9 notices issued                            | Data request kit; registry design; notices       |
| 12     | Every figure exportable and recomputable from the agency's data by a third party                                                   | Export package; recomputation test               |
| 13     | Publisher discloses any commercial interest in components it scores; applies the same gates to its own builds                      | Independence statement                           |

## 15. Instrument glossary

The instruments the standard expects, by the phase in which they first appear. Full formulations are in the AGBER methodology, Appendix A.

| **Phase**            | **Instruments**                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Look (0)             | Dollar-weighted driver Pareto and waterfall · as-designed map with citations and sufficiency report · as-practiced overlay and variance register · federal-vs-state alignment check · tri-mandate strip (PER with interval and bands; CAPER; APT) · indicator specifications and baselines · coverage matrix with capacity column · policy complexity profile · directional %C&A bands · regime calendar and telemetry-use statement |
| Measure (1)          | Sampled %C&A per handoff with Wilson intervals · reviewer agreement report · FMEA risk priority · persistence-weighted cost by node · Shewhart p and Laney p′ charts · CUSUM on weekly indicators · error-dollars-per-\$1,000 XmR chart · detectability calculator · queue model with timeliness constraint · signed baseline and reproducibility record · registered counterfactual designs · CAP export in 275.17 fields           |
| Watch everything (2) | Conformance and deviation map with log coverage · deviation-to-dollar attribution · Kaplan–Meier survival on pending states · mined %C&A across all cases · intervention attribution readout (DiD / synthetic control / ITS) · discrete-event simulation · automation candidate ranking · process-variable feed                                                                                                                      |
| Remove the step (3)  | Before/after node Laney p′ with phase line · hours-returned ledger · false-positive and override report · boundary and citation audit · multi-program consistency matrix · bot health and circuit-breaker telemetry                                                                                                                                                                                                                  |
| Add a helper (4)     | Agent latency and throughput · false-flag and override governance ledger · agent-assisted node charts · workload and client-outcome panel · cognitive-forcing telemetry audit · equity and language-parity audit                                                                                                                                                                                                                     |
| Keep learning (5)    | Indicator vitality report · evaluation-corpus delta report · cross-state node benchmark · three-year sustainment ledger                                                                                                                                                                                                                                                                                                              |

## 16. Revision and citation

B-SPC v2.3, September 2026. Supersedes v2.2 (adds the tri-mandate, regime subgrouping, measurement-system requirements, capacity-to-timeliness rule, circuit-breaker and parity clauses). Cite as: Zeluca Inc., Benefits Statistical Process Control (B-SPC) Standard v2.3, September 2026. The standard is free to use, adapt, cite and improve under the Creative Commons Attribution 4.0 International licence (CC BY 4.0). Field experience and disagreement are requested; the next revision is expected after the method has been used in a state across one full QC cycle.
