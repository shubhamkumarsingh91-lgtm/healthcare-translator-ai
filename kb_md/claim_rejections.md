# Claim Rejection Library

## Eligibility Failure
Meaning:
The patient does not have active insurance coverage on the date of service.

Common Causes:
- Coverage expired
- Incorrect service date
- Wrong member ID

Fix:
- Verify coverage dates
- Confirm member eligibility
- Check payer system

---

## Invalid Subscriber ID
Meaning:
The insurance ID is missing, incorrect, or improperly formatted.

Common Causes:
- Typo in ID
- Missing field
- Incorrect format

Fix:
- Validate ID format
- Cross-check eligibility system
- Update patient records

---

## Duplicate Claim
Meaning:
The same claim has already been submitted for the same member and date.

Common Causes:
- Resubmission without checking status
- System retry errors

Fix:
- Check claim history
- Avoid duplicate submission
- Verify claim status before resubmitting

---

## Missing Provider NPI
Meaning:
The billing or rendering provider identifier is missing or invalid.

Common Causes:
- NPI not entered
- Incorrect provider ID

Fix:
- Verify provider NPI
- Ensure correct provider mapping

---

## Missing Diagnosis Code
Meaning:
The claim does not include required diagnosis information.

Fix:
- Add valid ICD diagnosis code

---

## Invalid Procedure Code
Meaning:
The procedure code is not valid or not recognized.

Fix:
- Verify CPT/HCPCS codes
- Use correct coding standards

---

## Missing Prior Authorization
Meaning:
The service required approval but none was provided.

Fix:
- Obtain authorization
- Attach authorization number

---

## Missing Charge Amount
Meaning:
A service line does not include billing amount.

Fix:
- Add correct charge amount

---

## Invalid Place of Service
Meaning:
The location code for service is incorrect.

Fix:
- Verify place of service code

