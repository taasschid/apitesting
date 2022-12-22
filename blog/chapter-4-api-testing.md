# Chapter 4 - API Testing

Many new modern web applications are built using web-services, micro-services, and APIs. As a Super QA, you must have knowledge and experience of testing APIs and Web Services.

**WHAT IS API TESTING?**

An API is a collection of routines, tools, protocols that are together required to build a software application. Any system software or application software consisting of multiple APIs can perform Application Programming Interface (API) testing.&#x20;

This form of testing includes interactions between various or say multiple APIs as well as interactions between APIs and application programs. This procedure mainly includes making API calls using the software and observing the system response after receiving the output.

**HOW TO THE TESTING API ?**

&#x20;       Beberapa Tools yang dapat digunakan untuk testing API secara manual terdiri dari :

1. _Postman_
2. _Swagger_
3. _Imsomnia_

Here's How to Use Postman, to test several services in different environments:



1. Open Postman and Login with a Gmail account.&#x20;

![](<../.gitbook/assets/image (1) (1) (1).png>)

2\. Set the environment and collection&#x20;

![](<../.gitbook/assets/image (6).png>)

**3. Check the folder where the API is to be tested:**

Example of API Login&#x20;

a. Method: POST \
b. Input Environment Test, example: \{{DEV\}}\
c. Verify or Input Endpoint Login : /api/v3/auth/login\
d. Input a request body and select JSON

```
 {

   "username": "masrul",

   "password" : "123456"

 }    
```

![Input a Request Body](<../.gitbook/assets/image (7).png>)

e. Setting Authorization\
****Select Type : Bearer Token

Input Token : \{{access\_token\}}

![Setting Authorization](<../.gitbook/assets/image (9) (1).png>)



f. Click “SEND” button

**Result :**

The response must be 200 OK. It means that the request has been processed successfully.

![](<../.gitbook/assets/image (11) (1).png>)

Each test consists of a test action. These are individual actions that need to be tested per API test flow. For each API request, the test needs to perform the following actions:

**​​1. Verify correct HTTP status code** \
Example : creating a resource should return 201 CREATED and unpermitted requests should return 403 FORBIDDEN, etc. \
**2. Verify response payload** \
Check valid JSON body and correct field names, types, and values — including in error responses. \
**3. Verify response headers** \
HTTP server headers have implications on both security and performance. \
**4. Verify correct application state** \
This is optional and applies mainly to manual testing, or when a UI or another interface can be easily inspected. \
**5. Verify basic performance sanity** \
If an operation was completed successfully but took an unreasonable amount of time, the test fails.

Each test consists of a test action. These are individual actions that need to be tested per API test flow. For each API request, the test needs to perform the following actions:

The following Super QA test cases are included in the following general test scenario groups:

a. Basic Positive Test \
b. Extended positive test with optional parameters\
c. Negative test with valid input \
d. Negative test with invalid input \
e. Destructive testing \
f. Security, authorization, and permission tests (which are out of the scope of this post)

Basic Positive Test:&#x20;

| **Test Scenario Category** | **Test Action Category**                                                                                                                                                                                                                                                                                                                                                                      | **Test Action Description**                                                                                                                                                                                                                                          |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Basic positive tests       | Validate Status Code                                                                                                                                                                                                                                                                                                                                                                          | <p>1. All requests should return 2XX HTTP status code</p><p>2. Returned status code is according to spec:</p><p>– 200 OK for GET requests</p><p>– 201 for POST or PUT requests creating a new resource</p><p>– 200, 202, or 204 for a DELETE operation and so on</p> |
| Validate Payload           | <p>1. Response is a well-formed JSON object</p><p>2. Response structure is according to data model (schema validation: field names and field types are as expected, including nested objects; field values are as expected; non-nullable fields are not null, etc.)</p>                                                                                                                       |                                                                                                                                                                                                                                                                      |
| Validate State             | <p>1. For GET requests, verify there is NO STATE CHANGE in the system (idempotence)</p><p>2. For POST, DELETE, PATCH, PUT operations</p><p>– Ensure action has been performed correctly in the system by:</p><p>– Performing appropriate GET request and inspecting response</p><p>– Refreshing the UI in the web application and verifying new state (only applicable to manual testing)</p> |                                                                                                                                                                                                                                                                      |



| Basic positive tests | Validate Header                                                                                          | <p>Verify that HTTP headers are as expected, including content-type, connection, cache-control, expires,</p><p>access-control-allow-origin, keep-alive, HSTS, and other standard header fields – according to spec.</p><p>Verify that information is NOT leaked via headers (e.g. X-Powered-By header is not sent to user).</p> |
| -------------------- | -------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Performance Sanity   | Response is received in a timely manner (within reasonable expected time) — as defined in the test plan. |                                                                                                                                                                                                                                                                                                                                 |

**2. Here's an example: Positive + Optional Parameter** Execute API call with valid required parameters and valid optional parameters

Run the same test in #1, this time including the endpoint's optional parameters _(e.g., filter, sort, limit, skip, etc.)_

__

| **Test Scenario Category**    | **Test Action Category**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | **Test Action Description** |
| ----------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------- |
| Positive + Opsional Parameter | Validate Status Code                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | As in #1                    |
| Validate Payload              | <p>Verify response structure and content as in #1.  </p><p>In addition, check the following parameters:</p><p>– filter: ensure the response is filtered on the specified value.</p><p>– sort: specify field on which to sort, test ascending and descending options.</p><p>Ensure the response is sorted according to selected field and sort direction.</p><p>– skip: ensure the specified number of results from the start of the dataset is skipped</p><p>– limit: ensure dataset size is bounded by specified limit.</p><p>– limit + skip: Test pagination</p><p>Check combinations of all optional fields (fields + sort + limit + skip) and verify expected response.  </p> |                             |
| Validate Header               | As in #1                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |                             |
| Performance Sanity            | As in #1                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |                             |



_**3.** _ **Here's an example: Negative testing – valid input** Execute API calls with valid input that attempts illegal operations. i.e.:

– Trying to create a resource with a name that already exists (ex : user configuration with the same name)

– Trying to delete a resource that doesn't exist (ex: user configuration with no such ID)

– Trying to update a resource with illegal valid data (ex: rename a configuration to an existing name)

– Tried illegal operations (ex : delete a user configuration without permission.)\
–  Etc

\


| **Test Scenario Category** | **Test Action Category** | **Test Action Description**                                                                                                                                                                                                                                                                                                                                        |
| -------------------------- | ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
|                            | Validate Status Code     | <p>1. Verify that an erroneous HTTP status code is sent (NOT 2XX)</p><p>2. Verify that the HTTP status code is in accordance with error case as defined in spec</p>                                                                                                                                                                                                |
|                            | Validate Payload         | <p>1. Verify that error response is received</p><p>2. Verify that error format is according to spec. e.g., error is a valid JSON object or a plain string (as defined in spec)</p><p>3. Verify that there is a clear, descriptive error message/description field</p><p>4. Verify error description is correct for this error case and in accordance with spec</p> |
|                            | Validate Header          | As in #1                                                                                                                                                                                                                                                                                                                                                           |
|                            | Performance Sanity       | Ensure error is received in a timely manner (within reasonable expected time)                                                                                                                                                                                                                                                                                      |

**4. Here's an example: Negative testing – Invalid input** Execute API calls with Invalid input :

– Missing or invalid authorization token

– Missing required parameters

– Invalid value for endpoint parameters, e.g.:

– Invalid UUID in path or query parameters

– Payload with invalid model (violates schema)

– Payload with incomplete models (missing fields or required nested entities)

– Invalid values ​​in nested entity fields

– Invalid values ​​in HTTP headers

– Unsupported methods for endpoints



| **Test Scenario Category**       | **Test Action Category** | **Test Action Description** |
| -------------------------------- | ------------------------ | --------------------------- |
| Negative testing – Invalid input | Validate Status Code     | As in #1                    |
| Validate Payload                 | As in #1                 |                             |
| Validate Header                  | As in #1                 |                             |
| Performance Sanity               | As in #1                 |                             |



1. Berikut Contoh : Destructive testing

Sengaja mencoba untuk menggagalkan API untuk memeriksa kekokohannya:

1. Wrong content-type in payload
2. Content with wrong structure
3. Overflow parameter values. ex:

* Mencoba untuk create a user configuration with a title longer than 200 characters
* Mencoba untuk  GET a user with invalid UUID

&#x20;            which is 1000 characters long

* Overflow payload – huge JSON in request body

1. Boundary value testing
2. Empty payloads
3. Empty sub-objects in payload
4. Illegal characters in parameters or payload
5. Using incorrect HTTP headers (e.g. Content-Type)
6. Small concurrency tests – concurrent API calls that write to the same resources (DELETE + PATCH, etc.)
7. Other exploratory testing



| **Test Scenario Category**       | **Test Action Category** | **Test Action Description** |
| -------------------------------- | ------------------------ | --------------------------- |
| Negative testing – Invalid input | Validate Status Code     | As in #1                    |
| Validate Payload                 | As in #1                 |                             |
| Validate Header                  | As in #1                 |                             |
| Performance Sanity               | As in #1                 |                             |

**Test case** derived from the table above should cover different test streams according to their needs, resources, and priorities.\
