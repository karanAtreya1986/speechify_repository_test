# General QA Questions
**Question 1:** What are the key responsibilities of a QA Engineer in the software development lifecycle?
**Answer 1:** <!-- <Write your answer here> -->
The main responsibility is ensure the quality of the software.
Find bugs, prevent bugs, ensures software works as per customer requirements.

**Question 2:** What do you think is more important for QA: finding bugs or preventing bugs? Why?
**Answer 2:** <!-- <Write your answer here> -->
Both are important, finding bugs so that customer does not get the bug in his or her environment.
Preventing bugs, because it can be a big cost to the company at a later point in time.

**Question 3:** You find a critical bug on the day of a release. What steps would you take?
**Answer 3:** <!-- <Write your answer here> -->
Validate the bug (confirm it’s real and critical).
Communicate immediately to release manager/stakeholders with impact and risks.
Retrospective afterward to prevent recurrence.
Update test cases to include testing for this scenario in next release.

**Question 4:** What would you do if you found a requirement that was unclear or incomplete during testing?
**Answer 4:** <!-- <Write your answer here> -->
Reach out to the BA/product owner/stakeholder for clarification.
Document the clarification so the whole team has a single source of truth.
Perform exploratory testing of application to understand how it works.

**Question 5:** How would you manage testing if the development team delivers a feature at the last minute?
**Answer 5:** <!-- <Write your answer here> -->
Test the critical features of that particular feature.
Then do a regression testing around that module.

**Question 6:** What is exploratory testing, and when is it most useful?
**Answer 6:** <!-- <Write your answer here> -->
When we dont have requirements or its unclear, we can work with application to see how much we can understand.

**Question 7:** What is regression testing, and how do you decide what areas to cover during regression testing?
**Answer 7:** <!-- <Write your answer here> -->
Regression testing is done before release. We need to ensure all positive cases for all functionalities developed earlier should be tested once before releasing the software.

**Question 8:** What is a test case, and what details should a good test case include?
**Answer 8:** <!-- <Write your answer here> -->
Test case details the step to run a particular scenario.
It should include test id, pre-requisite, steps, expected result, actual result, requirement id, screenshot location, name of tester.

**Question 9:** Have you ever worked with tools for managing test documentation? Which ones, and how did you use them?
**Answer 9:** <!-- <Write your answer here> -->
HPALM, Jira, Mantis - some of the tools, I have used.
We used them to maintain the requirements, manage test cases, and then tracking defects.

**Question 10:** What should be included in a QA test report?
**Answer 10:** <!-- <Write your answer here> -->
Execution summary mentioning the environment name where it was tested.
Type of testing - functional or regression or smoke etc.
Number of defects, fixed, still pending.
Number of test cases run, in progress, not run.
Expected timelines to complete the test case.

**Question 11:** How do you handle situations where a developer disagrees with a defect you've reported?
**Answer 11:** <!-- <Write your answer here> -->
Talk to the developer and discusss the defect.
Talk to the other testers in the team to understand their viewpoint.
Have a call with development and testing team to come at a conclusion.
If still not solved, go to product owner or business analyst.

**Question 12:** How do you ensure that stakeholders understand the risk of releasing software with open defects?
**Answer 12:** <!-- <Write your answer here> -->
Inform stakeholders on the defects, what are their consequences, what are the workarounds if the defect occurs in production environment.

**Question 13:** How do you decide the severity and priority of a defect?
**Answer 13:** <!-- <Write your answer here> -->
Severity - how badly the defect is affecting the application, whether any work around is there or not.
Priority - based on the severity assign priority on how soon it should be fixed.

**Question 14:** You are tasked with providing a report of testing progress for a release. What would your report include?
**Answer 14:** <!-- <Write your answer here> -->
Functionalities tested.
Type of testing performed till now - regression, smoke etc.
Total number of test cases.
Completed test case count.
In progress test case count.
Not run test case count.
Defects total count.
Fixed defects count.
Not fixed defects count.
Blockers if any should be mentioned.
How much more time it will take for one round to complete excluding bugs.


# API Testing Questions

**Question 15:** What is the difference between REST APIs and SOAP APIs?
**Answer 15:** <!-- <Write your answer here> -->
REST API -
Uses HTTP methods (GET, POST, PUT, DELETE).
Lightweight, flexible, faster.
Data usually in JSON, XML (but less).
Stateless - does not remember anything. So secure.
SOAP API
Protocol with strict standards.
Always uses XML.
Heavier, slower.

**Question 16:** What is the significance of HTTP methods like GET, POST, PUT, and DELETE in REST APIs?
**Answer 16:** <!-- <Write your answer here> -->
These are basically the crud operations.
Get is for getting records from database.
Post is for creating records in database.
Put is for updating the records. Put can work as post if the record does not exist. Entire body has to be passed in put call.
Delete - for deleting records from database.

**Question 17:** What tools have you used for API testing (e.g., Postman, Swagger, JMeter)? Which one do you prefer, and why?
**Answer 17:** <!-- <Write your answer here> -->
Postman, restassured, request module, swagger.
Postman is best, because its a complete tool, where we can do functional, regression testing of the APIs.

**Question 18:** What's your experience with manual testing?
**Answer 18:** <!-- <Write your answer here> -->
13 years of experience in manual testing. All new functionalities have to be manual tested then only can be automated if they are working fine in production.

**Question 19:** How do you test the integration of an SDK with an application?
**Answer 19:** <!-- <Write your answer here> -->
First perform the component testing.
Then perfom the integreation of the two components once it is ready.
If the component is not ready use stubs or mocks to simulate the original feature.

**Question 20:** Imagine you receive a 401 Unauthorized response during testing. What steps would you take to troubleshoot?
**Answer 20:** <!-- <Write your answer here> -->
First check if the user has access to hit the database.
Second check if the token used is valid or needs to be regenerated.
Check if the url is correct.
Check if the method used is correct.



**Question 21:** What are status codes (e.g., 200, 400, 500) in an API response?
**Answer 21:** <!-- <Write your answer here> -->
Status code tells if the request-response is working as expected or not.
200 means getting data properly from back end, entering values properly in back end.
400 - related to access rights and permissions.
500 - related to server side issues, like server down etc.

# Technical Experience

**Question 22:** What is your experience in mobile / web app testing?
**Answer 22:** <!-- <Write your answer here> -->
13 years of experience in web testing, used selenium webdriver with java, playwright with javascript, playwright with typescript, cypress with javascript.
Used page object pattern for modularity.
Used hybrid framework, to read data from excel and incorporate them in tests.
HTML reports for stakeholders.


**Question 23:** Which programming languages have you worked with?
**Answer 23:** <!-- <Write your answer here> -->
Java, Javascript, Python, Typescript.
