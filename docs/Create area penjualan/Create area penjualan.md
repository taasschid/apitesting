---
sidebar_position: 1
---

# Create Area Penjualan

| No  | Field Name | Mandatory | Optional | Input                                                                           | Alert Information (Actual)                | Alert Information (Expected)                                                               | Details | Status code |
| --- | ---------- | --------- | -------- | ------------------------------------------------------------------------------- | ----------------------------------------- | ------------------------------------------------------------------------------------------ | ------- | ----------- |
| 1   | city       | TRUE      |          | 1. city: ""<br/>2. city: city yang sudah ada atau sama<br/>3. city: "Situbond@" | validation.required<br/>validation.unique | 1. city cannot be empty<br/>2. city already exist<br/>3. city cannot use special character |         | 400         |
| 2   | status     |           | TRUE     | 1. role_id: ""<br/>2. role_id: "a"<br/>3. role_id: "100"                        | validation.required<br/>                  | 1. status cannot be empty<br/>2. status must be number<br/>3. status not found             |         | 400         |