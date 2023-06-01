---
title: "Creating Test Cases In JIRA with Tricentis"
datePublished: Thu Jun 01 2023 03:00:39 GMT+0000 (Coordinated Universal Time)
cuid: clicju3l001ahrjnvgyneduiv
slug: creating-test-cases-in-jira-with-tricentis
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1685373316690/d9f5eece-9df5-4993-b050-ab78222251a4.png
tags: workflow, testing, jira, test-case-management-tools

---

# A Brief Introduction to JIRA

JIRA is a product of Atlassian and is considered one of the most popular project management and issue-tracking tools for software development and testing. It provides teams with a centralized platform to plan, track, and manage their projects, tasks, and issues.

The following are some benefits of using JIRA in software development:

1. **Issue Tracking**: JIRA allows teams to create and track issues throughout the software development lifecycle. "Issues" aren't only about bugs, but can also include feature requests, tasks, and so on. Each issue can be assigned to a team member, given a certain priority level, labeled, categorized, and tracked from the time it was created until a resolution is reached.
    
2. **Project Management:** It supports project creation and management, including capabilities to define project components, set up versions and milestones, and assign tasks to team members. This helps in ensuring transparency, collaboration, and timely completion of project milestones.
    
3. **Agile Methodology Support:** JIRA's flexibility enables it to support agile methodologies such as Scrum and Kanban, which can help agile teams easily visualize their workflow, manage their backlog, and adapt to changing requirements. Features like user stories, sprints, backlogs, and agile boards, allow teams to plan, prioritize, and track their work using agile practices.
    
4. **Customization and Workflow Automation:** With JIRA, users can customize labels, fields, workflows, and issue types based on their needs. It also provides support for workflow automation through its built-in rule engine, enabling teams to automate repetitive tasks, notifications, and workflow transitions.
    
5. **Enables Collaboration and Communication:** JIRA promotes collaboration and communication among team members by providing features such as comments, mentions, attachments, notifications, and in-app integrations with other collaboration tools to enable team members to discuss issues, share information, and provide updates.
    
6. **Integration and Extensibility:** JIRA offers various integrations with other development and testing tools. Source code repositories, continuous integration and deployment tools, and test management systems, are only some of the integrations that allow seamless data flow and synchronization between different tools, providing a unified project view.
    
7. **Reporting and Metrics:** JIRA provides reporting and metrics capabilities to track project progress, team performance, and issue resolution time. It offers built-in reports like burndown, velocity, and control charts, which are useful for monitoring and analyzing project data. Teams can use these metrics to identify bottlenecks, make data-driven decisions, and continuously improve their development and testing processes.
    

# Tricentis

Tricentis Test Management for JIRA is an add-on that integrates the Tricentis Test Management solution with JIRA. It extends the capabilities of JIRA by providing advanced test management functionalities that are not native to the application.

Here are some benefits of using Tricentis Test Management for JIRA:

1. **Test Planning and Design:** The Tricentis Test Management tool allows teams to create and manage test plans, test cases, and test suites directly within JIRA. Created test cases are counted as "Issues" in JIRA and provided the "Test Case" Issue type. They can also be organized into hierarchical folders, tagged with relevant labels, and associated with requirements, user stories, or other issues in JIRA.
    
2. **Test Execution and Tracking:** Team members can execute test cases and track the results of manual and automated tests within JIRA. Test runs can be scheduled within releases, assigned to team members, and tracked for progress. Testers can record their execution status, and attach screenshots, screen records, logs, or other artifacts found during testing.
    
3. **Traceability and Coverage:** The tool provides traceability between test cases and requirements or user stories. This helps generate a Forward Traceability and/or Backward Traceability matrix for the teams to ensure that the test coverage aligns with the project requirements.
    
4. **Test Metrics and Reporting:** Teams can generate reports on test execution progress, test coverage, defect trends, and other relevant metrics to help stakeholders gain insights into the testing process, identify bottlenecks, and make informed decisions.
    
5. **Integration with Automation Tools:** Tricentis Test Management for JIRA integrates with various automation tools, such as Tricentis Tosca and Selenium, among others to allow teams to execute automated tests and synchronize the test results within JIRA. These integrations help streamline the testing process and provide a consolidated view of manual and automated testing efforts.
    
6. **Import Test Cases**: The tool enables importing test cases from an Excel file, following the required format prescribed in the sample template they provide. It's also possible to import test cases by integrating other services, but this is the native implementation of test case importing embedded into the tool
    

# JIRA Issue Creation

## Process

The following provides a step-by-step process on how to create an issue in JIRA

1. From the JIRA page, open the Project Dashboard
    
2. Click "Apps" from the navigation header
    
3. (Assuming that your JIRA administrator has enabled templates) Select "Create from Template".
    
4. To create a Bug ticket, select the "Bug" issue type and the Bug template you need to use. For Feature/Improvement Requests, select the "Code Task" issue type and the Template that you need to use.
    
5. If you're just creating an issue without using a template, you can skip steps #1-4 and create a ticket by clicking the "Create" button on the top of the global navigation menu.
    
6. Click the "Confirm" button. This will show a modal to provide values for dynamic variables (if the issue is created from a ticket)
    
7. Click the "Confirm" button to move on to the issue creation page.
    
8. Fill in the [values](#values) for the issue.
    
9. Once the values are filled in, click the "Create" button.
    
10. Click "Close" to close the issue or "Confirm" to create another issue.
    

## Values

* **Summary** - Provide a quick overview of the issue
    
* **Assignee** - Unassigned
    
* **Priority**
    
    * **Highest** - urgent issues like issues affecting all customers, issues that cause the environment to fail, and issues with hotfixes required
        
    * **High** - customer requests or issues encountered by a group of customers
        
    * **Medium** - medium-level issues. In some tickets, these are tagged as "Normal" level issues due to labeling problems with integrated applications like GitHub.
        
    * **Low -** cosmetic issues, issues that aren't necessary to be fixed in the current sprint
        
    * **Lowest** - negligible issues, but having the fix for this would be nice to have
        
* **Affects Versions** - the version affected by the bug. If it's found in the dev environment, add the pending release as the affected version. If it was found in the production environment, add the version number of the latest app release as the affected version.
    
* **Fix versions** - the version when the fix for the specific issue was released or is planned to be released
    
* **Browser** - The name of the browser being used when the issue was reproduced
    
* **OS** - The operating system being used when the issue was encountered and/or reproduced
    
* **Attachment** - The section where users can provide screenshots or screen recordings of the issue encountered
    
* **Description** - A more in-depth description of the issue. The following includes a list of information that would be helpful to add to the issue description:
    
    * **Expected Results -** the expected result of the action done or the expected output of the feature
        
    * **Actual Results -** the actual result of the action done, or the actual output of the feature
        
    * **Steps to Reproduce** - a step-by-step description of the actions done to reproduce the issue
        
    * **Frequency Rate** - (Failure Rate/Trials Done)x100 = Frequency Rate (%)
        
    * **Workaround** - Workaround executed to mitigate the issue, if any
        
    * **Possible Root Cause** - a possible cause of the issue happening
        
    * **Fixes Done** - fixes that were done or will be implemented to resolve this issue
        
    * **Additional Notes** - Additional notes that are important to the ticket but weren't covered by the existing labels or descriptions, if any
        
* **Components** - Specific component/s where the issue was found
    
* **Labels** - optional, as this is usually dependent on the rules of the organization
    

## Test Cases

Test Case issues are created to serve as the test cases for a project and can be reused throughout the project's life cycle. When using the Tricentis Test Management Tool with JIRA, these test cases are classified as "Test Case" issue types. The following are the configurations related to Test Cases created with the Tricentis tool:

1. **Folder** - As a standard, this should be named after the function, component, or page where the test case belongs to
    
2. **Key** - The Issue number, concerning the project where the test case is created
    
3. **Summary** - As a standard, it's helpful to make use of the test case number to keep track of the test case for the page where it belongs. Using other test cases as a guideline, this would then follow the format: &lt;3-4 letters&gt;-####
    
4. **Description** - A basic description of the test case to be executed. This doesn't need to be as elaborate as the descriptions of the bug tickets or feature request tickets.
    
5. **Environment** - The environment where the test case will be executed. For a web app, the following format could be followed: **OS**, **Browser,** and **URL**
    
6. **Pre-condition** - Pre-conditions or assumptions that are needed for the test to work
    
7. **Test Steps** - Steps executed for the Test Cases
    
8. **Step Data** - Data inputs needed to execute the test cases and get the expected results
    
9. **Expected Results** - Expected results of the steps executed
    
10. **Linked Issues** - link the related Requirements Issues to enable RTM Generation
    
    * **Requirements Issues** - Issues created for coverage checking. This serves as the Requirements Checklist
        
    * **Epic Issues** - specifications for the Requirements issues. These are big code tasks that need more than 1 sprint to be completed
        
    * **Code Task** - Feature Requests for better Usability, Navigation, etc. to improve user experience
        
    * **Sub Tasks** - Child tasks of Epic issues or code tasks
        
11. **Components** - related components from the application
    
12. **Label** - optional, but it would be helpful to categorize all tests under one label, such as `testing`
    
13. **Type of Test** - Tricentis has two types of tests: `Functional` or `Non-functional`. So choose whatever fits the description of the test being run best
    

# Conclusion

Tricentis Test Case Management Tool is a helpful add-on for teams who already make use of JIRA for bug tracking and/or project management. Instead of looking for an external solution that might bring in additional third-party costs, it's important to consider how to improve existing systems first.

I hope this guide could help not only other testers looking for a test case management tool to integrate with JIRA, but those who want to improve their issue creation or ticket filing system in JIRA as well.