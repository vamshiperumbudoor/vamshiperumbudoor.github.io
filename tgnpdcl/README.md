# TGNPDCL — Smart Electricity Companion (Concept Demo)

An independent, responsive consumer-dashboard prototype for the Telangana electricity-billing assistance challenge.

## Preview

When GitHub Pages is enabled for the parent repository, visit:
https://vamshiperumbudoor.github.io/tgnpdcl/

## Problem addressed

Electricity bills can be difficult to interpret. Consumers need a clear view of:
- Current-cycle and historical units consumed.
- Daily peaks, low-use days and month-on-month changes.
- Itemized bill components and why totals change.
- Paid, upcoming and pending bills and payment dates.
- A transparent estimate of the next bill.
- Telugu explanations that make billing terms accessible.

## Included in this prototype

- Website / Android / iOS presentation switcher with distinct responsive device shells and navigation.
- Consumer overview with service details, sample meter reading context, monthly and daily usage charts, bill snapshot and due-date status.
- Usage history and consumption insights.
- Bill history with status filtering and payment history.
- Bill image/PDF selection and local image preview; sample bill explanation in English and Telugu.
- Charge explanations for energy, fixed/customer charges, fuel/power adjustments, duty/taxes, arrears/late fees and credits.
- Next-bill low/base/high estimate and adjustable usage-reduction scenario.
- Appliance estimator based on user-entered wattage and hours.
- Energy-saving guidance, demo service request form, FAQs and preferences.
- Responsive, keyboard-friendly controls and clear demo-data warnings.

## Important accuracy and feasibility boundaries

This page is a frontend concept using fictional sample household data. It is **not an official TGNPDCL service**, does not authenticate consumers, fetch live bills, submit real complaints, read a live meter, or collect payments. The TGNPDCL name is used to identify the challenge context; no official seal or government logo is reproduced. Obtain permission and approved brand assets before public production use.

A conventional cumulative electricity meter reports premises-level consumption, not which appliance used each unit. Appliance-wise tracking is possible only through dedicated sub-meters, smart plugs, a home energy-management system, or supported smart-meter interval data. The estimator here is explicitly a calculation from entered wattage × run time, not measured appliance telemetry.

Bill OCR/AI explanation requires a secure backend: image/PDF validation, OCR, extraction confidence, schema validation, tariff-aware calculations, LLM explanation constrained to extracted facts, and human-readable uncertainty. This prototype only previews the file locally and uses sample extracted data.

## Production integrations required

1. **Consumer identity & account:** approved TGNPDCL consumer authentication, service-number lookup, consent and account APIs.
2. **Bills & tariff engine:** official bill PDFs/structured bill data, current tariff orders and slab rules, fixed charges, duty, FSA/power-purchase adjustments, subsidies, arrears and rounding rules. Never infer current rates from sample figures.
3. **Meter & usage:** authorized meter-reading/MDMS or smart-meter interval APIs; timestamp, timezone, meter multiplier, estimated/actual reading flags and data-quality handling.
4. **OCR & Telugu AI:** secure document upload, OCR (including Telugu/English where present), structured extraction, confidence scores, charge reconciliation, Telugu translation/explanation and user correction flow.
5. **Payments:** approved payment aggregator / utility payment gateway, server-side order creation, signed webhook verification, idempotency, receipts and reconciliation. Never store card credentials.
6. **Notifications:** opt-in SMS/email/push for bill issue, due dates, abnormal usage and payment confirmation.
7. **Service & outage:** official complaint/ticket APIs, outage feed, service-area mapping, status updates and escalation rules.
8. **Security & privacy:** encryption in transit/at rest, least-privilege access, consent, retention/deletion policy, audit logs, rate limiting, secure secrets, vulnerability testing and applicable Indian data-protection requirements.

## Prediction methodology

A production forecast should project remaining-cycle units from validated interval or meter readings, compare like-for-like billing days, and apply the consumer's actual tariff schedule and bill components. Return a range and explain assumptions; do not present a forecast as the official payable amount.

## Local development

This is a static single-page HTML/CSS/JavaScript prototype. Open `index.html` in a modern browser or serve the parent repository with any static web server. No API keys or build step are required.

## Demo data

All names, service identifiers, meter values, dates, consumption, tariff category, amounts, payments, ticket IDs and predictions are illustrative. Replace them only with authorized, verified utility data in a secure production implementation.
