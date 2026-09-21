# GRC-Continuous-Control-Automation

Author: Shivaraj M.B | Senior Vendor Risk & GRC Leader

IP Notice: This repository contains the architectural blueprint, data methodology, and dashboard visualizations for a proprietary Third-Party Risk Management (TPRM) automation pipeline. To protect intellectual property, the core Python ETL scripts, GCP Document AI configurations, and proprietary algorithmic risk-scoring engines are withheld.

1. The Enterprise Vulnerability (The Problem)
Conventional Governance, Risk, and Compliance (GRC) frameworks rely on manual, point-in-time vendor risk assessments. Highly restricted data is governed by static artifacts (SOC 2, ISO 27001 certificates) that trap critical risk telemetry in unstructured PDF formats. This manual parsing creates a massive operational bottleneck, delays critical vendor onboarding, and obscures real-time threat visibility.

2. The Architectural Solution (The How)
I architected a 4-tier, hybrid Continuous Control Monitoring (CCM) pipeline that bridges traditional GRC with modern automation. The system utilizes a synthetic dataset representing $90M+ in vendor portfolios to demonstrate end-to-end automation.
  * Tier 1: Intelligent Document Processing (IDP): Utilizes Google Cloud Document AI to autonomously map spatial coordinates and extract unstructured compliance        artifacts into key-value pairs.
  * Tier 2: Python / Pandas Risk Engine: A programmatic ETL layer that cleanses OCR artifacts, normalizes schema drift, and algorithmically calculates baseline       Inherent and Residual Risk scores.
  * Tier 3: Human-in-the-Loop (HITL) Governance: A mandatory architectural checkpoint. Before data enters the master database, it queries a secondary exception registry. Lead Auditors can inject compensating controls to legally override machine-calculated scores, maintaining a strict audit trail.
  * Tier 4: Idempotent Persistence & Visualization: An upsert engine ensures clean database processing without duplicate records, feeding a dynamic Microsoft         Power BI decision-support interface.
  
   <img width="1379" height="796" alt="image" src="https://github.com/user-attachments/assets/04215636-0648-4abf-876b-3d92e16eb811" />

  

3. Executive Impact (The Outcomes)
   The implementation of this architecture successfully transitions TPRM from a "system of record" to a proactive assurance system.
   * Decoupled Administration: Eliminates manual data entry, allowing risk analysts to focus exclusively on critical remediation and high-value threat intelligence.
   * Regulatory Defensibility: The HITL exception registry ensures the automated pipeline satisfies the strict evidentiary requirements of global cybersecurity regulations like APRA CPS 234, DORA, and ISO 27001.
   * Executive Visibility: Consolidates unstructured evidence into a centralized Power BI dashboard, enabling C-suite stakeholders to monitor continuous year-over-year remediation trends and domain-specific vulnerabilities (InfoSec, BCP/DR, Compliance).
   
     <img width="1291" height="716" alt="image" src="https://github.com/user-attachments/assets/a9185f27-062e-484c-835c-e289b9cab26c" />
                                           Figure 4.2: TPRM Executive Dashboard

     ...

