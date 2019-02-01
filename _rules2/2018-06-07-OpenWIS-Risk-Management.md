---
layout: page
title: OpenWIS&reg; Risk Management
---

##### June 2018

This document describes the risk management process for risks to the OpenWIS Association. This is a supplement to the Articles of Association and Internal Rules. In the event of any discrepancy between the intentions noted in this document, meaning and governance shall be sought from the Articles of Association then the Internal Rules over this document. Note that individual projects being run or incubated by the Association each determine their own risk management process.

### Risk Management Process

Since Risks are just potential Issues, we use the Issue tracking built into GitHub to track Risks. This is done as follows:

1. Add a GitHub Issue to the openwis-documentation repository for each Risk: the title should start RISK-NNNNNN-title, where NNNNNN is the next available six digit number in sequence.
2. Add a detailed description of the Risk in the initial comment, using structured sentences.
3. Add estimated Impact and Probability (very low to very high) for financial, reputation and goals.
4. Assign risk RAG label (RED/AMBER/GREEN) accordingly.
5. Add the Issue to the GitHub project used to record the risk issues, to the appropriate column based on RAG.
6. Assign the risk owner(s) to the Issue.
7. If action on this risk is required outside the routine risk review cycle, assign a milestone for the next risk review or risk action.
8. Label with the Committee that is tracking eg: PMC/TC/SC/BM. If a risk is escalated, then change the label to the Committee it was escalated to. Label with RISK.
9. Add routine or ad-hoc risk reviews to the agenda of PMC/TC/SC meetings as required.
10. When necessary, PMC and TC would escalate risks to SC. PMC and TC would also provide a risk summary report to the Annual Meeting for review by both the SC and the Board.
11. The SC would escalate risks to the Board whenever they require Board decisions or actions to manage.
12. In general, project risks will be managed by the PMC, broader technical risks will be managed by the TC, risks to the Association will be managed by the SC, the Board will only manage risks escalated from the SC, usually because they need Board level actions/decisions according to the articles/rules. However. the Board may assume management of any risk at it's sole discretion.

**PROBABILITY scale:**

>|chance of occuring|description|% probability|
|---|---|---|
|Very Low| Unlikely |<5%|
|Low|Possible| 5-30%|
|Medium|Likely over time |30-50%|
|High| Likely| 50-75%|
|Very High|Likely and Imminent|>75%|

**IMPACTS assessments:**

>|Financial|€k|
|---|---|
|Very Low|<25|
|Low|25-50|
|Medium|50-75|
|High|75-100|
|Very High|>100|


>|Reputation| |
|---|---|
|Very Low|A few unhappy members/partners/contributors|
|Low|Several unhappy members/partners/contributors|
|Medium|Loss of potential members/partners/contributors|
|High|Loss of existing members/partners/contributors|
|Very High|Loss of credibility with WMO|


>|Goals| |
|---|---|
|Very Low|Minor impact on goals|
|Low|Significant impact on one goal|
|Medium|Significant impact on more than one goal|
|High|Failure to achieve one goal|
|Very High|Failure to achieve more than one goal|


**Probability/Impact matrix:**

>|prob\impact |VL|L|M|H|VH|
|---|---|---|---|---|---|
|VL|G|G|G|G|G|
|L|G|G|A|A|A|
|M|G|A|A|R|R|
|H|G|A|R|R|R|
|VH|G|A|R|R|R|

Where RAG status is: R=RED, A=AMBER, G=GREEN.

- RED = Immediate action required to mitigate, avert or otherwise manage the risk.
- AMBER = Plan of action required for managing the risk in the future.
- GREEN = Level of risk acceptable, no action required apart from monitoring.

Although a project PMC doesn't have to use the risk register structure above (each project manages its risks as agreed by the project) it might be useful because the Project Management Committee will need to escalate any risks to the Steering Committee that are a threat to the Association. They may also transfer technical risks that have wider implications than just the project, to the Technical Committee.

See the OpenWIS Association [risk log](https://github.com/OpenWIS/openwis-documentation/projects/4).

Individual risks will be reviewed by the Steering Committee on a schedule appropriate for the management of that risk, and by exception (ex-committee) if a risk requires urgent attention. The Steering Committee will review the entire [risk log](https://github.com/OpenWIS/openwis-documentation/projects/4) on a twice-yearly basis.
