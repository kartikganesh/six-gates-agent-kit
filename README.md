# Take the gates home

Public companion kit for security researchers, builders, and report reviewers attending **The Six Gates That Kill a Vulnerability Report**.

Use these Markdown files to make an agent ask better questions, preserve evidence, and write a claim a reviewer can check. They are portable instructions and templates. Their filenames do not imply installation or automatic loading by any agent.

## Get the files

Open this README from the local kit folder or ZIP. Attach the files you need or provide their contents through your agent's normal context workflow. If the speaker later provides a repository link, you can download or clone its files instead. An agent that can access those repository files still needs an explicit instruction to read them.

Start with `SIX-GATES.md` and `FINDING-TEMPLATE.md` for a candidate, or `SIX-GATES.md` and `TRIAGE-REPLY.md` for a review. Ask the agent to name the files it actually read before applying them. If it cannot access a file, provide it explicitly. A repository link alone does not establish that the agent has read the instructions.

When sharing the resulting assessment, record the repository revision or file copy used alongside the finding's evidence. Review the output yourself against the actual observations.

## Choose a starting point

| Audience | File | Use it to |
| --- | --- | --- |
| Researcher or builder | `SIX-GATES.md` | Assess a candidate and identify the next missing fact. |
| Researcher or builder | `FINDING-TEMPLATE.md` | Turn evidence into a bounded, reviewable finding. |
| Report reviewer | `TRIAGE-REPLY.md` | Give an evidence-based decision and a useful next step. |

Attach or explicitly provide the relevant files using your agent's normal context mechanism, then give it the candidate, relevant source, and evidence you are authorized to share.

## Prompts to copy

**Assess a candidate**

> Read SIX-GATES.md and FINDING-TEMPLATE.md. Name the files you read, then assess this candidate. Separate verified observations, source-based inferences, and unknowns. Give technical validity and reporting eligibility separate conclusions. Suggest only next steps permitted by the authorization I provide.

**Reply to a report**

> Read SIX-GATES.md and TRIAGE-REPLY.md. Review this report and its evidence. Write a concise reply that identifies the decisive evidence or missing fact. Do not treat missing evidence as proof that the claim is false.

**Check a repair**

> Read SIX-GATES.md. From the stated security rule, propose an authorized normal-use test and a forbidden-behavior test. Identify the expected result of each. If you cannot run them, label the plan as unexecuted.

## A teaching example

In the talk's separate local preview app, the intended rule is to return images only from the preview folder. A normal request returned Earth. A changed request returned Moon from outside that folder. After repair, the normal request still returned Earth and the outside request returned no image.

That evidence supports a finding about the local teaching app under its tested conditions. It does not establish reproduction in a product installation or disclosure of every file type.

## Before sharing a report

Review the agent's output against the raw evidence and the applicable policy. Keep secrets out of the shareable report while preserving an authorized, protected original. These files help structure research and review; they do not predict a program's acceptance decision.

Companion materials for Kartik Ganesh's talk at Rebellion, **The Six Gates That Kill a Vulnerability Report**.
