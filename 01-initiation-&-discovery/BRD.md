#Business Requirements Document (BRD)
**Project Name:** Omnichannel "Click and collect" (BOPIS) Overhaul
**Client:** ThreadNet Apparel
**Document Owner:** Anugi Lihansa Laknavi Pathirage, Lead Business Analyst
**Date:** June 2026

---

## 1. Executive Summary
ThreadNet Apparel is initiating a digital transformation project to overhaul its "Buy Online, Pick up In Store" (BOPIS) architecture. The objective is to implement real time inventory synchronisation across the E commerce platform, the central Enterprise Resource Planning (ERP) systems, and local physcial store Point of Sale (POS) networks to ensure a seamless, frictionless customer fulfillment experience. 

## 2. Problem Statement
ThreadNet's current omnichannel fulfillment architecture relies on disconnected legacy systems. Becasue the E-commerce platform only synchronises inventory data with the central ERP via a 12-hour batch processing cycle, physical store POS systems frequently lack real-time visibility of online reservations.

As a result, walk-in customers frequently purchase items that have already been reserved online. Currently, **18% of all BOPIS orders are canceled post purchase due to inventory stockouts at the store level**, leading to estimated **£450,000 annual loss in revenue** and severe damage to brand loyalty.

## 3. Business Objectives (KPIs)
The success of this new system will be measured against the following Key Performance Indicators:
* **Reduce BOPIS Cancellation Rate:** Decrease from 18% to < 3% within 3 months of launch.
* **Decrease In-Store Wait Time:** Reduce the average customer collection wait time from 8 minutes to under 2 minutes.
* **Increase Inventory Accuracy:** Achieve 99.9% real-time inventory parity between the E-commerce storefront and physical store POS nodes.

## 4. Discovery Findings & Operational Constraints
Following an initial period of elicitation (store floor observation and technical architecture review), the following constraints were discovered:
* **The "Secondary Tablet" Bottleneck:** Store staff currently do not receive BOPIS alerts on their primary POS registers. They must manually cross-reference incoming web orders on a secondary, slow-performing tablet, adding an average of 4 minutes to the fulfillment process.
* **API Rate Limitations:** The current E-commerce provider restricts API calls to a maximum of 1,000 requests per minute, which will dictate the technical design of the real-time synchronization middleware.

## 5. Stakeholder Register
* **E-commerce Director (Project Sponsor):** Primary focus on online conversion rates and reducing post-purchase cancellations.
* **Store Operations Manager:** Primary focus on reducing staff manual workload and mitigating in-store customer complaints.
* **Lead Solutions Architect:** Primary focus on database security, API integrations, and maintaining system uptime.

## 6. Scope Definition
* **In-Scope:** * Implementation of real-time inventory API middleware connecting the ERP and E-commerce platform.
    * Upgrading local POS software to support immediate push notifications for incoming BOPIS orders.
    * Designing a standardized physical staging workflow for retail staff.
* **Out-of-Scope:** * Redesigning the customer-facing website UX/UI.
    * Changing the existing payment gateway provider.
