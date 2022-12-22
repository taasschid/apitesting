# Chapter 7 - Bugs

**Definition** A bug is a technical defect or malfunction in an application that can cause the application to not function properly.

**What is Bug Reporting ?**

Background

Bug Reporting is a fundamental part of any QA day to day work. Filling a proper bug report is essential to product quality. However, we currently don’t have adequate guidelines on how bug reporting should have been done. This leads to a various style that used by QA in Aplikasi Super. In addition to that, there is a different interpretation of how the fields in GitLab or Jira are being used. The aim of this document is to provide a basis (minimum requirement) that QA can follow in creating a bug report.

**Goals**

1. Maintain consistency in bug reporting within QA in Aplikasi Super, related to the fields that being used and its interpretation
2. Improve auditability
3. Support QA Engineer team in the creation of QA Dashboards that will be applied for all mission in Aplikasi Super
4. To set a reliable basis for QA in bug report creation that is easy to understand , with sufficient information to help the developers to analyze the bugs. Therefore, they can fix bugs quickly

**Summary**

All bug, whether it’s a critical, major, or minor. Documentation note are logged in Gitlab or Jira.

In general, there are 2 bug types :

1. Critical bug\
   Only production bug, which have a major impact will be treated as Critical bug ( Ex : The bug caused the server is down, or disrupt major business workflow.
2. Non Critical bug\
   Any other bug must follow the bug reporting workflow below

There are several bug status :

1. TO DO
2. IN PROCESS – BLOCKED
3. RELEASE TO STAGING
4. TESTING QA – TESTING BLOCKED
5. REOPENED
6. READY FOR PRODUCTION
7. CANCELED
8. DELIVERED TO PRODUCTION

There are 4 Resolution for Completed bug :

1. FIX
2. WON’T DO
3. DUPLICATE
4. CAN’T REPRODUCE

Bug Classification

How to decide bug severity level ?

Bug Severity Level

![](<../.gitbook/assets/image (2) (1) (1).png>)

Why Quality is important ?

Customer satisfaction and experience is a golden gate for every business. If the product is not reliable., the company needs to invest more money in fixing or replacing it and the realize that it would be best the quality was controlled from the start.

By Priority

Below are Gitlab/Jira vs Quality Team vs Product Team Priority

| Priority | Description in Gitlab/Jira                           | Quality Team Priority |
| -------- | ---------------------------------------------------- | --------------------- |
| Highest  | This problem will block progress                     | Critical              |
| High     | Serious problem that could block progress            | Major                 |
| Medium   | Has the potential to affect progress                 | Major/Minor           |
| Low      | Minor problem or easily worked around                | Minor                 |
| Lowest   | Trivial problem with little or no impact on progress | Trivial               |
|          |                                                      | Improvement           |

&#x20;****&#x20;

<figure><img src="../.gitbook/assets/BUGS PROD DEFINE.jpg" alt=""><figcaption><p><strong>Bugs Severity And Priority</strong></p></figcaption></figure>

**SEVERITY:**- Severity is effect of bug effect means- Critical, Major, Moderate , Minor and Cosmetic. Bug/Defect severity can be defined as the impact of the bug on the application.

**PRIORITY**:- Priority is about scheduling of the bug. Scheduling means P0, P1, P2, P3. Defect priority can be defined as an impact of the bug on the customers business Bug Severity, bug based on level of severity Bug Priority, bug based on level of priority

## Bugs Flow

### Bugs Development

![](../.gitbook/assets/image.png)



* **Bugs:** QA finds a bug in the development stage.
* **BE/FE:** QA will communicate the results of the bugs that have been reproduced to the developer . If bugs occur in FE, then QA will make FE tickets on Jira and will be assigned to the developer after communicating the bugs to the engineering squad lead. On the same note, if bugs occur in BE then QA will make BE tickets on Jira and assign to the developer once communicating the bugs to the engineering squad lead.
* **Create a Subtask Bugs Sprint FE JIRA:** When a bug is determined to by QA which is generally in front-end development then QA will assign the Front-end developer and create a subtask which is called _Bugs Sprint_. QA will write the description including the steps to produce. Then on the attachment section QA evidence is attached which shows how bugs were produced.
* **Assign to developer FE:** QA will assign to the FE developer
* **Create a Subtask Bugs Sprint BE JIRA:** When a bug is determined to by QA which is generally in back-end development then QA will contact the Back-end developer and create a subtask bugs which is called _Bugs Sprint_. QA will write the description including the steps to produce. Then on attachment QA will attach the evidence which shows how bugs were produced.
* **Assign to developer BE:** QA will assign to the BE developer
* **Developer:** If the bug has been fixed by the developer, the assigned developer will shift the ticket on Jira to Ready QA test.
* **Ready QA Test:** QA will work on the ticket which has been fixed by the developer concerned. When the bugs still occur then QA will shift the ticket to Todo (Reassign again to developer)
* **DONE:** If the bugs have been solved then QA will move the ticket in jira to ready to deploy and will inform to engineering squad lead so that it can be up to production
* **Ready to Deploy:** Engineering squad lead inform to tech lead for Ready to Prod

### Bugs Production

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption><p>Bugs Production</p></figcaption></figure>

1. **Bugs Production:** QA receives a bug report from users or from other divisions.
2. **Helpdesk/WhatsApp:** A bug report goes to Helpdesk or WhatsApp .
3. **Analyze:** QA will check for bugs informed by operations team. If it's not a bug, then the problem will be reported to the product team and If a bug then QA will reproduce and QA will assign severity level to the bug
4. **Reproduce QA:** QA will make step by step what happens in production, if everything is finished then QA will make the bugs in Jira
5. **Product:** The product team will receive information from QA if there are production bugs or not bugs (features are still in development stage)
6. **BE/FE:** QA will communicate the results of the bugs that have been reproduced to the developer .If bugs occur in FE, then QA will make FE tickets at Jira and will be assigned to the developer after communicating the bugs to the engineering squad lead. and then for the same BE bugs
7. **Create a Ticket on Jira FE:/BE** QA will create a FE/BE ticket on Jira
8. **Assign to developer FE/BE:** QA will assign to the FE developer
9. **Developer:** If the bug has been fixed by the developer, the assigned developer will shift the ticket in Jira to ready QA test
10. **Ready QA Test:** QA will work on the ticket which has been fixed by the developer concerned. when the bugs still occur then QA will shift the ticket to Todo (Reassign again to developer)
11. **DONE:** If the bugs have been solved then QA will move the ticket in Jira to ready to deploy and will inform to engineering squad lead so that it can be up to production
12. **Ready Deploy to Production:** Engineering squad lead inform to tech lead for Ready to Prod

\
