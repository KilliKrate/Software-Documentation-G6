# Test Case Specification

## Lezioni alla pari
April 19, 2020

## Team Members
Ovidiu Andrioaia  
David Cirdan  
Luciano Mateias  
Zhiyang Xia


## Document Control
**Change History**

| Revision | Change Date | Description of changes |
| -------- | ----------- | ---------------------- |
| V1.0     | 04/19/2020  | Initial release        |

**Document storage**

This document is stored in the project's GIT repository at:
[https://github.com/KilliKrate/Software-Documentation-G6/blob/master/docs/Test%20Case%20Specification/index.md](https://github.com/KilliKrate/Software-Documentation-G6/blob/master/docs/Test%20Case%20Specification/index.md)
 
**Document Owner**

Group 6 is responsible for developing and maintaining this document.

## Table of Contents

> [Introduction](#introduction)
>
> [Login Application Integration Tests](#login-application-integration-tests)
>> [An individual signs up to the service](#an-individual-signs-up-to-the-service)
>>
>> [An user logs into the service](#an-user-logs-into-the-service)
>>
>> [An user changes his user settings](#an-user-changes-his-user-settings)
>
> [Lezioni alla Pari Client](#lezioni-alla-pari-client)
>> [An user views the courses, topics and lessons/quizzes list](#an-user-views-the-courses,-topics-and-lessons/quizzes-list)
>>
>> [An user creates a course, topic and lesson/quiz](#an-user-creates-a-course,-topic-and-lesson/quiz)
>>
>> [An user deletes a course, topic or quiz/lesson](#an-user-deletes-a-course,-topic-or-quiz/lesson)
>>
>> [An user opens a lesson](#an-user-opens-a-lesson)
>>
>> [An user takes a quiz](#an-user-takes-a-quiz)
>>
>> [A course administrator edits an existing lesson](#a-course-administrator-edits-an-existing-lesson)
>>
>> [A course administrator edits an existing quiz](#a-course-administrator-edits-an-existing-quiz)


## Introduction

The purpose of this documenti it to outline the integration test cases to be used in different stages of the software developement process. This document focuses mainly on integration testing, as unit testing is already performed by the developer/team working on the module, and is required before submitting a new feature to the existing application. System testing and Acceptance testing is also left out, as they will be done once the application is completed an functional.

[⬆️ Back to Top](#table-of-contents)

## Login Application Integration Tests

### An individual signs up to the service

|||
|-|-|
|__ID__| Test Case 1.1 |
|__Item or Feature__| Sign-Up |
|__Objective__| To ascertain that the registration process is easily completed and that input errors are forwarded back to the user for correction, like in the case of an email that is invalid or already in use |
|__Setup__| The user has launched the service's executable and clicked on the Register button |
|__Expected Output__| The user successfully registers to the service by inserting his personal data and correcting any wrong fields thanks to error feedback provided by the app. The user entry is successfully stored on a persistent user database for future log-in attempts |
|__Test Procedure__| 1. Open the Lezioni alla Pari application through its executable <br> 2. Click on the "Register" button <br> 3. Fill in your data following the app's instructions <br> 4. Correct any incorrect information <br> 5. Submit your registration via the "Submit" button |

### An user logs into the service

|||
|-|-|
|__ID__| Test Case 1.2 |
|__Item or Feature__| Log-in |
|__Objective__| To ascertain that the log-in procedure is easily completed with the assistance of error feedback in case of incorrect input, and that the log-in is secure, not allowing users with incorrect information to log into the application |
|__Setup__| The user has launched the service's executable and has already registered to the service by following the registration procedure |
|__Expected Output__| The user successfully logs into the app by entering his log-in credentials and correcting any wrong fields thanks to error feedback provided by the app. |
|__Test Procedure__| 1. Open the Lezioni alla Pari application through its executable <br> 2. Log-in with the credentials used for the registration procedure <br> 3. Correct any incorrect information <br> 4. Log-in via the "Log-in" button |

### An user changes his user settings

|||
|-|-|
|__ID__| Test Case 1.3 |
|__Item or Feature__| Edit user settings |
|__Objective__| To allow the user to change his user settings, mainly reset his password |
|__Setup__| The user has launched the service's executable and has already logged into the service by following the log-in procedure |
|__Expected Output__| The user successfully resets his password, and is able to log into the service with his new credentials |
|__Test Procedure__| 1. Open the Lezioni alla Pari application through its executable <br> 2. Log-in with the credentials used for the registration procedure <br> 3. Click on the "Edit User Settings" button <br> 4. Reset any data that you wish to reset <br> 5. Correct any incorrect information <br> 6. Click on the Submit button|

[⬆️ Back to Top](#table-of-contents)

## Lezioni alla Pari Client

### An user views the courses, topics and lessons/quizzes list

|||
|-|-|
|__ID__| Test Case 2.1 |
|__Item or Feature__| View courses and its contents |
|__Objective__| To enable the user to view a course, its topics and the lessons/quizzes contained therein. The user shall use this view to select a lesson/quiz he wishes to see |
|__Setup__| The user has logged into the service and launched the app through the welcome screen |
|__Expected Output__| The user is able to view all courses he has access to, and view all of its contents in three separate columns: courses for the first, topics for the second and lessons/quizzes for the third |
|__Test Procedure__| 1. Log into the app via the Login Application <br> 2. Select a Course from the Courses list <br> 3. Select a Topic from the Topics List |

### An user creates a course, topic and lesson/quiz

|||
|-|-|
|__ID__| Test Case 2.2 |
|__Item or Feature__| Create a course, add topics and lessons/quizzes |
|__Objective__| To enable the user to create his own course and populate it with relevant content, which will be made available to other users |
|__Setup__| The user has logged into the service and launched the app through the welcome screen |
|__Expected Output__| The user is able to create courses, topics and lessons/quizzes through the graphical user interface |
|__Test Procedure__| 1. Log into the app via the Login Application <br> 2. Click on the "+" button <br> 3. Give a name to your course <br> 4. Click on the "Create Course" button <br> 4. Repeat the same procedure for topics and lessons, with their respective buttons |

### An user deletes a course, topic or quiz/lesson

|||
|-|-|
|__ID__| Test Case 2.3 |
|__Item or Feature__| Delete a course, topic or lesson/quiz |
|__Objective__| To enable the user to delete content if he so chooses |
|__Setup__| The user has logged into the service, launched the app through the welcome screen and has already created the element he wishes to delete |
|__Expected Output__| The user permanently deletes the course |
|__Test Procedure__| 1. Log into the app via the Login Application <br> 2. Right Click on a quiz <br> 3. Click on the "Delete" button <br> 4. Click on the "Confirm" button |

### An user opens a lesson

|||
|-|-|
|__ID__| Test Case 2.4 |
|__Item or Feature__| Open a lesson |
|__Objective__| To enable the user to view educative content made by himself or other users |
|__Setup__| The user has logged into the service, launched the app through the welcome screen and selected a lesson from an available course|
|__Expected Output__| The user is able to correctly view a lesson, with all of its related content, through the Quill text editor, and go back to the main screen when he so chooses |
|__Test Procedure__| 1. Log into the app via the Login Application <br> 2. Select a course and a topic <br> 3. Select a lesson <br> 4. Wait for the content to load <br> 5. View the selected lesson |

### An user takes a quiz

|||
|-|-|
|__ID__| Test Case 2.5 |
|__Item or Feature__| Complete a quiz |
|__Objective__| To enable the user to start the completion of a quiz |
|__Setup__| The user has logged into the service, launched the app through the welcome screen and selected a quiz from an available course|
|__Expected Output__| The user is able to correctly view the quiz, answer questions, submit his answers and view the result of his attempt |
|__Test Procedure__| 1. Log into the app via the Login Application <br> 2. Select a course and a topic <br> 3. Select a quiz <br> 4. Wait for the content to load <br> 5. Answer the questions <br> 6. Submit the answers via the "Submit" button <br> 7. View the results of the attempt by clicking on the quiz once more |

### A course administrator edits an existing lesson

|||
|-|-|
|__ID__| Test Case 2.6 |
|__Item or Feature__| Edit a lesson |
|__Objective__| To enable the user to create his own educative content by writing and styling text, inserting images or providing external links |
|__Setup__| The user has logged into the service, launched the app through the welcome screen, has created a course, a topic and a lesson |
|__Expected Output__| The user is able to enter the "Edit" screen, create content through the Quill text editor and submit it for persistent storage |
|__Test Procedure__| 1. Log into the app via the Login Application <br> 2. Right Click on a lesson <br> 3. Click on the "Edit" button <br> 4. Wait for the editor to load <br> 5. Write, format and stylize text <br> 6. Insert images or external resources <br> 7. Submit the lesson via the "Submit" button |

### A course administrator edits an existing quiz

|||
|-|-|
|__ID__| Test Case 2.7 |
|__Item or Feature__| Edit a quiz |
|__Objective__| To enable the user to create customizable quizzes for his students |
|__Setup__| The user has logged into the service, launched the app through the welcome screen, has created a course, a topic and a lesson |
|__Expected Output__| The user is able to enter the "Edit" screen, add up to three different types of questions (single choice, multiple choice, open ended) and then submit his quiz for persistent storage |
|__Test Procedure__| 1. Log into the app via the Login Application <br> 2. Right Click on a quiz <br> 3. Click on the "Edit" button <br> 4. Wait for the editor to load <br> 5. Add a question by choosing a type, a title and up to three incorrect answers and one correct answer <br> 6. Submit the question via the "Submit" button <br> 7. Repeat the procedure for multiple questions <br> Submit the quiz via the "Submit" button|

[⬆️ Back to Top](#table-of-contents)