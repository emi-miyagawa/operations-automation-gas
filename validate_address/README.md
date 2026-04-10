# Address Validation (GAS)

## Overview
This script validates address data entered by customers in a landing page form by comparing it against Japan Post address reference data.

The purpose is to detect likely address issues before the data moves into downstream operations such as shipment, mailing, or manual follow-up.

---

## Problem
Customer-entered address data often contains:
- missing or incomplete address components
- formatting inconsistencies
- entries that do not match expected postal address patterns

If such data is passed downstream as-is, it can lead to returned mail, manual correction work, and avoidable operational loss.

---

## Approach
- Compared form-entered address data with Japan Post reference data
- Flagged likely mismatches and incomplete entries
- Focused on detecting obvious operational risks before processing

---

## Design Decision
The goal was not to reject every imperfect entry, but to identify cases with a high likelihood of delivery failure or rework.

I chose a practical validation approach that supports operations rather than enforcing unrealistic data perfection.

---

## Trade-off
- Not every edge case can be perfectly validated
- However, pre-checking obvious mismatches significantly reduces downstream friction

---

## Result
- Reduced avoidable returns and manual correction effort
- Improved data quality before downstream processing
- Helped create a more stable operational flow

---

## Positioning
This is an example of designing data validation under real operational constraints, using external reference data to reduce operational risk from customer-entered information.
