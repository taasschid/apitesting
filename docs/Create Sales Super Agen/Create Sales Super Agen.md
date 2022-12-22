---
sidebar_position: 1
---

# Create Sales Super Agen
| No  | Field Name  | Mandatory | Optional | Input                                | Alert Information (Actual)                                                      | Alert Information (Expected)                                     | Details | Status code |
| --- | ----------- | --------- | -------- | ------------------------------------ | ------------------------------------------------------------------------------- | ---------------------------------------------------------------- | ------- | ----------- |
| 1   | type        | TRUE      |          | 1. type: ""<br/>2. type: "Holid@y"   | validation.required                                                             | 1. type cannot be empty<br/>2. type cannot use special character |         | 400         |
| 2   | date        | TRUE      |          | 1. date: ""<br/>2. date: "2021-08-00 | validation.required<br/>Tidak ada validasi jika tanggal salah (ex: 2022, 08,00) | 1. date cannot be empty<br/>2. invalid date                      |         | 400         |
| 3   | description | TRUE      |          | 1. description: ""                   | validation.required<br/>                                                        | 1. description cannot be empty                                   |         | 400         |