# Chapter 6 - Flow QA Testing

Divided into 2 QA flows in conducting tests in Environment Staging to Up to Production:

**A. Squad CORE**

![](<../.gitbook/assets/image (3).png>)

**Process QA:**

1. **Sprint Grooming** is carried out by the Product Team, Tech Lead, Engineering Manager and QA Lead to identify sprint issues that will be developed and tested. **Test Plan** is carried out by the QA Manager / QA Lead / QA in planning the testing strategy stages and attaching several PRD / TRD and Testcase documents.
2. **Sprint Planning** is carried out by the Product Team, BE/FE Developers, Tech Leads, Engineering Managers and QA Leads in discussing the work to be carried out during the sprint.&#x20;
3. **Test Cases** are a QA tool to conduct test tests based on issues that run in the sprint, both related to improvements or new features that will be developed.
4. **QA Testing** is the realm of QA in taking tickets that have been completed by the Developer to do a Test Test based on the testcase that was created during development. \*\*\*\*\
   **Notes:**\
   \-> Testing process starts from Env _DEV_ after Passed will Up to Env _Demo_ and _Staging_, after the status is Passed then from Staging then the codes are deployed to _Production_\
   \-> When 1 issue in multiple test cases has a status "Failed" then the issue will be moved from QA Testing to _To Do._\
   If 1 Issue in all testcases get status "Passed" then the ticket will be shifted from QA Testing to\
   _Ready To Prod_
5. **Smoke Test** is carried out by QA in carrying out only the most important tests (main function) and or critical functions in outline before the detailed regression is run.&#x20;
6. **The Deployment Plan** will be prepared by the Engineering Manager regarding any features that are improved or new features that will be raised to production according to the agreed release schedule.
7. **Retrospective**, will discuss feed issues related to what has been resolved or not, and discuss the backlog of QA testing including solutions for needs to improve so as to improve the development of relations between QA teams without any judgments.

**b. Squad VANGUARD**

![](<../.gitbook/assets/image (5) (1).png>)

1. **Sprint Grooming** is carried out by the Product Team, Tech Lead, Engineering Manager and QA Lead to identify sprint issues that will be developed and tested at Vanguard.
2. **The Test Plan** is carried out by the QA Manager / QA Lead / QA in planning the testing strategy stages and attaching several PRD / TRD and Testcase documents. Sprint Planning is carried out by the Product Team, BE/FE Developers, Tech Leads, Engineering Managers and QA Leads in discussing the work to be carried out during the sprint.
3. **Test Cases** are a QA tool to conduct test tests based on issues that run in the sprint, both related to improvements or new features that will be developed.
4. **QA Testing** is the realm of QA in taking tickets that have been completed by the Developer to do a Test Test based on the testcase that was created during development. When 1 issue in several testcases gets the “Failed” status, the Issue will be moved from QA Testing to To Do. If 1 Issue in all testcases gets the status "Passed" then the ticket will be shifted from QA Testing to Ready To Prod
5. **Smoke Test** is carried out by QA in doing only the most important test (main function) or critical function in outline before the detailed regression is executed. Smoke tests are also carried out to ensure the application does not cause any problems when it goes into production.
6. **Deployment Plan** will be prepared by the Engineering Manager regarding any features that are improved or new features that will be raised to production according to the agreed release schedule.
7. **Retrospective,** will discuss feed issues related to what has been resolved or not, and discuss the backlog of QA testing including solutions for needs to improve so as to improve the development of relations between QA teams without any judgments.
