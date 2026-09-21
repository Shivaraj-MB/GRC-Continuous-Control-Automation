# TPRM Automated Data Schema (Abstract)

This document outlines the standardized data schema used to normalize unstructured compliance artifacts (SOC 2, ISO 27001 reports) after extraction via GCP Document AI. 

To maintain compliance and protect proprietary logic, the raw ETL scripts are withheld. The pipeline successfully maps the following critical dimensions into the master database:

* **Vendor Identification:** Vendor ID, Vendor Name, Assessment Year.
* **Risk Parameters:** Vendor Tier (1-3), Data Classification (Public, Confidential, Restricted).
* **Control Metrics:** Total Controls Evaluated, Total Controls Passed, Critical Failures, High Failures.
* **Algorithmic Scoring:** Calculated Inherent Risk Score, Calculated Residual Risk Score.
* **Domain Gaps:** InfoSec, BCP & DR, Compliance, Performance SLAs.
* **Final Posture:** Clean, Conditional Approval, Critical Failure, Pending Review.

This structured schema allows for idempotent database upserts, preventing duplicate records during recurring vendor assessments.