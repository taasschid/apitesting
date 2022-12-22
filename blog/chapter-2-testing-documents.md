# Chapter 2 - Testing Documents

### **BACKGROUND**

The basic idea is to include regression testing (partially) during  the feature testing period, this is the tactical preparation  that is relevant to the faster release cycle when the regression period is being shortened. To start we can use the rule of thumb: “Check the blast radius of the changes”.

**WHAT IS TEST PLAN DOCUMENT ?**

**Test plan document** is a document which contains the plan for all the testing activities to be done to deliver a quality product. Test Plan document is derived from the Product Description, SRS, or Use case document for all future activities of the project, it’s usually prepared by Test Lead or Test Manager.

**Test plans** acts as a blueprint or instruction manual of how and what you will test for a product release or sprint. It defines the scope, schedule, approach, and resources for your testing efforts.

**Test plans** includes the kind of information that everyone needs throughout the product's journey to do their job efficiently.

**WHAT IS TEST STRATEGY ?**

Test Strategy are high-level documents and are usually developed by the PM (Project Manager). This type of documentation captures our approach to testing the product and achieving the goals. And usually comes from BRD or PRD. Documents such as the Test Strategy doc are project-base documents which can be modified according to the project domain and requirements.

**WHAT IS TEST SCENARIO ?**

Test Scenario means to give an idea of what we have to test (test). Test scenarios are like high-level test cases.

**WHAT IS TEST CASES ?**

Test cases are a collection of steps that can be executed positively and negatively from a test scenario that has a set of pre-conditions, test data (test data), expected results, post-conditions, and actual results. results).

**HOW TO WRITE EASY TEST CASES ?**

Typically, QA engineers use Excel sheets to manually write test cases. In addition, you can use test management tools, such as TestRail, xray, Test Link, Qtest to create and maintain test cases.

![Contoh manual test case  untuk Internal Tools (Dashboard) ](<../.gitbook/assets/image (1) (2).png>)

In making the test case at Aplikasi Super, the QA Analyst is required to fill in some data in the Header on the Excel Sheet::

1\.  Project/Application Name

2\. Testing Date

3\. Tester Name / Designation

4\. Environment : Dev / Staging / Production

Then the QA Analyst performs some data entry to create a test case, which consists of:

1. Scenario ID
2. Testcase ID
3. Jira ID /Gitlab ID
4. Testcase Description
5. STP
6. Test Priority : **Critical, High, Medium, Low**
7. Type Of Testing : **Positive , Negative**
8. Expected Result
9. Actual Result
10. Test Result : **Passed or Failed**
11. Test Execution Date : **DD/MM/YYYY**
12. Defect ID (From bug logging Tool, If applicable)
13. Reference
14. Remark

**FLOW PROCESS**

1. Create Test Case
2. Create new test cases
3. Update test cases

2\. Test case Review

1. Share document testcase
2. Review with pear team
3. Review with PM/Developer

3\. Update Test Case

1. Add new test case
2. Update test case
3. Priority test case

4\. Run Test Case

1. Run the new test case
2. Run update test case

**WHAT TEST CASES SHOULD BE EXECUTED DURING THE FEATURE TESTING PERIOD?**

QA should execute Test cases for the new feature  and Test Cases regression related to the new feature. Hopefully, with this kind of execution QA can create a better timeline for Feature Testing and reduce testing in Staging Testing Period

&#x20;_(QA can do E2E Test to ensure new feature run smooth or smoke test or exploratory testing)_

**WHAT IS TEST BED ?**

**Test Bed** is the environment configured for testing. The test bed consists of hardware, software, network configuration, the application being tested, and other related software.

**WHAT IS TEST ENVIRONMENT?**

**Test Environment** is a combination of hardware and software which is where the Tester Team conducts testing.

Example :

Application Type: Web Application

OS: Ubuntu

Web Server: LINUX

Web Page Design: React JS

Client-Side Validation: JavaScript

Server-Side Scripting: Node JS

Database: My SQL

Browser: IE/Firefox/Chrome

**WHAT IS TEST DATA ?**

&#x20;       **Test data** is the data used by the tester to run test cases (test cases). When running test cases, the tester needs to enter some input data.&#x20;

To do this, the tester prepares test data (test data). And can be prepared manually and also by using tools

**WHAT IS TEST CLOSURE?**

Test Closure is a record that is prepared before the test team officially completes the testing process.&#x20;

This record contains the total number of test cases, the total number of testcases executed, the total number of defects found, the total number of defects fixed, the total number of unfixed bugs, the total number of no rejected bugs, etc.

**WHAT IS REQUIREMENT TRACEABILITY MATRIX?**

RTM is a table that contains a list of Requirements, attributes that vary for each Requirement, and the status of the Requirement to trace the Requirement to the Tester needed to ensure or verify whether all Requirements have been met.&#x20;

The parameters included in the Requirement Traceability Matrix are

1. Requirements ID
2. Requirement Type dan Description
3. Completed Test Cases Status

Example

| **Req.No**   | **Req. Description** | **Testcase ID**                                             | **Status**                                                                                                       |
| ------------ | -------------------- | ----------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| 112          | Login to the Apps    | TC-001, TC-002,TC-003                                       | TC-001 : PASS TC-002 : PASS                                                                                      |
| 113          | Search Product       | <p>TC-004, TC-005,</p><p>TC-006, TC-007,</p>                | <p> TC-004 PASS</p><p> TC-005 FAIL</p><p> TC-006 PASS</p><p> TC-007 NO RUN</p>                                   |
| 114          | Create Order         | <p>TC-008, TC-009,</p><p>TC-010,TC-011, TC-012 , TC-013</p> | <p>TC-008 PASS</p><p>TC-009 PASS</p><p>TC-010 PASS</p><p>TC-011 FAIL</p><p>TC-012 NO RUN</p><p>TC-013 NO RUN</p> |

**HOW TO CREATE RTM ?**

&#x20;     **Create RTM** Based on the Business Requirement Document (BRD) and Technical Requirement Document (TRD), the Tester started writing Test Cases.

**STEP 1 : Contoh sampel Uji Kasus (Testcase)**

“Verify Login, When the mobile number and PIN are entered correctly. It should state “Successfully Login”

| <p><strong>Testcase</strong></p><p><strong>ID</strong></p> | <p><strong>Testcase</strong></p><p><strong>Desc</strong></p> | **Test Steps**                                                                                                      | **Test Data**                            | **Expected Result** |
| ---------------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------- | ---------------------------------------- | ------------------- |
| 1                                                          | Verify Login                                                 | <ol><li>Open Apps : Aplikasi Super</li><li>Input Phone Number</li><li>Tap “Masuk”</li><li>Input Nomor PIN</li></ol> | <p>HP:081994796687</p><p>PIN :668712</p> | Login Succesful     |

STEP 2 :Identification of Technical Requirements related to Testcases being verified. For our test case, the Technical Requirement is T35 which is verified.

**Login**

T33  Phone Number must not be blank

T34  PIN must not be blank

T35  If Phone number and PIN are valid Login => T35 is the TR that verifies&#x20;

**Successful Login**

STEP 3 : Note This TR in the Testcase

| <p>TESTCASE</p><p>ID</p> | TR # | <p>Testcase</p><p>Desc</p> | **Test Steps**                                                                                                      | **Test Data**                            | **Expected Result** |
| ------------------------ | ---- | -------------------------- | ------------------------------------------------------------------------------------------------------------------- | ---------------------------------------- | ------------------- |
| 1                        | T35  | Verify Login               | <ol><li>Open Apps : Aplikasi Super</li><li>Input Phone Number</li><li>Tap “Masuk”</li><li>Input Nomor PIN</li></ol> | <p>HP:081994796687</p><p>PIN :668712</p> | Login Successful    |

STEP 4 : Identify the BRD for which TR (TR-35) is defined

| BR # | Module Name                   | Applicable Role               | Desc                                                                                                                                                                                                                         |
| ---- | ----------------------------- | ----------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|      | <p>Login dan</p><p>Logout</p> | <p>Manager</p><p>Customer</p> | <p><strong>Cust</strong> : a customer can login using the login page</p><p><strong>Mgr</strong> : a manager can login using the login page of costumer.</p><p>Post Login homepage will show different link based on role</p> |

STEP 5 : Note This BR in the Testcase

| <p>TESTCASE</p><p>ID</p> | BR # | TR # | <p><strong>Testcase</strong></p><p><strong>Desc</strong></p> | **Test Steps**                                                                                                      | **Test Data**                            | **Expected Result** |
| ------------------------ | ---- | ---- | ------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------- | ---------------------------------------- | ------------------- |
| 1                        | B1   | T35  | Verify Login                                                 | <ol><li>Open Apps : Aplikasi Super</li><li>Input Phone Number</li><li>Tap “Masuk”</li><li>Input Nomor PIN</li></ol> | <p>HP:081994796687</p><p>PIN :668712</p> | Login Succesful     |

STEP 6 : Follow the instructions above to create Test cases. Then Split the First 3 Columns of your Test Suite. RTM in testing is Ready!

| **BR #** | **TR #** | **Testcase ID** |
| -------- | -------- | --------------- |
| B1       | T35      | 1               |
| B2       | T36      | 2               |
| B3       | T37      | 3               |
| B4       | T38      | 4               |

Advantages of using RTM:&#x20;

1. Confirmation of Test Coverage (Coverage Test) 100%
2. Highlights of Missing Requirements and Document
3. To show overall defect or execution status with a focus on business requirements
4. Assist in analysis and impact on QA work in connection with or rework test cases.

\
\
\
