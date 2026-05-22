# Nessus-Based Risk Assessment Report

Methodology-aligned report for vulnerability-derived risk identification, scoring, evaluation, heat mapping, and treatment.

---

## Prepared For
**SLIMTECH**

## Assessment Basis
Nessus vulnerability scan output and analyst-led risk scoring

## Prepared By
**Olushola Ajala**

## Assessment Date
**10.05.2026**

---

> **Note:**  
> This document is intentionally written so it can be used as a professional report even when the final vulnerability list is still being compiled. Replace bracketed placeholders and populate Appendix A with the actual Nessus findings before final submission.

---

# Executive Summary

This report presents a structured risk assessment derived from vulnerability information identified through a Nessus scan. The assessment follows a practical sequence:

- Risk identification
- Risk scoring
- Risk evaluation against organizational risk appetite
- Risk heat mapping
- Risk treatment selection

The purpose of the assessment is not only to list technical weaknesses, but also to translate those weaknesses into business-relevant risk statements that support remediation planning and management decision-making.

Using Nessus output as the primary technical source, each vulnerability is reviewed and classified by severity, then assessed for exploitability and impact. These factors are combined into a risk score that is subsequently compared with the organization's stated or assumed risk appetite.

Findings that exceed acceptable thresholds should be prioritized for treatment, while lower-rated issues may be monitored, accepted, or scheduled for remediation based on operational context.

---

# 1. Assessment Overview

## 1.1 Objective

- Assess vulnerabilities identified from the Nessus scan
- Determine relative organizational risk using a defined scoring methodology
- Prioritize remediation based on:
  - Business impact
  - Exploitability
  - Alignment with organizational risk appetite

---

## 1.2 Scope

This assessment covers vulnerabilities identified on:

- Assessed assets
- Systems
- Applications
- Network segments included in the Nessus scan

The analysis focuses on risk arising from discovered technical weaknesses and does not replace:

- Enterprise risk management
- Architectural reviews
- Compliance audits

---

## 1.3 Method Summary

| Stage | Purpose | Outcome |
|---|---|---|
| Risk Identification | Review Nessus findings and classify vulnerabilities by severity and exposure context | Initial risk register |
| Risk Scoring | Rate exploitability and impact for each finding | Comparable risk scores |
| Risk Evaluation | Compare scores to the organization's risk appetite | Priority decisions |
| Risk Matrix Plotting | Position findings on a heat map using probability and impact | Visual prioritization |
| Risk Treatment | Select the most suitable response for each risk | Remediation plan |

---

# 2. Risk Identification

Risk identification began with the review of the Nessus scan results to determine the vulnerabilities present in the environment and their associated severity ratings.

Nessus classifications such as:

- Critical
- High
- Medium
- Low

provide an initial indication of technical seriousness, but they do not by themselves represent full organizational risk.

Each vulnerability should therefore be translated into a risk statement that reflects:

- The affected asset
- The identified weakness
- The potential adverse outcome if exploited

This process helps move the analysis from technical findings to business-relevant risk understanding.

Where appropriate, validation can be performed to confirm:

- Whether the issue is exploitable
- Whether compensating controls exist
- Whether the affected asset is business-critical

---

## Severity Classification

| Severity | Interpretation | Typical Priority |
|---|---|---|
| Critical | Very severe weakness that may lead to immediate compromise, service disruption, or unauthorized access | Immediate action |
| High | Serious weakness with strong exploitation potential or significant impact if exploited | Urgent remediation |
| Medium | Moderate weakness that should be addressed in a planned remediation cycle | Scheduled remediation |
| Low | Limited impact or exploitability, though still relevant for hygiene and hardening | Monitor or remediate as resources permit |

---

# 3. Risk Scoring Methodology

After identification, each vulnerability is scored by considering two core dimensions:

1. Exploitability
2. Impact

This ensures the final score reflects both:

- Likelihood of successful attack
- Organizational consequence if exploitation occurs

---

## Scoring Scale

| Factor | Low (1) | Medium (2) | High (3) |
|---|---|---|---|
| Exploitability | Exploit is difficult, requires rare conditions or strong attacker capability | Exploit is possible with moderate effort or partial access | Exploit is straightforward, publicly documented, or readily weaponized |
| Impact | Minor operational effect or limited business consequence | Noticeable service, integrity, or confidentiality impact | Major business disruption, sensitive data exposure, or compromise of critical assets |

---

## Risk Score Formula

```text
Risk Score = Exploitability + Impact
```

---

## Risk Rating Table

| Score Range | Risk Rating |
|---|---|
| 2 | Low |
| 3–4 | Medium |
| 5–6 | High |

---

# 4. Risk Evaluation Against Risk Appetite

Risk evaluation determines whether scored vulnerabilities fall within or outside the organization's acceptable risk tolerance.

This stage converts technical scoring into a management decision tool.

---

## Typical Appetite Model

| Risk Rating | Appetite Position | Required Action |
|---|---|---|
| Low | Within appetite | Accept, monitor, or address during routine hardening |
| Medium | Conditionally tolerable | Remediate within agreed timeline and track to closure |
| High | Above appetite | Escalate and treat immediately with ownership and due date |

---

# 5. Risk Matrix and Heat Map Positioning

Each vulnerability is positioned on a risk matrix using:

- Impact
- Probability

Probability may be informed by:

- Exploitability
- Exposure level
- Public exploit availability
- Required attacker effort

Impact reflects likely business consequences if exploitation occurs.

---

## Risk Heat Map

|  | Low | Medium | High |
|---|---|---|---|
| High | Medium | High | High |
| Medium | Low | Medium | High |
| Low | Low | Low | Medium |

**Figure 1:** Example risk heat map using Impact versus Probability.

---

# 6. Recommended Risk Treatment Techniques

Once evaluated, an appropriate treatment option should be selected.

Treatment decisions should consider:

- Urgency
- Cost
- Feasibility
- Business dependency
- Compensating controls

---

## Risk Treatment Options

| Treatment Option | Description | Typical Use Case |
|---|---|---|
| Mitigate | Reduce risk through controls or corrective actions | Patch software, harden configurations, enforce MFA |
| Accept | Formally acknowledge the risk | Low-risk findings with monitoring in place |
| Transfer | Shift part of the risk impact to another party | Cyber insurance or MSSP arrangements |
| Avoid | Eliminate the activity or condition creating the risk | Decommission unsupported systems |

---

## 6.1 Recommended Treatment by Risk Level

### Critical and High Findings
Should normally be:

- Mitigated immediately
- Assigned ownership
- Tracked to closure

### Medium Findings
Should be:

- Scheduled within remediation timelines
- Monitored where immediate remediation is not possible

### Low Findings
May be:

- Accepted
- Remediated during standard hardening cycles
- Monitored for escalation risk

---

# 7. Conclusion

This risk assessment approach converts Nessus scan output into a defensible and management-friendly process for prioritizing vulnerability remediation.

By progressing through:

1. Identification
2. Scoring
3. Evaluation
4. Matrix placement
5. Treatment

the organization gains a clearer understanding of:

- Greatest areas of exposure
- Remediation priorities
- Governance alignment

The final value of the report depends on:

- Accurate risk register population
- Consistent scoring methodology
- Alignment with organizational risk appetite

Once the Appendix is completed with actual findings, this document can serve as both:

- Technical reporting artifact
- Governance and management reporting document

---

# Appendix A — Nessus Findings Register

> Replace the placeholders below with actual Nessus findings.

| Vulnerability | Asset | Severity | Exploitability | Impact | Risk Score | Treatment |
|---|---|---|---|---|---|---|
| [Finding 1] | [Asset Name] | High | 3 | 3 | 6 | Mitigate |
| [Finding 2] | [Asset Name] | Medium | 2 | 2 | 4 | Scheduled Remediation |
| [Finding 3] | [Asset Name] | Low | 1 | 1 | 2 | Accept / Monitor |

---

# References

- Nessus Vulnerability Scanner
- Organizational Risk Management Policy
- Vulnerability Management Procedures
- Security Best Practices and Hardening Standards
