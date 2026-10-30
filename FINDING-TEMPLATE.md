# Finding evidence template

**Audience:** security researchers and builders.

Replace the bracketed fields with evidence. Leave missing facts marked **unknown**. Do not fill gaps with plausible details. Use `SIX-GATES.md` as the assessment instructions.

## Bounded headline

[Caller with stated permissions] can [observed added capability] through [controlled input] in [target and conditions].

## Decision snapshot

- **Technical validity:** [supported / unresolved / refuted, under which conditions]
- **Reporting eligibility:** [covered / excluded / unknown, policy basis]
- **Decisive fact:** [evidence supporting or contradicting the claim, or the missing fact]
- **Next step:** [permitted action and the question it resolves]

## Target and authorization

- **Target:** [product or teaching app, installation, version or commit, configuration]
- **Environment:** [local lab / test deployment / other authorized environment]
- **Authorization:** [reference, permitted actions, limits]
- **Evidence provenance:** [who collected it, when, environment, artifact identifiers]

## Boundary and added capability

- **Caller and baseline:** [role, existing permissions, what the caller can already do]
- **Controlled input:** [field, entry point, and reachable path to the operation]
- **Security rule:** [restriction and its basis in policy, design, configuration, or source]
- **Observed result:** [what happened, linked to the evidence]
- **Added capability:** [what the result adds beyond the baseline]
- **Impact limits:** [conditions, affected data or action demonstrated, untested extensions]

## Evidence a reviewer can follow

| Artifact | What it establishes | What it does not establish |
| --- | --- | --- |
| [Request or action identifier] | [Caller, input, prerequisite state] | [Unproven reachability or deployment conditions] |
| [Response, log, or result identifier] | [Observed result] | [Broader impact not demonstrated] |
| [Source or advisory reference] | [Code behavior or published affected conditions] | [Reproduction on this installation] |

**Reproduction:** [Minimal steps within the authorized environment, expected ordinary behavior, actual observed behavior. Label proposed steps as unexecuted.]

**Evidence handling:** [Protected raw originals, shareable redacted copies, relevant access limits. Do not include credentials or unnecessary personal data.]

## Gate assessment

| Gate | Answer and status | Evidence or missing fact |
| --- | --- | --- |
| Target still affected? | [supported / contradicted / unknown] | [reference] |
| Who controls the input? | [answer and status] | [reference] |
| What extra access appears? | [answer and status] | [reference] |
| What was observed? | [answer and status] | [reference] |
| Does the program cover it? | [covered / excluded / unknown] | [policy and date checked] |
| Is the claim defensible? | [bounded claim and remaining limits] | [reference] |

## Repair and verification

**Proposed repair:** [Restore the stated rule while preserving intended behavior.]

| Test | Expected after repair | Observed after repair |
| --- | --- | --- |
| Ordinary permitted use | [Intended result] | [Result and artifact, or unexecuted] |
| Forbidden behavior | [Refusal of the demonstrated added capability] | [Result and artifact, or unexecuted] |

**Remaining questions:** [Untested conditions or regressions relevant to this claim.]

**Shareable claim:** [Final sentence no broader than the recorded evidence.]
