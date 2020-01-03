## Requirements for the Lezioni alla pari project
Table of Contents
> 1 INTRODUCTION
>> 1.1 Overview
>>
>> 1.2  Goals and Objectives
>>
>> 1.3 Scope
>>
>> 1.4 Definitions
>> 
>> 1.5 Document Conventions
>>
>> 1.6 Assumptions
>
> 2 GENERAL DESIGN CONSTRAINTS
>> 2.1  Product Environment 
>>
>> 2.2 User Characteristics
>>
>> 2.3 Mandated Constraints
>> 
>> 2.4 Potential System Evolution
>
>3 NONFUNCTIONAL REQUIREMENTS
>> 3.1 Operational Requirements
>>
>> 3.2 Performance Requirements
>>
>> 3.3 Security Requirements
>> 
>> 3.4 Safety Requirements
>>
>> 3.5 Legal Requirements
>>
>> 3.6 Other Quality Attributes
>> 
>> 3.7 Documentation and Training
>>
>> 3.8 External Interface
>>> 3.8.1 User Interface
>>>
>>> 3.8.2 Software Interface
>
> 4 SYSTEM FEATURES
>> 4.1 Feature 1
>>
>> 4.2 Feature 2
>>
>> 4.3 Feature 3
>
> 5 APPENDICES

Authors<br>
Ovidiu Andrioaia, David Cirdan, Luciano Mateias and Zhiyang Xia.
### 1 INTRODUCTION
#### 1.1 Overview
Lezioni alla pari is an application that focuses on simplyfing the sharing of knowledge between various parties inside a closed environment (e.g. the departments of a company) easier and within everyone’s reach. The software streamlines the creation of courses that can contain documents, videos and quizzes on a wide range of topics.

This document provides information on the requirements of the Lezioni alla pari application, and aims to deliver an intelligible documentation of the software to the developers that can use it as a reference, as well as their customers, that can have a deeper insight of the project and its sophistications.
#### 1.2 Goals and Objectives
The main objective of this project is to develop a platform that will provide the following:
1. A login system for the users
2. An intuitive graphical user interface
3. A lesson creating system with containers that can have documents, videos and quizzes
4. Automated quiz correction
### 1.3 Scope
Lezioni alla pari will store all the users data inside a local file, all the contents created inside the user environment won't be accessible outside
the platform, and only registered individuals will be able to participate. The application is open-source and can be downloaded through Github, it can be installed only on Personal Computers.
### 1.4 Definitions
**Use case** - describes a goal-oriented interaction between the system and an actor. A use case may define several variants called scenarios that result in different paths through the use case and usually different outcomes.

**Actor** - user or other software system that receives value from a use case.

**System** - set of features provided by the application that are directly associated with each other.

**Scenario** - one path through a use case.

**Application** - what is being described here; the software system specified in this document.

**Project** - activities that will lead to the production of the application described here.

**Interface** - visual representation of the system 

### 1.5 Document Conventions
TBD (to be defined / to be discussed) - information that still needs to be gathered, framed or that it is incomplete.
<br>
Unknown - development feature, option that hasn't been implemented yet.
### 1.6 Assumptions
It is assumed that users will have installed all the required libraries and the latest version of python3 before starting
to use the program. Apart from the application login, there are no security measures nor automated data backup.


