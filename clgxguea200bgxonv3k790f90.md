---
title: "A Guide on How to Write Test Cases"
seoTitle: "A Guide on How to Write Test Cases"
seoDescription: "Here is a helpful guide on how to write test cases, suggested test case management tools, test case format, and test case creation best practices"
datePublished: Wed Apr 26 2023 09:00:39 GMT+0000 (Coordinated Universal Time)
cuid: clgxguea200bgxonv3k790f90
slug: a-guide-on-how-to-write-test-cases
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/mcSDtbWXUZU/upload/3e151752545391452da6ed01464ecc58.jpeg
tags: testing, testcases, test-case-management-tools, test-case-management-software, test-case-creation

---

# What is a Test Case?

According to [Guru99](https://www.guru99.com/test-case.html), a **Test Case** is "a set of actions executed to verify a particular feature or functionality of your software application." Unlike **Test Scenarios** which are a bit more vague and cover a wider range of scenarios, test cases are more specific, citing more specific conditions to be tested.  

# Test Case Creation Tools

Here are some helpful tools that I've personally tried using when creating test cases:

1. Microsoft Excel
    
2. Google Sheets
    
3. Tricentis Test Management
    

# Test Case Format

Test Cases have different formats depending on the standards of the organization. The following is a format that I've been using for years:

### Sheet 0: File Title

* Component\_TestType\_YYYYMMDD-&lt;version-number&gt;
    

### Sheet 1: Title Page

* Application/Component to be tested
    
* Acronyms and meanings (if applicable)
    
* Document version
    

### Sheet 2: Document History

* Date
    
* Document Version
    
* Changes Made
    
* Author
    

### Sheet 3: Configuration Sheet

* Test Environment - include whatever is applicable to your test
    
    * OS:
        
    * OS version:
        
    * Browser:
        
    * Kernel version: (usually for Linux-based OS)
        
    * Application Version
        
    * Platform version
        
    * BIOS version
        
    * Hardware Version
        
    * Firmware Version
        

### Sheet 4: Test Case Sheet

* Sheet Name - Base the sheet name on the component or feature being tested
    
* Tester - who executed the tests
    
* Author - who wrote the test cases
    
* Reviewer - who reviewed the test document
    
* Test Cases
    
    1. **Test Case No.** - based on the page/component to be tested, e.g. XXX-0001
        
    2. **Test Scenario** \- Test Scenario covering the test case to be done, e.g. Sign Up
        
    3. **Test Case** - The specific test to be done, e.g. Sign up using Google SSO
        
    4. **Description** - A description of the Test Case (if applicable)
        
    5. **Pre-conditions** - conditions that need to be satisfied before the test is executed
        
    6. **Test Steps** - steps to be followed to ensure that the test case is properly executed
        
    7. **Post-conditions** - expected conditions of the application after the test steps are executed
        
    8. **Expected Results** - results that are expected following the execution of the test case. This becomes the basis for the PASS/FAIL result
        
    9. **Test Results** - <mark>PASS/FAIL/SKIPPED</mark>, <mark>OK/NG/SKIPPED</mark>. The words used for the results are usually dependent on the standards of the organization, but PASS/FAIL/SKIPPED are the standard
        
    10. **Test Run Date** - the date when the test case was executed. It's expected that all the tests for this document are executed on the same day to ensure that there are no variable changes. However, there are possible exceptions to this like "Long Run Tests", and "Sleep Tests" among others, which require a day or more to execute.
        
    11. **Remarks** - any notes or links for references  
        

# Best Practices

1. **Simplicity** - Test Cases should be simple and not overly complicated. They must be as clear and concise as much as possible so that even if the tester is not the author of the document, they would not have a difficult time running the tests.
    
2. **Identifiability** - Test Cases are identifiable with their Test Case Number. This should be unique to each test case to avoid mistakes in identifying which test case is which and for what component.
    
3. **Understandability** - Test Cases should be easy to understand and are self-explanatory
    
4. **Traceability** - the test cases must be mappable to the requirements documents (Software Development Requirements, Basic Requirements, Detailed Requirements, etc). Functionalities and tests should **not** be assumed when writing the test cases.
    
5. **Consider Use Case Scenarios** - As Use Case Scenarios were written with the roles of specific users in mind, it's helpful to refer to Use Cases when creating test cases.
    
6. **Ensure 100% Coverage** - test cases must cover all of the requirements. This could be checked by referring to an RTM (Requirements Traceability Matrix)
    
7. **Do Not Repeat Yourself (DRY)** - Do not repeat test cases. If test cases are needed to execute a subsequent test case, it can be referenced using its Test Case Number.
    
8. **Updatability** - Test Cases should be updatable to keep up when there are changes in the requirements or scope of the application
    
9. Make use of existing test techniques and principles
    
    1. **Boundary Value Analysis (BVA)** - testing values that are on the boundaries of the accepted inputs to avoid exhaustive testing
        
    2. **Equivalence Partition** - dividing test values into partitions that could cover the specified values in the range to avoid exhaustive testing
        
    3. **State Transition Technique** - testing to how switching between states after doing certain actions affects the behavior of the application
        
    4. **Pareto Principle** - the 80-20 principle, where 80% of bugs are found in 20% of the components. Simply put, this means that most bugs can usually be found in the same components
        
10. **Self-cleaning** - after executing the test cases, the environment should not be rendered unusable; the environment should be able to be reverted back to its state before the test case was executed.
    
11. Use an **ACTIVE VOICE** when writing the test cases
    
12. A single test case should not have more than **15 steps**. Otherwise, consider dividing the test case into parts.