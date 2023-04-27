---
title: "Ewww, why is there a bug in my code?"
datePublished: Fri Apr 21 2023 09:00:42 GMT+0000 (Coordinated Universal Time)
cuid: clgqbn7d002ga9onv2yz70e5p
slug: ewww-why-is-there-a-bug-in-my-code
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/qZzJoiKHqmo/upload/5ffc77a64f85b3bd2cd75e0143adccc3.jpeg
tags: testing, qa, software-testing, bugs-and-errors, qa-testing

---

# What is a Bug?

<mark>Clue: the answer is unrelated to the cover photo of this post.</mark>

In the context of Software Development, a bug is an unexpected result of an unwanted event triggered due to known or unknown causes, which ends up making the software application not work as per the expected results or as specified in the requirements.

And, much like some bugs, they make us feel bad. (And maybe a little worse than bad in the cases where these bugs could turn disastrous).

Human errors, failing to catch incorrect inputs, hardware errors--there are so many possible causes for bugs to appear. This is why it's important to run efficient and effective tests in order to mitigate the risk of having a buggy application.

Kind of a long definition right there, so quickly map it out:

<mark>ERROR leads to a BUG, which causes the system to FAIL.</mark>

# Types of Bugs

There are varying types of bugs depending on their source, where they're found, and the risks they pose, among several considerations.

Here is a list of common types of bugs that can be encountered when dealing with a web application:

1. **Functional Bugs** - bugs that are mainly due to the application's results not aligning with the expected results as per the requirements
    
2. **Logical Bugs** - bugs that cause the application to behave incorrectly due to some logical errors introduced into the system.
    
3. **Workflow Bugs** - bugs that cause the user's navigation through the application to be disrupted.
    
4. **Unit Level Bugs** - bugs found in component or unit levels
    
5. **System-Level Integration Bugs** - bugs that appear due to the failure of interactions between integrated units of code forming the application.
    
6. **Out-of-Bound Bugs** - bugs that are due to unexpected usage of the app, including entering out-of-bounds values and invalid input types into input fields.
    
7. **Security Bugs** - bugs that pose a security risk to both the users and developers of the application. This might come in the form of data leaks, data manipulation, and other exploitations of vulnerability.
    
8. **UI Bugs** - bugs related to the design or layout of the application that make it difficult for the user to interact with the application.
    
9. **Cosmetic Bugs/Visual Bugs** - similar to UI bugs, except Cosmetic Bugs are mostly due to small errors that don't necessarily disrupt the user's workflow. Examples of these include typographical errors, inconsistent terminologies used in buttons, etc.
    

# Why do bugs need to be solved?

As early as possible in the Software Developer Life Cycle, it is important to be able to detect and fix bugs. This is because the longer along the cycle the bug is found, the more costly it is to fix.

An example of this is a bug that is missed by the developers and the QA team and made it to the customer at production. Aside from causing a longer turnaround time to fix the bug (i.e. the cost it takes for the dev team to do the fix, for the QA team to re-run the tests, and for the development team to deploy the fix), there's also the cost of trust (i.e. the customer might be unsure of the security or reliability of the application especially if they're encountering so many bugs), and might also incur additional costs on the side of other departments.

# Bug Tracking Tools

Bug tracking tools are software tools that are used by Software Development and QA Teams to identify, track and manage bugs, feature requests, and the like in their application.

Integrating bug-tracking tools into the workflow not only helps track bugs and map them to requirements easily, but it could also reduce the working time for QA and the development team to record progress.

It's important to establish a Bug Tracking Tool to be used throughout the organization in order to streamline the reporting, tracking, and managing process of the bugs found in the application.

Bug tracking tools also provide easier and faster communication, collaboration, and turnaround time in-between teams.

Bug tickets also serve as sources of information about the application, and are therefore usable as part of the application's documentation.

Here are some bug-tracking tools that I've tried using myself:

1. [JIRA](https://www.atlassian.com/software/jira)
    
    JIRA is arguably the most popular bug-tracking tool of the ones I've used. It has an intuitive interface, it's easy to use and informative without feeling too overwhelming.
    
    Because of its popularity and worldwide adoption, a lot of third-party tools can be integrated to be used with JIRA. This makes it easier to integrate JIRA into the team's workflow (which is, frankly, a huge factor to consider when deciding on a bug-tracking tool to use)
    
    Fun fact: Atlassian has a FREE online training course on [JIRA Fundamentals](https://university.atlassian.com/student/path/815443-jira-fundamentals?sid=196463ab-a6c3-4d8a-a323-7e028111c5b3&sid_i=9) which comes with a badge that you can add to your portfolio!
    
2. [Bugzilla](https://www.bugzilla.org/about/features)
    
    Bugzilla is a free, open-source bug-tracking tool that is easy to install and use. Although the interface looks simple, it does the job well and is even being used by [Mozilla](https://bugzilla.mozilla.org/home) as their bug-tracking tool. It also integrates with some third-party applications such as Bonsai, CVS, Subversion, and Tinderbox
    
3. [GitHub](https://docs.github.com/en/issues/tracking-your-work-with-issues/about-issues)
    
    If your workflow already makes use of GitHub as a repository, you might consider using its issue-reporting system. Although Github does already have a built-in bug reporting system in each repository, there are also a [bunch of templates](https://github.com/devspace/awesome-github-templates) you can use for customizing your bug tickets. However, it still does allow the configuration of external issue trackers such as JIRA.
    
4. [Gitlab](https://docs.gitlab.com/ee/user/project/issues/index.html)
    
    Similar to Github, Gitlab also has a built-in issue-reporting system within the repository. It also supports third-party applications, including JIRA, Bugzilla, and Redmine.
    
5. [Redmine](https://www.redmine.org)
    
    Redmine is a "flexible project management web application written using Ruby on Rails Framework" (or so its website says). It's also open source and is hosted on SVN as well as Github.
    
    It also supports plugins including TW Watchers, Gantt Chart plugin, UX Upgrade Plugin, and Resource Management Plugin.
    
6. [Mantis](https://mantisbt.org)
    
    Mantis is also an open-source issue tracker that has a simple interface but is able to provide a customizable workflow. It's also well-documented, with several guides provided for Administrators and Developers.
    
    There are a ton of installable plugins to help increase productivity and make it easier to integrate into the team's workflow.
    

# Bug Ticket Format

As someone who's been filing bug tickets as a QA left and right for almost 4 years, here's a template that you can use as a basis for your own team's bug tickets.

### \[Summary/Title\]

*Use the Summary of the bug ticket as its title to make it easier to identify the tickets.*

### \[Description\]

*Describe in more detail what the bug is. Some important questions to ask yourself: What is happening? Why is it happening? Where is it happening?*

### \[Expected Results\]

*What are the expected results as per the requirements?*

### \[Actual Results\]

*What are the actual results that happened once testing was done?*

### \[Steps to Reproduce\]

*Provide the detailed steps to reproduce the issue.*

### \[Workaround\]

*If possible, provide some workarounds you found to mitigate the current issue.*

### \[Failure Rate\]

How often is the issue happening? Is it intermittent (i.e. less than 10% chance to occur), or is it a solid issue? To get the failure rate, use the following formula:

$$TestPassCount/TestFailCount$$

As a standard baseline, it is good to re-run the tests for a minimum of 5 times to see if the bug is a solid issue

### \[Additional Notes\]

*If there are any other additional information gathered, provide them here. E.g. this issue only happens in a specific app version, if it is only happening in dev and not in prod, etc.*

### \[Possible Root Cause\]

*Once you have identified the root cause of the issue, it would be easier to find a fix for it.*

### \[Possible Fixes\]

*It's good to note what helped fix the issue for documentation purposes.*

### \[Environment\]

***OS****:*

***Kernel Version:*** *(if applicable)*

***Browser****:*

***Platform/Model:***

***BIOS Version:*** *(if applicable)*

### \[Component\]:

*Any components from your application related to the bug. This would depend on your organization.*

### \[Labels\]:

*Any labels associated with the bug. Hardware, software, customer report, etc. Again, this would all depend on your organizational standards.*

### \[Priority\]:

*Highest, High, Medium, Low, Lowest*

### \[Severity\]:

*High, Medium, Low*

### \[Fix Version\]:

*Provide the version number of where the fix will be released*

# References:

[Types of Software Bugs | Browserstack](https://www.browserstack.com/guide/types-of-software-bugs)

[Bugs in UI Testing | Browserstack](https://www.browserstack.com/guide/bugs-in-ui-testing)

[Software Testing Bug vs. Defect vs. Error vs. Fault vs. Failure | Guru99](https://www.geeksforgeeks.org/software-testing-bug-vs-defect-vs-error-vs-fault-vs-failure/)