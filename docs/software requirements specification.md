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

Authors  
Ovidiu Andrioaia, David Cirdan, Luciano Mateias and Zhiyang Xia.
## 1 INTRODUCTION

### 1.1 Overview
Lezioni alla pari is an application that focuses on simplyfing the sharing of knowledge between various parties inside a closed environment (e.g. the departments of a company) easier and within everyone’s reach. The software streamlines the creation of courses that can contain documents, videos and quizzes on a wide range of topics.

This document provides information on the requirements of the Lezioni alla pari application, and aims to deliver an intelligible documentation of the software to the developers that can use it as a reference, as well as their customers, that can have a deeper insight of the project and its sophistications.

### 1.2 Goals and Objectives
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

#### 1.5 Document Conventions
TBD (to be defined / to be discussed) - information that still needs to be gathered, framed or that it is incomplete.  
Unknown - development feature, option that hasn't been implemented yet.
#### 1.6 Assumptions
It is assumed that users will have installed all the required libraries and the latest version of python3 before starting
to use the program. Apart from the application login, there are no security measures nor automated data backup.

## 2 GENERAL DESIGN CONSTRAINTS

### 2.1 Product Environment
Lezione alla pari is the first product in our series dedicated to online learning and does not require a third part software. It is portable and usable by any operating system or hardware.

### 2.2 User characteristics
In order of increasing priority, the following categories of users can be distinguished for this application:

* Companies and other work areas, who can use our product to simplify the learning of the courses (for example the safety courses), or to explain the operation of a new machinery

* Schools, who can use our product to provide simplified learning. These users will probably be the primary users of the user interface.

### 2.3 Mandated Constraints
For now, our product works only locally, functioning as a closed system. The only requirements for our platform are: 
1. stable internet connection 
2. device that can connect to the network
3. Python knowledge

### 2.4 Potential System Evolution
For now, our product works only locally, but we are planning to make the platform web based. making it available to all world users without having to install the application

## 3 NONFUNCTIONAL REQUIREMENTS

### 3.1 Operational Requirements

- The application will allow users to concurrently access and modify the data. In case a lesson is edited, all users currently accessing said lesson will be notified and offered to switch to the new version, or keep reading/watching the current one.

### 3.2 Performance Requirements

- The server will accomodate, at release, up to 100TB of data, delivered through Amazon AWS, which provides efficient document delivery and video streaming all over the world. This will of course scale as the application becomes more popular.

- Response times may vary based on server workload. All database operations like login, registration and document reading should take <1 second. 

- Document editing may take more based on the size of the uploaded images, if any. 

- Video lesson streaming is guaranteed to be fluid with resolutions up to 720p, 1080p and more will be available, but may result too slow if the content delivery servers are under heavy workload.

- Video lesson upload will take more, based on server workload and user connection speed.

### 3.3 Security Requirements

- The application must use the most up to date standards and practice for its security: sensible information created and shared by users must be kept private and confidential. The software must adhere to the NIST, OWASP and CWE standards, in order to protect data from malevolent attacks to the platform.

- The application must guarantee absolute privacy: data shared through our servers will be encrypted and inaccessible by anyone but the intended recipients of the information. This also includes the team members themselves.

### 3.4 Safety Requirements
No safety requirements were identified for this application.

### 3.5 Legal Requirements
All data delivered through the platform is private, and will throughly adhere to GDPR laws and OECD Privacy Principles. Copyright will not be enforced on user-made content, since it is of a private, non-commercial and non-redistributable nature.

### 3.6 Other Quality Attributes

- The software is portable on all desktop computer platforms, since the application heavily relies on Python. A mobile app will be made available if demand justifies it.

- If the end-user wants to establish his own private Lezioni alla Pari server, instead of using the offical one, he should be able to. This will ensure maximum privacy and performance. A standalone server executable shall be thereby included in a post-release update if the demand justifies the developement costs. 

### 3.7 Documentation and Training

- No training will be delivered when the application is delivered. A short tutorial will introduce the new users to the main features of the application. The application should be extremely intuitive to use, so UX will be a big focus during developement.

### 3.8 External Interface

#### 3.8.1 User Interface 
- The user interface for the application will follow a modern and minimalist style, which makes important elements easily noticeable, and keeps the main features always in view.

- The login and registration forms will be quick and straightforward, with the purpose of introducing the user to the application immediately.

- An user will easily be able to determine the courses and lessons he has created, thanks to smart color use, and will also have easy access to any content he needs.

- Accessibility options, such as increased font sizes and color blindness support will be available at launch.

#### 3.8.2 Software Interface

- All operations and logic defined by the use cases will be achieved through Python and SQL queries. SQL will take care of login, registration and course access, while a cooperation between SQL and Python will achieve document delivery and video streaming