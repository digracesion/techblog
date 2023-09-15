---
title: "Creating Issues in GitHub"
seoTitle: "Creating Issues in GitHub"
seoDescription: "How to manage issues in GitHub, sample issue template and how to use templates for creating issues"
datePublished: Fri Sep 15 2023 08:45:12 GMT+0000 (Coordinated Universal Time)
cuid: clmkcthx1000o09if9oqwdwmp
slug: creating-issues-in-github
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/KPAQpJYzH0Y/upload/da19e75b6aa2e7255fd9a818c7dc6b1d.jpeg
tags: github, qa, template

---

## Issue Management in GitHub

GitHub supports [issue management](https://docs.github.com/en/issues/tracking-your-work-with-issues/about-issues) out of the box. Users can create issues in a [variety of ways](https://docs.github.com/en/issues/tracking-your-work-with-issues/creating-an-issue) and can even link pull requests to issues and resolve an issue automatically once a pull request is merged.

For most teams who don't have the option to subscribe to popular Project Management apps like JIRA, Asana, ClickUp, or Monday, you can make use of GitHub's issue management system to track the bugs in your application.

Additionally, GitHub also has a ["Projects"](https://github.com/features/issues) feature that could connect to different repositories and serve as a task-tracking tool. Since it can be linked automatically to issues, it's easier to track not only tasks but also issues straight from GitHub.

GitHub projects provide the ability to create views and watch tasks as a Table, Board, or Roadmap, so users are free to configure Kanban Boards, Table views, or other ways they wish to view their tasks for their projects.

## Issue Templates

Here are the steps you can follow to create templates for GitHub issues:

1. Open your GitHub repository
    
2. Click on the "Settings" tab
    
3. Under "Features", enable "Issues"
    
4. Click on "Set up Templates". GitHub automatically generates a Bug report template for the repository.
    
5. Click "Preview and Edit" on the Bug Report or Feature Request Template
    
6. Click on the Edit icon right next to the Bug Report or Feature Request Template title
    

Another way is to do the following:

1. Open your GitHub repository
    
2. Click on the "Issues" tab
    
3. Click "New Issue"
    
4. Click "Edit Templates". Click on the `bug_report.md` or `feature_request.md` to select which template to work on
    
5. Click on the Edit icon to edit the template.
    

GitHub supports markdown editing, so feel free to edit the contents of the template. If you wish to follow a sample format for filing bug reports and feature requests, I've come up with the following template that you can also use for your project:

### Bug Reports

```markdown
**Template Name:** Bug Report
**About:** Create a report to help improve the application
**Template Content:**

**Description**

<!-- A clear and concise description of what the bug is. -->

**Expected Behavior**
<!-- A clear and concise description of what you expected to happen. -->

**Actual Behavior**
<!-- A clear and concise description of what actually happened -->

**Steps to Reproduce**
<!-- A step-by-step guide on how to reproduce the issue -->

**Attachments**

<!-- If applicable, add screenshots or video links to help explain your problem. -->

**Minimal example**
 <!-- Link to minimal example, if applicable. eg: StackBlitz link -->

**Additional Notes**

<!-- Add any other remarks or context about the problem here. -->

**Issue Default Title:** [BUG]
**Labels:** bug
```

### Feature Requests

```markdown
**Template Name:** Feature Request
**About:** Suggest an idea to further improve the application
**Template Content:**

**Description of the problem**

<!-- Is your feature request related to a problem that you've encountered? Describe a clear and concise description of what the problem is. e.g.: I'm always frustrated when [...] -->

**Expected Changes**

<!-- A clear and concise description of what changes you would want to happen -->

**Additional Notes**

<!-- Add any other context or screenshots about the feature request here. -->

**Issue Default Title:** [FEATURE]
**Labels:** enhancement
```