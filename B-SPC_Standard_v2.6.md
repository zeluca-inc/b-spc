# Benefits Statistical Process Control (B-SPC) Standard

*Open standard · Version 2.6 · 1 October 2026 · Published by Zeluca, Inc. · License: CC BY 4.0*

A standard for measuring, charting and attributing payment and procedural error in government benefit programs

This standard specifies how a benefit agency, an auditor, a researcher or a vendor should measure error where it enters a process, chart it so that noise is not mistaken for signal, and attribute movement to a cause. From v2.6 it also specifies how that work is expressed in the two bills a state now pays (the benefit cost-share and the administrative bill), how credit for it is divided in error dollars, and how the staff capacity behind it is measured before anything scales. It is written to be applied without any particular software. Zeluca publishes it, holds its own products to it, and invites correction. Use, adapt and cite freely.

## 1. Scope and definitions

The standard applies to programs whose accuracy is measured by a sampled, dollar-weighted error rate — SNAP first, and Medicaid MEQC/PERM, TANF and CCDF where the same integrated workforce and income rules apply. It governs management measurement between official cycles; it does not replace, re-estimate or predict the official rate. Targets, projections and nowcasts permitted by §11.1 are planning instruments labeled PROJECTED; none is ever published as an estimate of the official rate.

| **Term** | **Definition** |
| --- | --- |
| Handoff | The transfer of a work item between two named process nodes. The unit of measurement. |
| Acceptance criterion | What a complete and correct work item must contain at a handoff, derived from policy with a citation. Where policy states none, the handoff is UNDEFINED and that is a finding. |
| Percent complete-and-accurate (%C&A) | The share of items arriving at a node that the receiver can process without correction, addition or clarification. Measured by the receiver. The three failure modes are counted separately. |
| Escaped-defect rate | The share of items that passed a node's check and were later found in error. A lower bound on the defect rate at the handoff. |
| Critical-to-quality (CTQ) node | A handoff selected by dollars × persistence × concentration; typically three to five per driver path. |
| Persistence | Expected months an error pays before detection. Enters severity as a multiplier. |
| Regime | A period in which the process is operating under different rules or load — disaster program, mass change, system cutover, policy effective date — charted separately. |
| Tri-mandate | Payment error rate (PER), case and procedural error rate (CAPER) and application processing timeliness (APT) reported together; no one of them is published without the other two. |
| Governing rate year | The fiscal year whose official rate sets a given year’s benefit cost-share. Under current law FY2028 uses the better of FY2025 or FY2026, and FY2029 onward uses the rate three fiscal years earlier. |
| Planning target (R\*) and required points (ΔR) | R\* = tier threshold − z·SE, with SE from the FNS annual report and z stated (1.0, about five chances in six; 1.28, about nine in ten). ΔR = latest official rate − R\*. |
| Lever, yield and coverage | The three levers are find-and-fix on the existing caseload, point-of-action controls and pre-authorization review. Yield is the share of a driver’s error dollars a lever removes where it touches a case; coverage is the share of the governing year’s sampled benefit-months it reaches in time. |
| Attributed dollars and unattributed remainder | Error dollars credited to an initiative at the grade its registered design reached, shared dollars credited once. The remainder is the part of a change in the rate that graded initiatives, outside effects, the federal regression adjustment and sampling noise do not explain. It is always reported. |
| Utilization (ρ) | Hours of review or processing needed ÷ hours available, for the same office or team and period. |
| Failure demand | Work caused by an earlier failure of the process rather than by new need: duplicate applications, status calls, repeat document requests, re-verification, re-opening, error correction. |
| Released capacity | Worker hours no longer needed for the same output, Σ(volume × minutes saved) ÷ productive minutes per FTE, with an interval. |

## 2. The three views and the evidence ladder

A process is known three independent ways: as-designed (policy and procedure, each node with a citation), as-practiced (observed at the desk and attested by the people who send and receive work), and as-executed (system event logs across every case). No single view is authoritative; where they disagree, the disagreement is the finding. The same measure climbs an evidence ladder as data matures: attested with a band → sampled with an interval → mined with stated log coverage. The definition never changes on the way up. Capacity measures climb the same ladder: walkthrough bands (attested), then work sampling or a time study (sampled), then event-log timings (mined), with the log-coverage statement saying which figure came from which.

## 3. Basis tags and evidence grades (mandatory)

| **Tag / grade** | **Requirement** |
| --- | --- |
| SOURCED | Retrieved from statute, regulation or manual, with citation and offset into the text. |
| DERIVED | Computed by a stated rule or formula from other tagged values. |
| ASSUMED | A default in the absence of data, with owner and sensitivity bounds. |
| ATTESTED | Stated by a practitioner in a structured, recorded session; role and date recorded; reported as a band. |
| SAMPLED | Measured on an empirical sample; n, method and 95% Wilson interval stated; reviewer agreement demonstrated (§6). |
| MINED | Computed from event logs; log coverage percentage stated. |
| PROJECTED | The output of a stated planning formula (target plan, lever projection, probability-of-tier nowcast, capacity before it is measured), carrying the formula, its inputs and each input’s tag. Not an evidence grade: never graded Evidenced, Indicated or Hypothesis, and never plotted as a trend beside a measured rate. |
| Evidenced | Two or more independent views agree; for an intervention, a design registered before rollout shows the effect at conventional significance. |
| Indicated | One view plus documented judgment, or favorable movement still inside control limits. |
| Hypothesis | Asserted; the data to test it is not held. Reported as such, never as a number to plan against. |
| Figure status | Every figure the board expects is present or carries one of three statuses with a reason: LOCKED (not produced in this phase, by decision), UNAVAILABLE (an input is missing) or REFUSED (the wording would outrun the evidence). A missing value is never shown as zero. |
| Vendor-reported | Reported by the party delivering a countermeasure; carries the reporter’s name. Shown as activity only, and never enters an error-dollar or attribution figure until a measured effect supports it. |

Rule: no point estimate without an interval; no rate without its n and window; no rolled yield without the chain beneath it, and none while any handoff in the chain is Hypothesis or UNDEFINED. Every figure names its own year and source, and a tile or calculation never combines figures from different years: an FY2025 official rate and FY2026 driver shares may sit on one board, never in one tile. A public estimate made before the agency’s own figure exists is DERIVED from named public sources, labeled as a public estimate, and replaced at the first opportunity.

## 4. The indicator specification (ten fields, versioned)

Every indicator, leading or lagging, is written to ten fields before its first value is recorded: identifier (IND-\[domain\]-\[number\]); name; definition; formula with explicit numerator and denominator; source system, report and field; owner (a named role); cadence and trigger; direction of good; linked driver and handoff; baseline value with date and the CUSUM shift target. Definitions are never amended in place: a change retires the identifier and opens a new one with a new baseline. The source is named specifically — "field X of weekly report Y produced by team Z," never "from the eligibility system."

### Selection, validation and retirement

An indicator earns a place on the board only if it moves before the error dollars do, is cheap to read every week, and belongs to someone who can act on it. Candidates are drawn from the failure modes of each top driver and scored 1–5 on six criteria before any data are pulled: mechanism proximity, availability, lead time, controllability, exclusivity, and gaming risk (scored in reverse). The top three to five per driver go forward to validation.

Validation is case-level, on review results the agency already holds (quality assurance, pre-authorization, find-and-fix and state QC), never on QC-sampled cases selected for the purpose. For a binary indicator with prevalence p among reviewed cases, report the relative risk RR of an error when the indicator is present; the attributable share of error dollars, PAF = p(RR − 1) / \[1 + p(RR − 1)\], computed on dollars; AUC for continuous indicators; and median lead time, each with an interval. Validated: lower bound of RR above 1.5 and PAF at least 10% of the driver’s dollars, on at least 200 reviewed cases. Provisional: below that. Rejected: the RR interval includes 1.

A validated indicator predicts; it does not prove cause, and its value as a target is tested in a registered design like any countermeasure. Every deployed indicator keeps an audit sample of cases where it reads clean, is re-validated each quarter, and is retired after two quarters below its threshold. No more than three indicators per driver are on the board. The specification adds four fields to the ten above: failure mode, lead time, validation status with its statistics, and gaming controls with the audit sample.

A language model may draft candidates, score their prior plausibility with a stated reason, and write specifications and extract queries against the agency’s data dictionary only, marking any field not in the dictionary "to confirm". It does not estimate correlations, sees no case data outside the agency’s environment, and its output is Hypothesis until validated.

## 5. The chart set

| **Chart** | **Use it for** | **Specification** |
| --- | --- | --- |
| Tri-mandate strip | PER, CAPER and APT side by side | Point estimate ± 1.96·SE for PER and CAPER; tier bands and points-to-next-tier on PER; 95% line and 30-day / 7-day split on APT; raw-vs-official badge; cadence stamp on each tile |
| Two-bills strip | The dollars behind the rate | Benefit cost-share at stake at the current tier, dollars saved by crossing the next tier line, and points to that line with the interval; administrative bill at the 75% state share and the state cost of one staff-year; each tile names its year and source |
| Shewhart p-chart | Small, similar-size subgroups (30–50-case node samples) | 3σ limits from actual n; Nelson rules |
| g-chart or time-between-escapes CUSUM | Rare-event nodes (fewer than five expected defects per subgroup) | Counts cases between escapes; a p-chart cannot see a shift at a controlled node near 2% with n = 50 |
| Laney p′ chart | Variable or large n (monthly raw rate; mined node rates) | z_i = (p_i − p̄)/√(p̄(1−p̄)/n_i); σ_z = mean moving range of z / 1.128; limits p̄ ± 3·σ_z·√(p̄(1−p̄)/n_i). Corrects over- and under-dispersion so alarms are shifts, not sample-size artifacts |
| XmR (individuals and moving range) | Error dollars per \$1,000 issued; persistence-weighted loss | Limits at mean ± 2.66·MR̄; MR limit 3.267·MR̄ |
| Tabular CUSUM | Weekly leading indicators | Standardized z; k = half the shift of interest (default 0.5σ); h = 4–5σ; C⁺ and C⁻ tracked; shift target written in the indicator spec |
| Pareto with waterfall | Error dollars by driver, addressable vs residual floor | Dollar-weighted; tolerance shown as excluded but visible; over- and under-payment separate |
| Coverage matrix | Driver × initiative × indicator, with a capacity column | Ownership is exclusive before movement is graded; every initiative shows its attribution status; the capacity column stays locked until the review-workforce baseline exists; shared indicators marked "not attributable" |
| Projection tile | Whether the portfolio still closes the gap to the target | PROJECTED points by lever and driver, with the basis of each yield; shown on its own, never as a trend beside the official, state-reported or raw rate |
| Rate bridge | Who moved which dollars between two rates | Waterfall: each graded initiative’s points; outside effects from the regime calendar; change in the federal regression adjustment; sampling noise; unattributed remainder, never hidden. Nothing is shown larger than its measured effect |
| Scale-readiness card | Whether a check can go statewide | Four lines (error effect, capacity ρ, yield to beat, guardrails) before the pilot, at the scale gate and after rollout; verdict Scale, Scale with conditions or Hold |
| Locked panels | Measures whose data does not yet exist | Shown, labeled, inert — never omitted |

### Special-cause detection (Nelson rules)

\(1\) one point beyond 3σ; (2) nine consecutive on one side of center; (3) six consecutive rising or falling; (4) fourteen alternating; (5) two of three beyond 2σ on one side; (6) four of five beyond 1σ on one side; (7) fifteen within 1σ (stratification); (8) eight consecutive beyond 1σ on both sides (mixture). A signal is reported with the rule that fired. Movement inside the limits with no rule firing is reported as common cause. The default detection set is rules 1, 2, 5 and 6, with the in-control average run length published for each chart; rules 3, 4, 7 and 8 are investigation aids, not alarms.

### Limit setting (Phase I) and monitoring (Phase II)

Limits are set from at least 20–25 subgroups judged stable, then frozen. Until then every chart carries a "limits provisional" stamp and no special cause is reported. Limits are re-set after a confirmed process change, a re-baseline or a regime window. A monthly raw rate yields twelve subgroups a year and is a Phase I chart for its first two years; weekly indicators are where early signals live. Every controlled node has a named process owner, standard work, and an out-of-control action plan that says who acts, and within what time, when a chart signals. A chart without one is a picture, not a control.

### Rational subgrouping and regimes

Caseloads under a different regime — disaster program (7 CFR 280), mass change, system cutover, policy effective date — are tagged and charted separately; a phase line marks every regime boundary and every intervention start. Commingling a two-week disaster surge with the baseline corrupts limits for months.

## 6. Measurement system requirements

- Before a sampled rate counts, two or three reviewers independently score 20–30 shared cases against the written criteria; agreement (Fleiss' kappa) must reach 0.75 (target 0.80). Disagreement is resolved by tightening the criterion, not by averaging.

<!-- -->

- Samples are drawn from non-QC-sampled cases only, de-identified, reported in aggregate; 30–50 cases per node gives a proportion with a usable interval.

- Attestation is collected from both sides of a handoff (sender and receiver) and never averaged; the receiver's figure governs.

- Each component carries its own cadence stamp — per QC cycle, weekly, on change, on re-baseline, continuous. A single global "live" timestamp is prohibited.

- Before any detector, review rule or worklist is deployed, the review workforce is baselined: errors found per review hour, capture rate and false-positive rate. This is the yield a new check must beat and the starting point of its queue.

- Capacity figures carry their basis: touch time from walkthrough bands, work sampling, a time study or recordings; waits from the event log. Where staff serve several programs, the program’s share is allocated before any hour is counted. Hours are reported by office or team, never by worker.

- A state-run shadow QC sample, where used, is reviewed to QC standards by reviewers separate from official QC and never touches QC-sampled cases.

## 7. Attribution

A claim that an intervention changed a rate requires a design registered before rollout: the unit of assignment (office, county, consortium, region), the assignment rule (staggered, matched or randomized), the primary indicator expected to move, the expected direction and rough size, and the observation window. At window close the effect is estimated (difference-in-differences, synthetic control, or interrupted time series on the indicator) and graded. Without a registered design, movement is reported as "correlation in time." Ownership of an indicator is exclusive before its movement is graded. The scale gate is numeric and is agreed, with the statewide rollout scheduled, before the trial starts; it is not renegotiated at the gate. Where assignment units number fewer than ten, inference is by permutation or wild-cluster bootstrap, stated in the design.

### Faster designs

Where contamination allows, assignment is by case or worker inside the routing or prompt tool; otherwise units go live in waves whose order is drawn by lot. Weekly outcomes may be read against group-sequential or sequential-probability-ratio boundaries fixed in advance, so a clear effect scales in weeks and an unclear one runs its full window. Factorial designs, multi-armed bandits (with a fixed-allocation arm kept for the registered estimate) and uplift routing trained on trial data only are permitted on the same terms. Capture–recapture estimates of error not yet found are Indicated, never Evidenced. Small-area (hierarchical Bayes) rates are shown with intervals, never as league tables of workers. A node is declared under control only by acceptance sampling: with no errors in n random reviews, the 95% upper bound on its rate is 3/n.

### Attribution in error dollars

Every initiative in the register carries one attribution status: Unregistered, Registered (with its registration date), Running, Graded (Evidenced, Indicated or Hypothesis) or Not effective. An unregistered initiative cannot claim a dollar, and from the first board the count of initiatives that can and cannot claim is shown.

Each initiative has a dollar chain of three columns: activity (what it or its vendor reports), node effect (the change in the escaped-defect rate at the step it targets) and error dollars (node effect × the driver’s dollars through that node × the initiative’s coverage). Vendor-reported figures enter the activity column only. Where initiatives work the same driver at the same node, shared dollars are credited once, in product form, 1 − Π(1 − yᵢ·cᵢ); claims that together exceed what the driver lost are marked Contested.

Between any two rates the account is a bridge: points from graded initiatives; outside effects from the regime calendar; the change in the federal regression adjustment; sampling noise; and the unattributed remainder, which is always shown. Because the official rate rests on about a thousand sampled cases a year, no single initiative’s effect can be read from the published number. Attribution is measured at the node and in the driver’s dollars, reconciled to the official rate within its interval, and the statement says so.

## 8. Capacity

No detection, review or check is deployed without a capacity plan. For each affected node: arrival rate, service rate, reviewer count; utilization held at or below 0.85; expected wait from the queue model solved so that the probability of breaching the 30-day (regular) or 7-day (expedited) processing standard stays under 5%. Work-in-process is reconciled to Little's Law from counts the agency already produces.

### Scale readiness

Before a detection, review rule or check goes statewide, a scale-readiness card is produced at three moments (before the pilot, at the scale gate and after rollout) on four lines: error effect (PROJECTED, then graded); capacity, ρ = hours needed ÷ hours available, from the flag rate, statewide volume, minutes per review and the review-workforce baseline; the yield to beat; and guardrails (CAPER, timeliness and household burden). Scale when the graded effect clears its registered gate and ρ ≤ 0.85. Scale with conditions when the effect clears and capacity does not: narrow to the highest expected dollars, roll out in waves, or fund review from released capacity, each option shown with its effect on hours and on projected points. Hold when the effect does not clear or a guardrail worsens.

### Capacity and process efficiency

| **Measure** | **Definition** | **Basis as data matures** |
| --- | --- | --- |
| Touch time | Worker minutes per task and case type | Walkthrough bands → work sampling or time study → log, where start and end are recorded |
| Cases per worker | Completed actions per productive FTE-month by case type, program share allocated | Aggregates → measured → log |
| Process cycle efficiency | Touch time ÷ elapsed time, by step and office | Estimated → performance analysis of the event log |
| Failure demand | Work caused by an earlier failure of the process (§1) | Aggregates → sampled → log |
| First-pass yield and rework | Share of actions completed without a loop; recomputations, bounced handoffs and restarts per case | Case samples → log |
| New required work | Minutes per task × monthly volume for work new law adds (for SNAP, H.R. 1 work-requirement exemptions, countable-month tracking and hours verification) | Agency estimate → measured |
| Household outcomes | Families asked twice for the same document; re-application within 90 days of a denial or closure | Aggregates → sampled → log |
| Released capacity | Σ(volume × minutes saved) ÷ productive minutes per FTE, with interval, booked by destination | Measured changes only |

Released hours are spent by a plan the agency signs, in this order: new required work (including H.R. 1 tasks and caseload growth), then quality-assurance and pre-authorization review, then training and complex casework. The standard reports hours and their value, not positions; any headcount change is the agency’s decision. An efficiency change is registered and graded like any countermeasure, and is not adopted if its node error rate, CAPER, timeliness or household measures move the wrong way. Released capacity is shown as budget absorbed or hours reinvested, never as a saving until the agency books one.

## 9. Automation and human decision

- Automation removes or mistake-proofs steps; it never determines eligibility, calculates a binding budget, or takes an adverse action. Certification is reserved to merit-system personnel (7 U.S.C. 2020(e)(6)(B)). A check may require an affirmative action; it never withholds a merit worker's authorization.

- Cognitive forcing is mandatory where an automated output is presented: visual diff of reported vs extracted values; affirmative checkpoints before a budget saves; structured override reasons; time-on-case telemetry with rapid approvals routed to second-party review.

- In-workflow assistants operate within written budgets: added latency per case (≤60 s), inline response (≤1.5 s), false-flag rate per module (≤5%), a biweekly cross-functional review of flags, actions and overrides, and a kill switch that is drilled.

- Presentation-layer automation (screen or terminal scraping) is used only where no API or event interface exists, and only behind a circuit breaker that detects failure within minutes, reroutes to the worker queue and alerts a supervisor.

- Equity: extraction accuracy, confidence and latency are tested for parity across language, document type and income type; targeting and routing models carry no demographic or geographic features.

- In-workflow checks are deployed first as sidecars to the eligibility system, so they can be switched off without a system change, and move into the core system only after they have been graded.

## 10. Federal quality control firewall

Only post-transmission aggregate QC data enters management measurement. Cases pulled for the federal QC sample are never selected for review, correction, prioritization or automation before transmission; suppression is implemented so that no worker or office can infer which cases are sampled. Vendor discussion of any sampled case is documented and open to FNS. Contractors touching QC processes or policy training give FNS 30 days' notice with deliverables (Handbook 310 §154). Sub-threshold errors are excluded from the rate but reported for corrective action (§623). The tolerance threshold is indexed annually (\$57 FY2025, \$58 FY2026); it has not been eliminated.

Four routes to a lower reported rate are ruled out: touching, prioritizing or re-working cases because they are in the QC sample; pressing for lenient QC findings, or shielding QC reviewers’ decisions from federal re-review; denying or closing cases defensively, which moves error into the negative rate and harms eligible households; and correcting overpayments in ways that create underpayments. State QC findings believed wrong go to federal arbitration on their merits, with a documented case, and QC reviewers are never told which cases matter to a tier line.

## 11. Targets, the two bills and reporting

### 11.1 Targets and projections

An engagement that sets a target writes down the tier line, the governing rate year and the confidence of landing under it: R\* = threshold − z·SE and ΔR = R0 − R\*. A lever projection tests feasibility: ΔR_d = R0 · s_d · \[1 − Π_l (1 − y_d,l · c_d,l)\], summed over drivers, where s is the driver’s share of error dollars and y and c are each lever’s yield and coverage. The product form stops two levers being credited for the same dollar. The verdict is Feasible when the lower bound (70% of assumed yields) meets ΔR, Stretch when only the central value does, and otherwise not feasible in that rate year; the tier or the year then moves, in writing. Assumed yields are replaced by measured ones as they arrive. A probability-of-tier nowcast may combine a shadow QC panel, state QC and the historical regression adjustment. All of these are PROJECTED (§3).

### 11.2 The two bills

Wherever the rate is shown against its tiers, its value is shown in both bills. The benefit cost-share: under current law, from FY2028 a share of benefit costs set by the governing year’s rate, with none below 6%, then 5%, 10% and 15% at the 6%, 8% and 10% lines, and a delay for a state whose rate multiplied by 1.5 is 20% or more. The administrative bill: from FY2027, which began on 1 October 2026, the state pays 75% of SNAP administrative costs, up from 50% (H.R. 1; FNS proposed rule of 24 June 2026). An error point therefore has a dollar value at the tier line, and a freed staff hour saves the state three-quarters of its cost rather than half. The state cost of one staff-year is loaded cost × program share × 75%, labeled a public estimate until the agency supplies its own figures.

### 11.3 Reporting to a corrective action plan

| **7 CFR 275.17 element** | **B-SPC component** |
| --- | --- |
| Description of each deficiency | Dollar-weighted driver attribution; CTQ nodes |
| Source through which detected | QC findings plus the process baseline for the mechanism |
| Magnitude and geographic extent | Dollar and persistence weighting; office-level cuts |
| Causal factors | The handoff where the error enters; deviation-to-dollar link |
| Actions, expected outcomes, target dates | Initiative register with the addressable-vs-floor ceiling; target plan and lever projection (PROJECTED) |
| Manner of monitoring and evaluating effectiveness | Leading indicators on control charts; registered designs; evidence grades; attribution ledger and rate bridge |

Semiannual updates (1 May / 1 Nov) are exported from the register, not written from memory. CAPER above the national average and timeliness below 95% are reported in the same submission. The attribution statement (the rate bridge, graded dollars by initiative and what nobody can claim, with method and intervals) is issued at each FNS release, each state budget request and each 1 May / 1 November update, and becomes the evidence section of the plan.

## 12. Conformance and independence

A product or engagement conforms to B-SPC when every published figure carries a basis tag and an interval, every movement claim carries a grade, the tri-mandate strip is present, charts use limits and rules as specified, the QC firewall holds, and every figure is exportable and independently recomputable from the agency's own data by any party the agency chooses — including one checking the publisher. Zeluca accepts no commissions, referral fees or reseller margins from any vendor whose work passes through a B-SPC evaluation it conducts, and applies the same evidence gates to components it builds. The measurement role (target plan, projection, indicator validation and trial results) is kept independent of whoever delivers a countermeasure; results are registered before they are known and reported whether or not they favor the countermeasure. Corrections to this standard are welcome at methods@zeluca.com; a revision is issued with every full life cycle engagement completed in the field.

## 13. Worked example (illustrative figures)

A state with 1,050 completed QC reviews publishes 9.44% with a standard error of 1.24: the 95% interval is 7.0–11.9%, spanning three tiers. Its AC06 export ranks wages and salaries (311) first at \$5.3M of error dollars; AC03 timing shows 61% of those errors entered at the most recent action. The as-designed map places the income-determination handoff between "verification received" and "budget computed"; the acceptance criterion (SOURCED, state manual §24.14 and 7 CFR 273.9) requires a pay-period-complete stub set and a documented conversion factor. Mirror attestation gives 45–65% complete-and-accurate at that handoff (ATTESTED). A 50-case non-QC sample scored by three reviewers (κ = 0.81) gives 58% (SAMPLED, Wilson 95% CI 44–71%). The escaped-defect floor from AC03 is 9%. Severity: \$5.3M × an expected 4.2 months undetected; occurrence 0.42; detection 0.30 (a second-party review exists at 30% of cases) → the highest risk-priority number on the path. The registered design: a pre-authorization income check rolls out to the three largest county offices first, then the rest at week six; the primary indicator is "income cases with second-party review before authorization," expected up; window twelve weeks. At window close the CUSUM on that indicator fires at week seven for the early offices and not for the later ones, and the difference-in-differences estimate on the node yield is +11 points (CI +4 to +18): graded Evidenced. The monthly raw rate on the Laney p′ chart shows no special cause — expected, since the sample cannot resolve a change this size within the window, which the detectability calculator said in advance. The corrective action plan update reports the node yield, the indicator movement and the grade, and states that the official rate will not be able to confirm the effect until the next cycle.

**Continued (v2.6, illustrative).** The state targets the 8% line in the FY2027 rate year, which sets its FY2030 share, with z = 1.0: R\* = 8.0 − 1.24 = 6.76% and ΔR = 2.68 points. The lever projection on the top two drivers gives 2.9 points central and 2.0 at 70% of assumed yields: Stretch. In dollars, on \$1.0 billion of annual benefits the state sits at the 10% share, \$100 million a year; the 5% share would cost \$50 million. Its \$80 million administrative cost now costs it \$60 million a year, \$20 million more than under the 50% share, and one SNAP staff-year at a loaded \$95,000 and a 60% program share costs it about \$43,000. Before the income check goes statewide, its scale-readiness card reads 1,000 flags a week at 18 minutes: 300 hours needed against 240 available, ρ = 1.25. Limited to the 60% of flags with the highest expected dollars, it needs 180 hours, ρ = 0.75: Scale with conditions, at a smaller projected effect that the card shows. At the next release the published rate is 8.9%. The bridge credits the income check with 0.30 points (its graded node effect × the wages dollars through the node × statewide coverage), outside effects on the regime calendar with 0.10 and the change in the federal regression adjustment with 0.05, and shows 0.09 points unattributed. The attribution statement adds that the whole 0.54-point change lies inside the sampling noise of the difference between two published rates, and that two other initiatives, never registered, cannot claim any of it.

## 14. Conformance checklist

| **\#** | **Requirement** | **Evidence of conformance** |
| --- | --- | --- |
| 1 | Every published figure carries a basis tag, its window and its n | Figure metadata; sample of ten figures inspected |
| 2 | Every rate carries an interval; no rolled yield without its chain | Chart set; %C&A report |
| 3 | Every movement claim carries a grade, and Evidenced claims cite a registered design | Design register; attribution readouts |
| 4 | Tri-mandate strip present wherever PER is shown | Board; CAP export |
| 5 | Charts use the specified limits and Nelson rules; signals name the rule | Chart configuration; alarm log |
| 6 | Rational subgrouping by regime; phase lines on every chart | Regime calendar; charts |
| 7 | Indicator specifications complete in ten fields; changes retire and re-issue identifiers | Indicator register with version history |
| 8 | Reviewer agreement demonstrated before any sampled rate is published | Kappa report per sample cycle |
| 9 | Capacity plan on file for every review, check or detector before deployment | Queue model outputs; timeliness check |
| 10 | No eligibility decision, binding budget or adverse action automated; cognitive forcing present; budgets and kill switch documented | Design review record; C-42; drill log |
| 11 | QC firewall: aggregates only; sampled cases never selected or suppressed visibly; §154.9 notices issued | Data request kit; registry design; notices |
| 12 | Every figure exportable and recomputable from the agency's data by a third party | Export package; recomputation test |
| 13 | Publisher discloses any commercial interest in components it scores; applies the same gates to its own builds | Independence statement |
| 14 | Every projection tagged PROJECTED, never graded and never trended beside a measured rate | Target plan; projection tile |
| 15 | Every initiative carries an attribution status; dollars shown only at the registered grade; overlap credited once; unattributed remainder always shown; vendor figures in activity only | Attribution ledger; rate bridge; attribution statement |
| 16 | Scale-readiness card with ρ ≤ 0.85, or stated conditions, before any check goes statewide | Card per initiative, at each gate |
| 17 | Capacity and efficiency figures carry their basis and are reported by office or team; released hours booked to a plan the agency signs | Capacity baseline; release plan and ledger |
| 18 | Every figure names its year and source; no tile mixes years; LOCKED, UNAVAILABLE and REFUSED shown with a reason, never as zero | Board package metadata |
| 19 | Leading indicators validated on case-level review results before deployment; audit sample kept; re-validated quarterly | Validation report; audit samples |
| 20 | Limits provisional until 20–25 stable subgroups; default detection set with published run length; owner and out-of-control action plan for every controlled node | Chart configuration; OCAP file |
| 21 | Both bills shown in dollars wherever the rate is shown against its tiers | Board; attribution statement |

### 14.1 Applicability at the Look (Phase 0)

A three-week Look cannot produce the subgroups, samples or graded designs some rows require. At the Look, a product or engagement conforms when every row marked Applies is met, every row marked Document is on file, and every row marked Not yet is shown on the board as LOCKED with its reason.

| **\#** | **At the Look** | **Why** |
| --- | --- | --- |
| 1, 2, 4, 12, 18 | Applies | Tags, windows, n, intervals or attested bands, the tri-mandate strip, year and source, and recomputability hold from the first figure |
| 3, 15 | Applies | No movement is graded at the Look: coverage and correlation in time only, "not yet earned" on first load; each initiative’s attribution status is shown |
| 7 | Applies | Indicator specifications are signed; baselines arrive in Phase 1 |
| 14, 21 | Applies | The target, projection and both bills are part of the Look read-out |
| 17 | Applies, as bands | Capacity from walkthrough bands and public estimates, labeled as such |
| 5, 20 | Not yet | No chart can report a signal before 20–25 stable subgroups; charts carry "limits provisional" |
| 6 | Partly | The regime calendar starts at the Look; phase lines apply once charts run |
| 8, 19 | Not yet | No sampled rate is published and no indicator is validated at the Look |
| 16 | Not yet | The capacity column stays locked until the review-workforce baseline exists in Phase 1 |
| 10 | Not applicable | Nothing is automated at the Look |
| 9, 11, 13 | Document | Capacity-plan rule, QC data request kit and notices, and the independence statement |

## 15. Instrument glossary

The instruments the standard expects, by the phase in which they first appear. Full formulations are in the AGBER methodology v2.6, Appendix A.

| **Phase** | **Instruments** |
| --- | --- |
| Look (0) | Dollar-weighted driver Pareto and waterfall · as-designed map with citations and sufficiency report · as-practiced overlay and variance register · federal-vs-state alignment check · tri-mandate strip (PER with interval and bands; CAPER; APT) · indicator specifications and baselines · coverage matrix (capacity column locked until the review-workforce baseline exists) · policy complexity profile · directional %C&A bands · regime calendar and telemetry-use statement · target plan, lever projection and track · policy-option sizing · the two bills · attribution status of every initiative · capacity and cost bands and waste register · QC accuracy and arbitration log |
| Measure (1) | Sampled %C&A per handoff with Wilson intervals · reviewer agreement report · FMEA risk priority · persistence-weighted cost by node · Shewhart p and Laney p′ charts · CUSUM on weekly indicators · error-dollars-per-\$1,000 XmR chart · detectability calculator · queue model with timeliness constraint · signed baseline and reproducibility record · registered counterfactual designs with numeric scale gates · review-workforce baseline · CAP export in 275.17 fields · find-and-fix yield ledger · projection tile · indicator validation report · probability-of-tier nowcast · scale-readiness card · dollar chain and overlap check · measured capacity baseline and release plan · out-of-control action plans, standard work and daily management board |
| Watch everything (2) | Conformance and deviation map with log coverage · deviation-to-dollar attribution · Kaplan–Meier survival on pending states · mined %C&A across all cases · intervention attribution readout (DiD / synthetic control / ITS) · discrete-event simulation · automation candidate ranking · process-variable feed · shadow QC panel and undetected-error estimate · node acceptance certificate · rate bridge and portfolio table · performance, rework and failure-demand analysis of the log · hours-returned-to-quality-assurance ledger |
| Remove the step (3) | Before/after node Laney p′ with phase line · hours-returned ledger · false-positive and override report · boundary and citation audit · multi-program consistency matrix · bot health and circuit-breaker telemetry |
| Add a helper (4) | Agent latency and throughput · false-flag and override governance ledger · agent-assisted node charts · workload and client-outcome panel · cognitive-forcing telemetry audit · equity and language-parity audit |
| Keep learning (5) | Indicator vitality report · evaluation-corpus delta report · cross-state node benchmark · three-year sustainment ledger · attribution statement at each FNS release, budget request and CAP date · capacity control charts and staffing model |

## 16. Revision and citation

B-SPC v2.6, 1 October 2026. Supersedes v2.3. The version number now follows the AGBER methodology it accompanies; no B-SPC v2.4 or v2.5 was issued, and references to "B-SPC v2.4" in earlier project documents mean v2.3 read with AGBER v2.4. v2.6 adds limit-setting discipline, the default detection set and rare-event charts (from AGBER v2.4); the PROJECTED tag, target and projection rules, faster designs, and indicator selection, validation and retirement (v2.5); and the two bills, attribution in error dollars with the rate bridge, the scale-readiness card, capacity and process-efficiency measures, figure statuses, the year-and-source rule, eight conformance rows and the applicability of every row at the Look (v2.6). Cite as: Zeluca Inc., Benefits Statistical Process Control (B-SPC) Standard v2.6, October 2026. The standard is free to use, adapt, cite and improve under the Creative Commons Attribution 4.0 International license (CC BY 4.0). Field experience and disagreement are requested; the next revision is expected after the method has been used in a state across one full QC cycle.
