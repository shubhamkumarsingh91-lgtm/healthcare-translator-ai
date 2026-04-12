# EDI 837 Structure (High-Level)

## Overview

EDI 837 is structured as a hierarchical claim format used to transmit healthcare billing data.

---

## Flow

Header → Subscriber → Provider → Claim → Service Lines

---

## Key Sections

### Header
Contains:
- Transaction metadata
- Sender/receiver info

---

### Subscriber Information
Includes:
- Subscriber ID
- Coverage details
- Patient relationship

---

### Provider Information
Includes:
- Billing provider
- Rendering provider
- NPI identifiers

---

### Claim Information
Includes:
- Claim ID
- Diagnosis codes
- Dates of service

---

### Service Lines
Includes:
- Procedure codes
- Charge amounts
- Units

---

## Validation Points

- Subscriber eligibility
- Provider validity
- Code correctness
- Data completeness

---

## Common Failure Points

- Missing subscriber data
- Invalid provider identifiers
- Incorrect codes
- Duplicate submissions
