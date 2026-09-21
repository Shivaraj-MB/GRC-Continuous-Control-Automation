# Human-in-the-Loop (HITL) Exception Registry

A core architectural principle of this pipeline is that pure algorithmic automation introduces unacceptable governance liability in enterprise compliance. 

### The Exception Workflow
This architecture implements a strict Human-in-the-Loop (HITL) exception mechanism to allow authorized Lead Auditors to override machine-calculated risk scores:

1. **Automated Baseline:** The Python processing engine calculates the baseline Inherent and Residual risk scores based on explicit control failures extracted by the AI.
2. **Registry Query:** Before finalizing the master database, the pipeline queries a secondary `Exception_Registry.csv`.
3. **Auditor Override:** If a Lead Auditor has logged a compensating control (e.g., acknowledging an air-gapped network that a parser cannot conceptually understand), the system overrides the AI's calculated score with the auditor's governed score.
4. **Immutable Audit Trail:** The architecture preserves both the original automated result and the manually governed result. 

This ensures that the automated pipeline satisfies the strict evidentiary requirements of global cybersecurity regulations like APRA CPS 234 and DORA.