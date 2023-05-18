---
stoplight-id: 7ns2saryqwsyz
---

# Introduction

Verituity API allows creating of user profiles (payees) and payments (claims) using secure REST service.

Verituity supports zero-trust multi-tenant architecture. Every tenant has its own realm which is further partitoned in separate business units.
Each business unit is identified by unique Program ID - created during onboarding.

Profiles can be related to business or individuals and can also be linked in a parent(guardian) to many dependents relationship with age verification. This is not currently exposed via this API.

Users are created with typical attributes like first name, middle name, last name, email and optional address elements.

A mandatory Unique clientUserId attribute is required to ensure proper identification of users. 
Customer can select the value of the attribute - it can be account number, email address or any other immutable value that will not change with time.

Verituity also offers different payee verification options - one of them exposed in this API is Relationship Verification (RV).

RV attributes are optional name / value attributes that can created during user creation and validated on the user portal by payee. 

Example of attributes: a policy number or last four digits of driver's license - they can be provided during creation of the user and configured via flexible rules during user registration.

RV checking can be enabled per realm and the values are specific for each payee. Number of RV attributes is variable - from 0 to N.


