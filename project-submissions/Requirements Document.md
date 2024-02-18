# Requirements Document - Banter Ice Cream (January 28, 2024)

# Revision History

| Name | Date | Reason for Changes | Version |
| ----------- | ----------- | ------------- | ---------- | 
| Amanda Anderson | January 29, 2024 | Create document from template and draft section 1 | 1.0 |
| Dhuruvan Anavaratha Krishnan | January 29, 2024 | Created draft for sections 2.4 and 2.5 | 1.1 |
| Yu Tang | January 29, 2024 | Created draft for sections 4.2 - 4.5 | 1.2 |
| Benjamin Osalira | January 30, 2024 | Created draft for section 3: 3.1, 3.2 and 3.3 | 1.3 |
| Justin Drastil | January 30, 2024 | Created draft for section 4.1 | 1.4 |
| Luca Bolzonello | January 30, 2024 | Edit of section 3.3 | 1.5 |
| Nolan Curtis | January 30, 2024 | Created draft for 2.1 | 1.6 |
| Tim Xu | January 30, 2024 | Created draft for 2.2 and 2.3 | 1.7 |
| Everyone | January 30, 2024 | Review and edit sections | 1.8 |
| Everyone | January 31, 2024 | Further review and change formatting | 1.9 |
| Everyone | February 2, 2024 | Final Review | 2.0 |
| Amanda Anderson | February 8, 2024 | Add template for sections 5-10 | 3.0 |
| Everyone | February 10-13, 2024 | Update document according to feedback | 3.1 |
| Amanda Anderson | February 13, 2024 | Update template for sections 5, 6 | 4.0 |

# 1. **Overview** <a name="overview"></a>

This document will explore an opportunity to centralize Banter Ice Cream’s internal management. First, we will discuss Banter’s business requirements and illustrate the goal of the project. Second, the document will discuss the major features, scope, and limitations of the project. Third, more context for the project will be provided such as user classes, operating environment, and constraints. Fourth, will expand on each system feature to include description, priority, functional requirements, and use cases. Fifth, will define data requirements. Sixth, will describe external interface requirements including user interfaces, hardware interfaces, software interfaces, and communication interfaces. Seventh, will discuss software quality attributes that are prioritized in system. Eighth, will include further analysis models. Finally, there is an appendix for additional details.

These sections are outlined in the following Table of Contents.

## **Table of Contents**
1. [Overview](#overview)
2. [Business Requirements](#requirements)
   1. [Background](#background)
   2. [Buisiness Opportunity](#opportunity)
   3. [Business Objectives](#objective)
   4. [Success Metrics](#success)
   5. [Product Vision Statement](#vision)
3. [Scope and Limitations](#scope)
   1. [Major Features](#features)
   2. [Project Scope](#project-scope)
   3. [Limitations and Exclusions](#limitations)
4. [Context Description](#context)
   1. [User Classes and Characteristics](#user-classes)
   2. [Operating Environment](#operating-environment)
   3. [Design and Implementation Constraints](#constraints)
   4. [Assumptions and Dependencies](#assumptions)
   5. [Glossary of Terms](#glossary)
   6. [References](#references)
5. [System Features](#system-features)
   1. [Scheduling and Time Tracking](#feature-1)
   2. [Communication and Announcment](#feature-2)
   3. [Recipe Management](#feature-3)
   4. [Onboarding Materials](#feature-4)
6. [Data Requirements](#data-requirements)
   1. [Logical Data Models](#data-model)
   2. [Data Dictionary](#data-dictionary)
   3. [Reports](#data-report)
   4. [Data Integrity](#data-integrity)
7. [External Interface Requirements](#external-interfaces)
   1. [User Interfaces](#user-interfaces)
   2. [Hardware Interfaces](#hardware-interfaces)
   3. [Software Interfaces](#software-interfaces)
   4. [Communication Interfaces](#communication-interfaces)
8. [Software Quality Attributes](#quality-attributes)
9. [Analysis Models](#analysis-models)
10. [Appendix](#appendix)
  
# 2. Business Requirements <a name="requirements"></a>

## i. **Background** <a name="background"></a>
The client, Banter Ice Cream, wants an improvement of the software that they are using for scheduling, communication, and payroll management. Banter's current scheduling system, Homebase, is used at least once per week to check shift schedules, swap shifts, and record time worked. The problem with this current software is it lacks certain features resulting in employees having difficulty switching shifts. A feature missing is the ability for staff to view the available schedules of other employees to find open shifts. Another feature missing results in difficulties in payroll integration with Homebase. Currently the application does not summarize hours which requires bookkeepers to manually calculate regular, holiday, overtime, sick days, and vacation days for each employee. Basecamp is a separate system utilized by Banter Ice Cream to send staff wide announcements and news regarding the company. Having a separate piece of software to receive announcements results in Basecamp being checked infrequently, leading employees to miss messages about new ice cream flavours and ice cream deliveries between locations. Employees missing ice cream flavour announcements lowers customer satisfaction as the provided information about current ice flavours is not accurate. Employees missing messages about scheduled deliveries lowers efficiency as the employees are not prepared to unload the deliveries. The client wants a solution that will make managing finances, swapping shifts, communicating with staff, and onboarding staff easier to accomplish by having one combined app. This conglomeration of their systems will help onboard new staff as less platforms are required to be learned by employees, in addition to all onboarding material being more easily found by all employees.


## ii. **Business Opportunity** <a name="opportunity"></a>
The new system will be a single platform, that combines the functionality of Homebase and Basecamp. Using one platform will improve employee engagement because they will only need to check one application for updates. Using one platform will also reduce onboarding time as new employees only need to learn one system. The new system will improve on the scheduling functionality of Homebase, including features for shift management, swapping shifts, clocking in and out, and calculating hours worked. The scheduling system will reduce scheduling errors due to incorrectly swapped shifts and will reduce payroll errors by summarizing hours according to the client's requests. The new system will also include the communication functionality of Basecamp. The communication system will improve employee knowledge of company updates and increase instances where employees are prepared for planned ice cream deliveries. The new system will also store information about Banter Ice Cream, including onboarding materials and ice cream recipes, so they are available to each employee with access. Both onboarding materials and recipe management will improve employee knowledge of Banter Ice Cream and improve onboarding experience. Improved employee knowledge, improved communication, improved onboarding, and reduced scheduling errors will result a better customer experience and improved customer satisfaction. Overall, the new system shall result in more engaged employees, more satisfied customers, fewer payroll errors, and easier onboarding for new employees.


## iii. **Business Objectives** <a name="objective"></a>

Banter Ice Cream's new system will faciliate business growth through better internal management practices using the new system. The following objectives will all contribute to increased business growth. The methods for measuring these objectives are described in the Success Metrics section.
* Improve employee engagement by 50%.
* Improve customer satisfaction by 25%.
* Reduce time associated with payroll by 25%.
* Reduce manual errors associated with payroll by 50%.
* Reduce time associated with onboarding new employees by 25%.

The listed objectives shall be achieved within three months of release.


## iv. **Success Metrics** <a name="success"></a>

The following metrics will be used to measure the success of the system.

**Announcement Visibility**
      
- Within 3 months of release, staff's interactions with the announcements are increased by 50%. This will be measured by the number of replies, reactions, and further questions to the managers.
      
**Customer Satisfaction**
      
- In 3 months of release, the Google reviews average score would increase by 0.5 stars in its scale of 1 to 5.
- By 6 months, the Google reviews average score would increase by 1.0 star. 

**Bookkeeping Efficiency**
   
- In 3 months of system's release, bookkeepers will spend 25% less time during each payroll period.
- After 6 months of release, manual errors associated with payroll would reduce by 50%.

**Onboarding New Employees**

- Within 3 months of release, new staff should take 25% less time to familiarize themselves with the system during onboarding.


## v. **Product Vision Statement** <a name="vision"></a>
The new system intends to improve communication between staff at Banter Ice Cream. This will be accomplished by reducing scheduling confusion, minimize time spent manually calculating hours, and ensuring relevant information is passed to employees. This will be done by combining the systems that are currently used, Homebase and Basecamp; with additional features to improve the client's integration with Quickbooks. The goal of this product is to increase employee engagement with the system, streamline the creation of staff schedules, improve finance management, and improve customer satisfaction by providing accurate and up to date information.

# 3. Scope and Limitations <a name="scope"></a>

## i. **Major Features** <a name="features"></a>

To ensure Banter Ice Cream's system effectively meets the operational needs and improves internal management, the following features will be included.

**Scheduling System:**
   - Create, modify, and manage shifts through a scheduling interface.
   - Employees can swap shifts, subject to managerial approval, to accommodate personal needs while ensuring operational requirements are met.
   - Calendar views for employees and managers to provide a clear overview of work schedules.
     
**Clock-In and Clock-Out System:**
   - Clock in at the start and clock out at the end of shifts, enabling precise tracking of work hours for all hourly employees.
   - Automatically tracks employee hours, including regular, overtime, sick days, and holidays.
   - Automatically calculate earnings, including overtime.
 
**Recipe Management System:**
   - A recipe management module that allows managers to create, edit, and archive recipes, including full details and allergen information.
   - Front of house staff will have access to view recipes and allergen information but not the detailed ingredients, ensuring they are informed for customer queries without access to proprietary recipe details.
   - Kitchen staff will have access to full recipe details, including ingredient lists, preparation instructions, and allergen information, to ensure accurate preparation.
   - Historical recipe records, enabling tracking of changes over time and access to previous versions for reference or reintroduction.
  
**Communication and Announcement System:**
   - Embedding capabilities for images, videos, and PDFs in announcements and messages to enrich communication.
   - Ability to send and receive company-wide announcements and communicate about shifts changes.   
      
**Role-Based Access:**
   - Different access levels for managers, bookkeepers, delivery drivers, and staff, as defined in User Classes and Characteristics section of this Requirements Document.
   - Safeguard sensitive information through controlled access, ensuring privacy and security across the system.
   - Tailored interfaces and features depending on the user’s role within the company.   

**Onboarding Material Access:**
   - Grant employees access to a library of onboarding materials, such as instructional videos, directly within the system. 
   - Ability to upload onboarding materials.
  

## ii. **Project Scope** <a name="project-scope"></a>

The software being developed is a comprehensive employee management and communication system designed specifically for Banter Ice Cream. Its purpose is to consolidate existing systems Homebase and Basecamp into one centralized platform that integrates with Quickbooks, improving internal communication, scheduling efficiency, and payroll management. The anticipated benefits include better-informed employees, streamlined shift management, reduced manual errors in payroll, and an overall increase in operational efficiency. This directly aligns with the client's objectives of enhancing customer satisfaction, improving employee engagement, and facilitating business growth through better internal management practices.


## iii. **Limitations and Exclusions** <a name="limitations"></a>

**Quickbooks Integration - (Limitation)**
- Direct integration with Quickbooks was determined to be lower priority. Therefore, we will limit this feature to implementing a summary of hours worked by each employee. The bookkeeper can manually process this summary.

**Desktop View - (Exclusion)**
- The clients have indicated that they only want a mobile application view for the system and that the desktop view is not desired.

**Notifications - (Exclusion)**
- It has been determined with clients that notifications are not a high priority for the system.

**Inventory Management System - (Exclusion)**
- Inventory Management was mentioned as a desired feature, but it does not fit in with the rest of the system requested.

**Automated Data Migration - (Exclusion)**
- Automated Data Migration to the new system may be a difficult feature to implement. It is more practical to do manually since it’s a one-time action that only needs to happen once during onboarding to the new system.


# 4 Context Description <a name="context"></a>

## i. **User Classes and Characteristics** <a name="user-classes"></a>

When creating a centralized platform for Banter Ice Cream, understanding the diverse user classes is crutial to craft an efficient and user-centric platform that seamlessly integrates with Banter Ice Cream's opperational needs.
      
**Front of House / Kitchen Managers:**
* **Characteristics:**
   * High frequency of use (daily or weekly)
   * Responsible for scheduling, training, announcements, and managing staff
   * Has a supervisory role
   * Moderate to high technical expertise
* **Requirements:**
   * Advanced scheduling functionalities (creation, editing, approval, etc)
   * Ability to create, view and edit each recipe in the recipe management feature
   * Access to training modules and documents
   * New employee account creation
   * Announcement creation and management
   * Communication channels for group or individual messaging
* **Importance:** Favored user class since there role is critical for staff management and communication

**Bookkeeper:**
* **Characteristics:**
   * Moderate frequency use (mostly during payroll periods)
   * Focus on accounting, payroll, and tracking work hours
   * High technical expertise in accounting software
* **Requirements:**
   * Clock-in/Clock-out features
   * Hours for each employee need to be summarized with overtime, holiday, etc
   * Access to employees banking information
   * Access to training modules and documents
* **Importance:** Critical for financial management (favored class during specific periods)

**Delivery Drivers:**
* **Characteristics:**
   * Use during sporadic weekly shifts
   * Main focus on clocking in/out and communication
   * May have different levels of technical expertise
* **Requirements:**
   * Clock-in/Clock-out features
   * Need to be able to view shift schedule
   * Communication channel for shift-related updates
   * Real-time schedule accessibility
   * Access to training modules and documents
* **Importance:** Frequent users which have direct impact on customer satisfaction (favored user class)
  
**Front of House Staff:**
* **Characteristics:**
   * Daily use during shifts
   * Main focus on clocking in/out, receiving updates, and managing shifts
   * May have different levels of technical expertise
* **Requirements:**
   * Clock-in/Clock-out features
   * Access to allergens from each recipe in the recipe management feature
   * Access to training modules and documents
   * Interface for shift management (Viewing, Shift Change, etc.)
   * Communication channels for shift coverage and updates
* **Importance:** Frequent users with direct impact on customer satisfaction (favored user class)

**Kitchen Staff:**
* **Characteristics:**
   * Daily use during shifts
   * Main focus on clocking in/out, receiving updates, and managing shifts
   * May have different levels of technical expertise
* **Requirements:**
   * Clock-in/Clock-out features
   * Full viewing access to each recipe in the recipe management feature
   * Access to training modules and documents
   * Interface for shift management (Viewing, Shift Change, etc.)
   * Communication channels for shift coverage and updates
* **Importance:** Frequent users with direct impact on customer satisfaction (favored user class)

**Favored User Classes:**
* **Priority Users:** Front of House / Kitchen Managers, Bookkeeper, Front of House Staff, Kitchen Staff
* **Transactional Users:** Delivery Drivers


## ii. **Operating Environment** <a name="operating-environment"></a>

The operating environment for the system is a mobile application that is compatible with both Android and iOS systems. A mobile application was chosen to allow front of house staff, kitchen staff, and delivery drivers frequent access to the system to increase employee engagement. Each front of house staff, kitchen staff, and delivery driver will need to clock in and clock out during their shift. They will also need to access announcements, shift schedules, and messages.

A desktop viewable application will not be considered for the first release of the system.

## iii. **Design and Implmentation Constraints** <a name="constraints"></a>

The system must adhere to the following design and implementation constraints.

**Security of Banking Information**
- Each employee can view and update their own banking information. 
- Banking information for each employee is kept private from all other employees, except bookkeepers. 
- Bookkeepers are able to use banking information to pay employees.
- Abides by provincial and federal privacy laws.

**Number of Employees**
- The system must be able to handle 30 users accessing the system simultaneously.
- Over the system lifetime the system must not limit the number of employees.
- The system must be able to store user data about at least 70 employees.


## iv. **Assumptions and Dependencies** <a name="assumptions"></a>

The following assumptions and dependencies affect the requirements in this document.
- We assume that all employees working at Banter Ice Cream have smartphones that are capable of connecting to the internet. 
- We assume that we are able to interface with Quickbooks.


## v. **Glossary of Terms** <a name="glossary"></a>

| **Word**  | **Definition** |
| ------------- | ------------- |
|  Banter | Banter Ice Cream, an ice cream shop with two locations; in Abbotsford, BC and Chilliwack, BC. |
|  Client | Banter Ice Cream |


## vi. **References** <a name="references"></a>

No references used in this document.


# 5 System Features <a name="system-features"></a>

This template illustrates organizing the functional requirements for the product by system features, the major services provided by the product. You may prefer to organize this section by use case, mode of operation, user class, object class, functional hierarchy, or combinations of these, whatever makes the most logical sense for your product.
 
## i. Scheduling and Time Tracking <a name="feature-1"></a>

State the feature name in just a few words.

### a. Description and Priority
Provide a short description of the feature and indicate whether it is high, medium, or low priority.

### b. Functional Requirements
Where applicable - Itemize the detailed functional requirements associated with this feature. These are the software capabilities that must be present in order for the user to carry out the services provided by the feature, or to execute related use case(s). Include how the product should respond to anticipated error conditions or invalid inputs. Requirements should be concise, complete, unambiguous, verifiable, and necessary. Use “TBD” as a placeholder to indicate when necessary information is not yet available. Each requirement should be uniquely identified with a sequence number or a meaningful tag of some kind. These could be requirements that the clients provided directly or were defined by the designer group as a result of rendering the feature. Each requirement should also include information a(1) bout Backward Traceability (the rationale for the requirements and the source – RFP and which section in it, client meeting and which notes from that meeting, etc.. and (2) Forward Traceability (how the requirement can be verified by the users.

REQ-1:

REQ-2:

### c. Use cases associated with the feature or functional requirement

This is the use case specification. For each Use Case, list the dialog elements in the use case that elaborates or is related to this feature or one of its functional requirements, i.e. sequences of user actions and system responses that stimulate the behavior defined for this feature/functional requirement.


## ii. Communication and Announcment <a name="feature-2"></a>

State the feature name in just a few words.

### a. Description and Priority

Provide a short description of the feature and indicate whether it is high, medium, or low priority.

### b. Functional Requirements
Where applicable - Itemize the detailed functional requirements associated with this feature. These are the software capabilities that must be present in order for the user to carry out the services provided by the feature, or to execute related use case(s). Include how the product should respond to anticipated error conditions or invalid inputs. Requirements should be concise, complete, unambiguous, verifiable, and necessary. Use “TBD” as a placeholder to indicate when necessary information is not yet available. Each requirement should be uniquely identified with a sequence number or a meaningful tag of some kind. These could be requirements that the clients provided directly or were defined by the designer group as a result of rendering the feature. Each requirement should also include information a(1) bout Backward Traceability (the rationale for the requirements and the source – RFP and which section in it, client meeting and which notes from that meeting, etc.. and (2) Forward Traceability (how the requirement can be verified by the users.

REQ-1:

REQ-2:

### c. Use cases associated with the feature or functional requirement

This is the use case specification. For each Use Case, list the dialog elements in the use case that elaborates or is related to this feature or one of its functional requirements, i.e. sequences of user actions and system responses that stimulate the behavior defined for this feature/functional requirement.


## iii. Recipe Management <a name="feature-3"></a>

State the feature name in just a few words.

### a. Description and Priority
Provide a short description of the feature and indicate whether it is high, medium, or low priority.

### b. Functional Requirements
Where applicable - Itemize the detailed functional requirements associated with this feature. These are the software capabilities that must be present in order for the user to carry out the services provided by the feature, or to execute related use case(s). Include how the product should respond to anticipated error conditions or invalid inputs. Requirements should be concise, complete, unambiguous, verifiable, and necessary. Use “TBD” as a placeholder to indicate when necessary information is not yet available. Each requirement should be uniquely identified with a sequence number or a meaningful tag of some kind. These could be requirements that the clients provided directly or were defined by the designer group as a result of rendering the feature. Each requirement should also include information a(1) bout Backward Traceability (the rationale for the requirements and the source – RFP and which section in it, client meeting and which notes from that meeting, etc.. and (2) Forward Traceability (how the requirement can be verified by the users.

REQ-1:

REQ-2:

### c. Use cases associated with the feature or functional requirement

This is the use case specification. For each Use Case, list the dialog elements in the use case that elaborates or is related to this feature or one of its functional requirements, i.e. sequences of user actions and system responses that stimulate the behavior defined for this feature/functional requirement.


## iv. Onboarding Materials <a name="feature-4"></a>

State the feature name in just a few words.

### a. Description and Priority
Provide a short description of the feature and indicate whether it is high, medium, or low priority.

### b. Functional Requirements
Where applicable - Itemize the detailed functional requirements associated with this feature. These are the software capabilities that must be present in order for the user to carry out the services provided by the feature, or to execute related use case(s). Include how the product should respond to anticipated error conditions or invalid inputs. Requirements should be concise, complete, unambiguous, verifiable, and necessary. Use “TBD” as a placeholder to indicate when necessary information is not yet available. Each requirement should be uniquely identified with a sequence number or a meaningful tag of some kind. These could be requirements that the clients provided directly or were defined by the designer group as a result of rendering the feature. Each requirement should also include information a(1) bout Backward Traceability (the rationale for the requirements and the source – RFP and which section in it, client meeting and which notes from that meeting, etc.. and (2) Forward Traceability (how the requirement can be verified by the users.

REQ-1:

REQ-2:

### c. Use cases associated with the feature or functional requirement

This is the use case specification. For each Use Case, list the dialog elements in the use case that elaborates or is related to this feature or one of its functional requirements, i.e. sequences of user actions and system responses that stimulate the behavior defined for this feature/functional requirement.


# 6 Data Requirements <a name="data-requirements"></a>

## i. Logical Data Models <a name="data-model"></a>
E.g., entity-relationship diagrams and UML class diagrams. You may provide a data model for the business operations or the data that the system modifies. Not the same thing as a database design data model.

## ii. Data Dictionary <a name="data-dictionary"></a>

| Data Element       | Description                                                                                          | Composition or Data Type                                                                                | Length  | Values                                                                                       |
|--------------------|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------------------|
| Account Number     | Unique number representing a personal bank account                                                   | Integer                                                                                                 | 12      | Positive numbers                                                                             |
| Allergen           | Details of an allergen found in an ingredient in a recipe                                            | Allergen ID + Allergen Name + Recipe ID                                                                 | N/A     | N/A                                                                                          |
| Allergen ID        | Unique number representing a personal bank account                                                   | Integer                                                                                                 | 12      | system-generated sequential integer, beginning with 1                                        |
| Allergen Name      | The name of a food that according to government of Canada commonly causes an allergic reaction       | String                                                                                                  | 128     | Any ASCII characters                                                                         |
| Announcement       | A message sent out to all employees of Banter Ice Cream                                              | Announcement ID + Author + Content + 0:5{File} + 0:n{Reaction} + 0:n{View} + Date Posted                | N/A     | N/A                                                                                          |
| Announcement ID    | Unique identifier for an announcement                                                                | Integer                                                                                                 | 12      | system-generated sequential integer, beginning with 1                                        |
| Author             | Key to employee who is responsible for creating the object (Announcement, Message, Recipe, Schedule) | Employee ID                                                                                             | N/A     | N/A                                                                                          |
| Banking Info       | Information about an employee’s bank account, such that the bookkeeper can pay the employee.         | Bank Info ID + Employee ID + Transit Number + Institution Number + Account Number                       | N/A     | N/A                                                                                          |
| Bank Info ID       | Unique identifier for stored bank account information                                                | Integer                                                                                                 | 10      | system-generated sequential integer, beginning with 1                                        |
| Contact            | Information used to contact an employee.                                                             | Email + Phone Number                                                                                    | 320     | Form of local@domain                                                                         |
| Content            | The text contents of a message or announcement object                                                | String                                                                                                  | 10000   | Any ASCII characters                                                                         |
| Date Posted        | The date and time that an announcement is sent to the system                                         | DateTime                                                                                                | 8 bytes | Format YYYY-MM-DD HH:MI:SS                                                                   |
| DateTime           | The date and time that a reaction occurs                                                             | DateTime                                                                                                | 8 bytes | Format YYYY-MM-DD HH:MI:SS                                                                   |
| Direction          | A description of what steps are used to follow a recipe                                              | String                                                                                                  | 1000    | Any ASCII characters                                                                         |
| Email              | An email address                                                                                     | String                                                                                                  | 320     | Form of local@domain                                                                         |
| Emoji ID           | Unique identifier for an emoji using Unicode Standard format                                         | String                                                                                                  | 10      | Form is “U+” followed by 5 alphanumeric characters. For example, U+1F37B                     |
| Employee           | Information about the individual who works at Banter Ice Cream                                       | Employee ID + Employee Name + Role + Contact + 1:2{Location} + Banking Info ID + Username + Schedule ID | N/A     | N/A                                                                                          |
| Employee ID        | Unique identifier for an employee                                                                    | Integer                                                                                                 | 20      | system-generated sequential integer, beginning with 1                                        |
| Employee Name      | Name used to address an employee of Banter Ice Cream                                                 | String                                                                                                  | 128     | Any ASCII characters                                                                         |
| End Time           | The date and time that a shift ends.                                                                 | DateTime                                                                                                | 8 bytes | Format YYYY-MM-DD HH:MI:SS                                                                   |
| File               | An attached file of an allowed file type (pdf, video, or image)                                      | File                                                                                                    | 20 MB   | File format must be pdf, avi, mov, mp3, mp4, png, jpg, heic                                  |
| Ingredient         | Details of an ingredient used in a recipe                                                            | Ingredient ID + Name + Quantity + Units + Recipe ID                                                     | N/A     | N/A                                                                                          |
| Ingredient ID      | Unique identifier for an ingredient                                                                  | Integer                                                                                                 | 20      | system-generated sequential integer, beginning with 1                                        |
| Ingredient Name    | A term used to identify an ingredient                                                                | String                                                                                                  | 32      | Any ASCII characters                                                                         |
| Institution Number | A number representing the financial institution responsible for a given bank account                 | Integer                                                                                                 | 3       | Positive number                                                                              |
| isActive           | A true or false value that indicates if a recipe is currently served at a Banter Ice Cream location. | Boolean                                                                                                 | 1       | True, False                                                                                  |
| Location           | Name for a branch of Banter Ice Cream. Currently two possibilities, Abbotsford or Chilliwack.        | String                                                                                                  | 20      | Abbotsford, Chilliwack                                                                       |
| Message            | A message sent to one or employees at Banter Ice Cream.                                              | Message ID + Author + 1:n{Recipient} + Content + 0:5{File} + Timestamp                                  | N/A     | N/A                                                                                          |
| Message ID         | Unique identifier for a message                                                                      | Integer                                                                                                 | 20      | system-generated sequential integer, beginning with 1                                        |
| Password           | A secure text that allows access to an account                                                       | String                                                                                                  | 50      | Any ASCII characters                                                                         |
| Phone Number       | A phone number                                                                                       | Integer                                                                                                 | 10      | Positive number                                                                              |
| Transit Number     | A number representing the institution branch responsible for a given bank account                    | Integer                                                                                                 | 5       | Positive number                                                                              |
| Quantity           | The amount of an ingredient used in a recipe                                                         | Integer                                                                                                 | 2       | Positive number                                                                              |
| Reaction           | A non-textual response to an announcement by an employee using an emoji                              | Reaction ID + Emoji ID + Employee ID + DateTime                                                         | N/A     | N/A                                                                                          |
| Reaction ID        | Unique identifier for a reaction                                                                     | Integer                                                                                                 | 20      | system-generated sequential integer, beginning with 1                                        |
| Recipe             | Instructions on how to make an Ice Cream Flavour.                                                    | Recipe Name + Author + isActive + 0:n{Allergen} + 1:n{Ingredient} + 1:n{Direction}                      | N/A     | N/A                                                                                          |
| Recipient          | An employee who receives a message                                                                   | Employee ID                                                                                             | N/A     | N/A                                                                                          |
| Role               | The function that is required of a given employee or shift.                                          | String                                                                                                  | 20      | Manager, Front of House Staff, Kitchen Staff, Bookkeeper, Delivery Driver                    |
| Schedule           | The shifts currently assigned to an employee.                                                        | Employee ID  + 0:n{Shift ID} + Author                                                                   | N/A     | N/A                                                                                          |
| Shift              | An assigned time for an employee to work at a given Banter Ice Cream branch location.                | Shift ID + Start Time + End Time + Role + Location                                                      | N/A     | N/A                                                                                          |
| Shift ID           | Unique identifier for a shift                                                                        | Integer                                                                                                 | 20      | system-generated sequential integer, beginning with 1                                        |
| Start Time         | The date time that a shift begins.                                                                   | DateTime                                                                                                | 8 bytes | Format YYYY-MM-DD HH:MI:SS                                                                   |
| Timestamp          | The date and time that the object was created.                                                       | DateTime                                                                                                | 8 bytes | Format YYYY-MM-DD HH:MI:SS                                                                   |
| Units              | The units for a quantity                                                                             | String                                                                                                  | 20      | Standard baking units: cups, tablespoons, teaspoons, milliliters, liters, milligrams, grams  |
| User Account       | An account that an employee using to access the system                                               | User ID + Employee ID + Username + Password                                                             | N/A     | N/A                                                                                          |
| User ID            | Unique identifier for a user                                                                         | Integer                                                                                                 | 20      | system-generated sequential integer, beginning with 1                                        |
| Username           | Unique identifier for a user in the form of an email                                                 | String                                                                                                  | 320     | Form of local@domain                                                                         |
| View               | An employee who has viewed an announcement                                                           | Employee ID + Timestamp                                                                                 | N/A     | N/A                                                                                          |

The system shall have data entries as described by the data dictionary. The data dictionary has 5 columns. The first column, data element, provides an identifier for the type of data entry. The second column, description, describes in plain language, what the data entry will represent in the system. The third column, composition or data type, describes what data is included in the data entry. A composition has multiple data elements listed that make up one entry of that data element. Each data element listed is separated using a “+” sign. Some data elements may also have curly braces around them. In front of the curly braces there are numbers to represent the minimum and maximum number of the data element in curly braces that can be associated with each value saved of the data entry type, the form is "minimum number of the data element:maximum number of the data element". If the data element is not a composition it is a primitive, therefore it can be described by its data type. The fourth column, length, provides more context for a primitive data element’s data type in the form of a maximum length for the data type. The fifth column, values, provides more context for a primitive data element’s allowed values. 


## iii. Reports <a name="data-report"></a>
If your system will generate reports, then describe the attributes of those reports. You can detail the layout of the report.

## iv. Data Integrity <a name="data-integrity"></a>
Data acquisition, integrity, retention, and diposal If possible, describe how data is acquired, retained, and later on disposed. Describe the requirements for protecting the integrity of the data.

# 7 External Interface Requirements <a name="external-interfaces"></a>

## i. User Interfaces <a name="user-interfaces"></a>

Describe the logical characteristics of each interface between the software product and the users. This may include sample screen images, any GUI standards or product family style guides that are to be followed, screen layout constraints, standard buttons and functions (e.g., help) that will appear on every screen, keyboard shortcuts, error message display standards, and so on. Define the software components for which a user interface is needed.

## ii. Hardware Interfaces <a name="hardware-interfaces"></a>

Describe the logical and physical characteristics of each interface between the software product and the hardware components of the system. This may include the supported device types, the nature of the data and control interactions between the software and the hardware, and communication protocols to be used.

## iii. Software Interfaces <a name="software-interfaces"></a>

Describe the connections between this product and other specific software components (name and version), including databases, operating systems, tools, libraries, and integrated commercial components. Identify the data items or messages coming into the system and going out and describe the purpose of each. Describe the services needed and the nature of communications. Identify data that will be shared across software components.

## iv. Communication Interfaces <a name="communication-interfaces"></a>

Describe the requirements associated with any communications functions required by this product, including e-mail, web browser, network server communications protocols, electronic forms, and so on.

# 8 Software Quality Attributes <a name="quality-attributes"></a>

Sepcify requirements that include performance, security, reusability, maintainability, usability, availability, interoperability, etc.

# 9 Analysis Models <a name="analysis-models"></a>

# 10 Appendix <a name="appendix"></a>
