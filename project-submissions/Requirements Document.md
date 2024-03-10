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
| Team | January 30, 2024 | Review and edit sections | 1.8 |
| Team | January 31, 2024 | Further review and change formatting | 1.9 |
| Team | February 2, 2024 | Final Review | 2.0 |
| Amanda Anderson | February 8, 2024 | Add template for sections 5-10 | 3.0 |
| Team | February 10-13, 2024 | Update document according to feedback | 3.1 |
| Amanda Anderson | February 13, 2024 | Update template for sections 5, 6 | 4.0 |
| Team | February 18, 2024 | Add content to sections 5, 6, and 8 | 4.1 |
| Amanda Anderson | March 5, 2024 | Format sections 5, 9 | 5.0 |
| Team | March 10, 2024 | Add content to sections 5, 7, 9 | 5.1 |

# 1. **Overview** <a name="overview"></a>

This document will explore an opportunity to centralize Banter Ice Cream’s internal management. First, we will discuss Banter’s business requirements and illustrate the goal of the project. Second, the document will discuss the major features, scope, and limitations of the project. Third, more context for the project will be provided such as user classes, operating environment, and constraints. Fourth, will expand on each system feature to include description, priority, functional requirements, and use cases. Fifth, will define data requirements. Sixth, will describe external interface requirements including user interfaces, hardware interfaces, software interfaces, and communication interfaces. Seventh, will discuss software quality attributes that are prioritized in system. Eighth, will include further analysis models. Finally, there is an appendix for additional details.

These sections are outlined in the following Table of Contents.

## **Table of Contents**
1. [Overview](#overview)
2. [Business Requirements](#requirements)
   1. [Background](#background)
   2. [Business Opportunity](#opportunity)
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
      - [Description and Priority](#f1-description)
      - [Functional Requirements](#f1-functional)
      - [Use Cases](#f1-usecases)
      - [Storyboards](#f1-storyboards)
      - [Sequence Diagram for Create Schedule](#f1-sequence)
      - [Swimlane for Create Schedule](#f1-swimlane)
      - [State Diagram for Shift Swap](#f1-state)
   3. [Communication and Announcment](#feature-2)
      - [Description and Priority](#f2-description)
      - [Functional Requirements](#f2-functional)
      - [Use Cases](#f2-usecases)
      - [Storyboards](#f2-storyboards)
      - [Dialog Map for Send Message](#f2-dialogmap)
   5. [Recipe Management](#feature-3)
      - [Description and Priority](#f3-description)
      - [Functional Requirements](#f3-functional)
      - [Use Cases](#f3-usecases)
      - [Storyboards](#f3-storyboards)
      - [Sequence Diagram for Storyboard 3](#f3-sequence)
      - [Swimlane for View Recipe](#f3-swimlane)
   7. [Onboarding Materials](#feature-4)
      - [Description and Priority](#f4-description)
      - [Functional Requirements](#f4-functional)
      - [Use Cases](#f4-usecases)
      - [Storyboards](#f4-storyboards)
   9. [Account Management](#feature-5)
      - [Description and Priority](#f5-description)
      - [Functional Requirements](#f5-functional)
      - [Use Cases](#f5-usecases)
      - [Storyboards](#f5-storyboards)
      - [Dialog Map for Edit Account](#f5-dialogmap)
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
   1. [Data Flow Diagram Level 0](#data-flow0)
   2. [Data Flow Diagram Level 1](#data-flow1)
   3. [Data Flow Diagrams Level 2](#data-flow2)
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
   - Calendar views for employees and Managers to provide a clear overview of work schedules.
     
**Clock-In and Clock-Out System:**
   - Clock in at the start and clock out at the end of shifts, enabling precise tracking of work hours for all hourly employees.
   - Automatically tracks employee hours, including regular, overtime, sick days, and holidays.
   - Automatically calculate earnings, including overtime.
 
**Recipe Management System:**
   - A recipe management module that allows Managers to create, edit, and archive recipes, including full details and allergen information.
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
|  Banter | Banter Ice Cream, an ice cream shop with two locations; in Abbotsford, BC and Chilliwack, BC. [1]|
|  Client | Banter Ice Cream |
|  Business Hours | The hours that Banter Ice Cream is open. Monday-Thursday 1-9pm, Friday 1-10pm, Saturday 12-10pm, and Sunday 12-9pm (inclusive). [1]|
|  New Employee | An employee of Banter Ice Cream that has worked at Banter for less than two weeks. |
|  Employee | An employee of Banter Ice Cream with any role listed in User Classes and Characteristics section, unless otherwise specified. |
|  Staff | Unless otherwise specified, refers to an employee. |
|  Manager | Front of House / Kitchen Managers as defined in User Classes and Characteristics. |

## vi. **References** <a name="references"></a>

[1] “Find Us,” Banter Ice Cream, https://www.bantericecream.com/find-us (accessed Feb. 18, 2024). 

# 5 System Features <a name="system-features"></a>
 
## i. Scheduling and Time Tracking <a name="feature-1"></a>

Scheduling and Time Tracking

### a. Description and Priority <a name="f1-description"></a>
The scheduling feature has a high priority. This is a system employees will use multiple times during their shift as well as outside of work hours to check their schedule and clock in and out. The feature allows all staff to the view posted schedule, request shift swaps, and indicate availability. Managers must be able to create, edit and delete schedule information. Managers and bookkeepers should be able to see a summarized list of worked hours for each employee. 

### b. Functional Requirements <a name="f1-functional"></a>

SCH-1: The scheduler must allow managers to create shifts for employees.  

SCH-2: The scheduler must allow shifts to be made 2-4 weeks in advance.  

SCH-3: The scheduler must allow only managers to delete shifts from the schedule.  

SCH-4: The scheduler must allow only managers to edit the schedule.  

SCH-5: When a schedule is edited all employees with affected schedules must be updated. 

SCH-6: The scheduler must not allow the modification of any details of a shift after the shift is over. 

SCH-7: Each shift must have a unique identifier to identify specific shifts.  

SCH-8: Schedule information must be stored for 6 years due to Canadian laws regarding business tax documents.  

SCH-9: When a shift swap request is approved the schedule must update for each employee.  

SCH-10: The schedule must not allow employees to be scheduled during the time with indicated availability off. 

SCH-11: The schedulers option to view tracked hours by managers and bookkeepers must be shown correct information.  

SCH-12: The system must automatically summarize employees tracked hours.  

SCH-13: The system must have a clocking in option to allow employees to have their hours automatically recorded using their account details.  

SCH-14: The system must have a clocking out option to allow employees to stop their hours from being recorded using their account details.  

SCH-15: The system must allow employees to request shift swaps with other employees.  

SCH-16: The system must allow managers to approve requested shift swaps from employees.  

SCH-17: The system must allow managers to deny requested shift swaps from employees.  

SCH-18: The system must not allow shift swaps which cause an employee to be double booked.  

SCH-19: The systems view schedule option must display correct information including all shift swaps, deleted shifts, edited shifts and holidays.  


### c. Use cases associated with the feature or functional requirement <a name="f1-usecases"></a>
![image](https://github.com/Uvic-SENG321Spring2024/team8-developer/blob/main/diagrams/Schedulediagram.png)
Within the scheduling system there are 3 primary actors. Staff is the actor representing Front of House Staff, Kitchen Staff, and Delivery Drivers. The scheduling system should allow all employees to know when they are working, allow Managers to create and edit schedules, and allow Bookkeepers to pay employees. All use cases are written assuming the user is logged in.

| ID and Name | UC-1: Create Schedule |
| ----------- | ----------- |
| Created By: | Nolan |
| Date Created: | 02/15/24 |
| Primary Actor: | Front of House and Kitchen Manager |
| Description | The actor assigns each shift to employees for the next two weeks. |
| Trigger: | Actor opens create schedule functionality of software. |
| Preconditions: |<ul><li>PRE-1: Actor is logged in to system.</li></ul> <ul><li>PRE-2: There is at least one employee in the system who is available to take shifts.</li></ul>|
| Postconditions: |<ul><li>POST-1: Each assigned shift is associated with an employee.</li></ul>|
| Normal Flow: |<ol>**1.0 Create Schedule**<li>Actor selects an employee(see Exception 1.4)</li><li>Actor assigns one or more shifts to the selected employee within employee's listed availability(see Exception 1.1, 1.2, 1.3).</li><li>Actor continues, selecting one employee at a time until all shifts are assigned.</li><li>Actor saves schedule.</li><li> Actor exits schedule creation functionality of app.</li></ol> |
| Alternate Flows: |  |
| Exceptions: |<ol>**1.1 Create Schedule Employee Availability Conflict**<li>Actor selects an employee.</li><li> If employee does not have listed availability, no shifts are assigned to them. </li><li>Actor moves on to step 3 of primary flow.</li></ol><ol>**1.2 Create Schedule Employee Hour Conflict**<li>Actor selects an employee.</li><li> If employee is working a maximum number of hours, no additional shifts are assigned to them. </li><li>Actor moves on to step 3 of primary flow.</li></ol><ol>**1.3 Create Schedule No Assigned Shifts For Employee**<li>Actor selects an employee.</li><li> Actor does not assign any shifts to the selected employee.</li><li>Actor moves on to step 3 of primary flow.</li></ol><ol>**1.4 Create Schedule Previous Selected Employee**<li>Actor selects an employee that was previously selected.</li><li> Actor assigns an additional one or more shifts to the selected employee.</li><li>Actor moves on to step 3 of primary flow.</li></ol>|
| Assumptions: | User is logged in |
| Priority: | High |
| Frequency of Use: | Every two weeks |
| Business Rules: | There are a maximum number of hours that each person is allowed to work, both per day and per week. |
| Other Information: |  |

**User Story 1: Approve Swap**

As a Manager I want to approve shift swap requests so that upon employee request shifts are swapped between the two employees.

**Acceptance Criteria:**

Given a Manager has approved a shift swap request then the shift being swapped for each employee must be switched.

**User Story 2: Create Schedule**

As a Manager I want to create a schedule for a 2 week period at one store location so that each employee knows when they are working.

**Acceptance Criteria:**

Given the schedule is made, when the schedule is viewed by employees, then the schedule shall be shown to the employee with correct information such as employees working, shifts, hours, and location.

**User Story 3: Edit Schedule**

As a Manager I want to edit an already made schedule to update, remove or add shifts so that the schedule is correct with any new information.

**Acceptance Criteria:**

Given the schedule is updated, when employees view the schedule, then the updated schedule should be shown with all alterations.

**User Story 4: Indicate Availability**

As a Staff member when I Indicate availability, I want to notify the managers that I cannot work during that period so that I am only working during that time.

**Acceptance Criteria:**

Given availability is indicated, when the schedule is posted the availability which was indicated should be the only time with scheduled shifts.

**User Story 5: View tracked hours**

As a Bookkeeper or Manager, I want to view the worked hours for each employee so that I can accurately pay them for their worked hours.

**Acceptance Criteria:**

When tracked hours for an employee are viewed then a summary of all worked hours including overtime and statutory holidays and vacations should be displayed.

**User Story 6: Clock in**

As a staff member I want to clock in at work so that the hours I work are accurately recorded in the system.

**Acceptance Criteria:**

Given I have clocked in, when my tracked hours are viewed then the hours I have worked should accurately be accurately recorded for that day.

**User Story 7: Clock out**

As an Staff member I want to clock out so that the hours I work are accurately recorded in the system.

**Acceptance Criteria:**

Given I have clocked out, when my tracked hours are viewed then the hours I have worked should accurately be accurately recorded for that day.

**User Story 8: Swap shift request**

As a Staff member I want to request a shift swap with another employee with the same role and upon acceptance create a shift swap request which needs to be approved.

**Acceptance Criteria:**

Given an employee has requested a shift swap with another employee, when another employee has accepted, then a shift swap request should be posted awaiting approval.

**User Story 9: View schedule**

As a Staff member I want to view the posted schedule for the current work weeks as well as the next 2 weeks so that I can view the correct information of what shift I am working.

**Acceptance Criteria:**

Given an employee selects to view the schedule they should be shown the up to date schedule with correct information for the current shift period as well as the next. 

**User Story 10: View all schedules**

As a Staff member I want to be able to view my personal schedule and the schedule of all employees. I want to be able to view the schedule in a weekly format and a monthly format so I can view the correct information in an easy to read format so that I know what shift I am working and what shifts everyone is working to allow for shift swap requests.

**Acceptance Criteria:**

Given an employee selects to view the schedule they should be shown the up to date schedule in their chosen format with correct information of all employees for the shift period.

### d. Storyboards <a name="f1-storyboards"></a>

### e. Sequence Diagram for Create Schedule <a name="f1-sequence"></a>

### f. Swimlane Diagram for Create Schedule <a name="f1-swimlane"></a>

### g. State Diagram for Swap Shifts <a name="f1-state"></a>


## ii. Communication and Announcement <a name="feature-2"></a>

Communication and Announcement feature allows sending and receiving messages and company-wide announcements.

### a. Description and Priority <a name="f2-description"></a>

The Communication and Announcement and announcement feature is a high priority feature in the system. This is because all staffs must receive notifications of new announcements, and be able to view the announcements to be aware of any major changes in the company. It is also important that all staff can send and receive messages to any staff member or staff messaging group. 

### b. Functional Requirements <a name="f2-functional"></a>

COM-1: The system must allow embedding capabilities for images, videos, and PDFs in announcements and messages to enchance communication.

COM-2: The system must provide the ability to send and receive company-wide announcements and communicate about shift changes.

COM-3: The system must have role-based access control, providing different access levels for different user roles. Managers must have access to create, edit, and remove announcements, while all other staff must have access to view announcements.

COM-4: The system must safeguard sensitive information such as chat logs and announcement management, through controlled access, ensuring privacy and security across the system.

COM-5: The system must provide tailored interfaces and features depending on the staff’s role within the company, ensuring that managers have access to announcement creation and management features, while all other staff have access to communication channels for group or individual messaging.


### c. Use cases associated with the feature or functional requirement <a name="f2-usecases"></a>

![Communication   Announcement UseCase Diagram](https://github.com/Uvic-SENG321Spring2024/team8-developer/assets/145606952/da994ce0-76ad-406c-a44e-7def4ecdd0d9)

Within the Communication and Announcement feature there are two primary actors, "Managers", and "All Staff". Managers have the ability to create, edit, and send company-wide announcements, while all staff can view these announcements and react to them. All Staff including the manager, can send messages to individuals or groups, view received messages, and edit messages they have sent. The system must allow embedding capabilities for images, videos, and PDFs in announcements and messages, provide role-based access control, safeguard sensitive information, and tailor interfaces and features based on user roles, ensuring effective communication and announcement management within the company. 

**User Story 1: Send message**

As an employee, I want to be able to send a message to another staff member or a group of coworkers, so that I can communicate information effectively. 

**Acceptance Criteria:** 

The system must allow all staff to be able to send messages to one or more people from the list of staff members. 

**User Story 2: View message**

As an employee, I want to be able to view the messages that are sent to me or the message group that I am part of, so that I can stay informed about communication within the company.  

**Acceptance Criteria:** 

The system must allow each staff member to see recieved messages.

**User Story 3: Edit message**

As an employee, I want to be able to edit a message that I have previously sent, so that I can make clarifications or update the message as required. 

**Acceptance Criteria:** 

The system must allow each staff member to be able to edit messages that the staff member had sent before. 

**User Story 5: React announcements** 

As an employee, I want to be able to react to company-wide announcements, so that I can share my opinion or acknowledge the content. 

**Acceptance Criteria:** 

The system must allow all staff to be able to react to announcements with emojis. 

**User Story 6: View announcements** 

As an employee, I want to be able to view all company-wide announcements, so that I can stay updated on the important changes and news within the company. 

**Acceptance Criteria:** 

The system must allow all staff to be able to view all announcements. Must be able to find the most recent announcement within 2 seconds. 

**User Story 7: View announcement information**

As a manager, I want to be able to view detailed information of any and every announcement, so that I can see information such as the information about how many people have viewed the announcements and who have viewed the announcements. 

**Acceptance Criteria:** 

The system must allow the manager, to be able to view all of the announcement's related information such as the creation date, information about who has viewed the announcement, and who has reacted. 

**User Story 8: Send announcements**

As a manager, I want to be able to send company-wide announcements to all staff members, so that I can share important information effectively. 

**Acceptance Criteria:** 

The system must allow the manager, to create and send company-wide announcements using text, images, videos, or PDF. 

**User Story 9: Edit announcements** 

As a manager, I want to be able to edit or update announcements that I have already sent, so that I can update information where necessary. 

**Acceptance Criteria:** 

The system must allow the manager to be able to access and edit announcements that have been sent. 

### d. Storyboards <a name="f2-storyboards"></a>

### e. Dialog Map for Send Message <a name="f2-dialogmap"></a>


## iii. Recipe Management <a name="feature-3"></a>

### a. Description and Priority <a name="f3-description"></a>
The Recipe Management feature has a high priority in the application. An Authenticated Manager, Kitchen Staff, or Front of House Staff must be able to view active or unactive recipes. Managers and Kitchen Staff must be able to view the full recipe including the ingredient list, preparation instructions, and allergens. Front of House Staff must only be able to view the allergens in a recipe. Managers are the only ones who are able to create, edit, archive and unarchive recipes. Expect a high frequency of use, Kitchen Staff and Front of House Staff will use this feature daily when making the ice cream and serving customers as the Front of House Staff are required to inform customers of any allergens in the ice cream. 

### b. Functional Requirements <a name="f3-functional"></a>

RMS-1: Kitchen Staff, Front of House Staff and Managers must be able to view active and inactive recipes. 

RMS-2: Managers and Kitchen Staff must be able to view the full recipe including ingredents list, preparation instructions, and allergens.

RMS-3: Front of House Staff must be only able to view the allergens of a recipe.

RMS-4: Managers must be able to create new recipes with details such as name, ingredients, preparation instructions and allergen information.

RMS-5: Managers must be able to edit existing recipes, including changing details, adding or removing ingredients, and updating allergen information.

RMS-6: Managers must be able to archive a recipe, changing its status to inactive, and be able to unarchive a recipe, changing its status to active.

RMS-7: The system must be able to display different recipe views based on the access of the user's role.

&emsp;&emsp;RMS-7.1: The system must have a detailed recipe view which contains name, list of ingredients, preparation instructions, and allergens.

&emsp;&emsp;RMS-7.2: The system must have a limited recipe view which only contains the name, and allergens.

RMS-8: The system must be able to archive recipes, removing it from the list of active recipes and adds it to the list of inactive recipes.

RMS-9: The system must be able to unarchive recipes, removing it from the list of inactive recipes and adds it to the list of active recipes.

RMS-10: The system must display a prompt the user to save when they exit editing mode if they didn't already save.

RMS-11: The system must display a prompt to the user to save when they exit creation mode if they didn't already save.

RMS-12: The system must provide an edit option for each recipe.

RMS-13: The system must implement a save option to confirm changes. 

RMS-14: The system must allow managers to exit editing mode.

RMS-15: The system must display an empty template with sections for name, ingredients, preparation instructions, and allergen information when creating a recipe.

RMS-16: The system must allow managers to enter text in each section.

RMS-17: The system must provide a save option for new recipes.

RMS-18: The system must ensure newly created recipes are visible in the list of recipes.

RMS-19: The system must allow managers to exit creation mode.

RMS-20: The system must allow managers to select specific recipes for archiving or unarchiving.

RMS-21: The system must have different access levels for Managers, Kitchen Staff, and Front of House Staff.

RMS-22: The system must display meaningful error messages to users in case of unsuccessful operations or system errors.


### c. Use cases associated with the feature or functional requirement <a name="f3-usecases"></a>

![RMS Usecase Diagram](https://github.com/Uvic-SENG321Spring2024/team8-developer/blob/main/diagrams/RMS-Usecase-Diagram-V4.png)

Within the recipe management system there are 3 primary actors, "Managers", "Kitchen Staff", and "Front of House Staff". The recipe management system allows Managers to "Edit Recipe", "Create Recipe", "Archive Recipe", and "View Recipe". The extends from "Archive Recipe" to "Unarchive Recipe" represent an alternate flow. If the recipe has an active status it will be able to be archived, but if the recipe has an inactive status it will be able to be unarchived. The "Front of House Staff" can only "View Limited Recipe" which includes a display of the allergen information. The extends from "View Recipe" to "View Limited Recipe" represents this as an alternate flow of the "View Recipe" usecase (see UC-2 Alternate Flow 2.1). The "Managers" and "Kitchen Staff" are the only users that can "View Detailed Recipe" which includes a display of the ingredents list, preparation instructions, and Allergens. The extends from "View Recipe" to "View Detailed Recipe" represents this as th normal flow of the "View Recipe" usecase (see UC-2 Normal Flow 2.0).

| ID and Name | UC-2 View Recipe |
| ----------- | ----------- |
| Created By: | Nolan, Justin |
| Date Created: | 02/14/24 |
| Primary Actor: | Kitchen Staff, Managers, Front of House Staff |
| Description | The Actor selects a recipe from the list of all possible recipes. The system displays a view of the recipe based on the actors level of access. |
| Trigger: | Actor selects recipe to open. |
| Preconditions: | <ul><li>PRE-1: User is logged in.</li><li>PRE-2: User is authenticated.</li></ul> |
| Postconditions: | <ul><li>POST-1: Recipe is displayed.</li></ul> |
| Normal Flow: | <ol>**2.0 View Detailed Recipe**<li>Kitchen Staff or Manager selects the recipe menu option.</li><li>Select active or inactive recipes to view.</li><li>Select desired recipe from list.</li><li>System displays the detailed recipe view.</li></ol> |
| Alternate Flows: | <ol>**2.1 View Limited Recipe**<li>Front of House Staff selects the recipe menu option.</li><li>Select active or inactive recipes to view.</li><li>Select desired recipe from list.</li><li>System displays the limited recipe view.</li></ol> |
| Exceptions: |  |
| Priority: | High |
| Frequency of Use: | 10 times per day by the Kitchen Staff, 1 time per day by Managers, 20 times per day by Front of House Staff. |
| Business Rules: | Must alert all customers of potential allergens. Only authorized ingredients may be in the ice cream. |
| Other Information: | RSM-2, RSM-3, RSM-7 |
| Assumptions: | Recipe already exists in the system. |

**User Story 1: Edit Recipe**

As an authenticated Manager, I want exclusive rights to edit existing recipes, so that I can change recipe details, add or remove ingredients, and update allergen information.

**Acceptance Criteria:**

There is an option to edit available on each recipe in the user interface. Upon selecting the option, I can choose the specific section of the recipe I want to edit. I can save the changes after editing and the system confirms the changes have been saved. The system should not save any changes if I exit the editing page, if I try to exit without saving the system should prompt me to save my changes. I can exit the viewing mode at any time.  

**User Story 2: Create Recipe**

As an authenticated Manager, I want exclusive rights to create new recipes, so that I can create new recipes with details such as name, ingredients, preparation instructions and allergen information.

**Acceptance Criteria:**

There is an option to create a new recipe in the user interface. After selceting that feature I should see an empty template for a recipe which contains a section for name, ingrediants, preparation instructions and allergen information. I should be able to enter text in each section. I should be able to save my work. The new recipe should be viewable on the list of recipes. I should be able to exit creation mode. 

**User Story 3: Archive Recipe**

As an authenticated Manager, I want exclusive rights to archive recipes, so that I can change the status of a recipe from active to inactive and change the status from inactive to active. 

**Acceptance Criteria:**

There is an option to archive recipes if the status is active and an option to unarchive recipes if the status is inactive in the user interface. Upon selecting that option I should be able to select which recipes I want to archive or unarchive. The recipe should be added to the inactive recipe list, if the status was active, and the recipe should be removed from the active recipe list. The recipe should be added to the active recipe lists, if the status was inactive, and the recipe should be removed from the inactive recipe list.  

### d. Storyboards <a name="f3-storyboards"></a>

#### Storyboard 1: UC-2 Normal Flow

![UC-2 Normal flow](https://github.com/Uvic-SENG321Spring2024/team8-developer/blob/main/Prototype%20Images/Storyboard2.png)

#### Storyboard 2: UC-2 Alternate Flow

![UC-2 Alternate flow](https://github.com/Uvic-SENG321Spring2024/team8-developer/blob/main/Prototype%20Images/Storyboard1.png)

#### Storyboard 3: Edit, Create, and Archive Recipe

![Create and Edit](https://github.com/Uvic-SENG321Spring2024/team8-developer/blob/main/Prototype%20Images/Storyboard3.png)

### e. Sequence Diagram for Storyboard 3 <a name="f3-sequence"></a>

![Sequence Diagram SB3](https://github.com/Uvic-SENG321Spring2024/team8-developer/blob/main/diagrams/RMS-Create%3AEdit-SequenceDiagram.png)

This sequence diagram shows the process of a Manager interatcing with the system to create, edit and manage recipes. The Manager starts by selecting the recipe menu icon, leading to the list of active recipes. The Manager then selects the create new recipe icon (plus symbol), leading to the display of a blank recipe template. The Manager proceeds to fill in various details such as the name, upload an image, provide a description, set the active status, input ingredients, and provide preparation instructions. After filling in those details, the Manager selects the back arrow, triggering a save verification window. Upon confirmation, the system check the recipe status and adds the newly created recipe to the top of the active recipe list. The Manager then interacts with the system to view the updated active recipe list and selects the new recipe for detailed information. The sequence concludes with the Manager entering edit mode, adding allergens to the recipe in the allergens section, and saving the changes, resulting in an updated active recipe list.  

### f. Swimlane Diagram for View Recipe <a name="f3-swimlane"></a>

![Swimlane UC-2](https://github.com/Uvic-SENG321Spring2024/team8-developer/blob/main/Prototype%20Images/Swimlane.png)

This swimlane diagram shows how a Manager, Front of House Staff, and Kitchen Staff interacts with the system when viewing a recipe. This diagram relates to UC-2 and covers the normal and alternate flows. All three lanes start the same way by selecting the recipe menu option. The Manager and Kitchen Staff lanes interact with the system in the same way and represts the normal flow of UC-2. After the Manager/Kitchen Staff selects the recipe menu option they then select whether they want to view active or inactive recipes. If active is selected the system displays the active recipe list, otherwise the system displays the incative recipe list. The Manager/Kitchen Staff then selects the desired recipe to view, resulting in the system displaying the detailed recipe. The Front of House Staff lane interacts with the system lane to represent the alternate flow of UC-2. After the Front of House Staff selects the recipe menu option they then select whether they want to view active or inactive recipes. If active is selected the system displays the active recipe list, otherwise the system displays the incative recipe list. The Front of House Staff then selects the desired recipe to view, resulting in the system displaying the limited recipe. 

## iv. Onboarding Materials <a name="feature-4"></a>

This feature describes the different levels of access different employees have to onboarding materials such as instructional videos.

### a. Description and Priority <a name="f4-description"></a>
The Onboarding Materials feature has a low priority in the application. An authenticated employee (except delivery drivers) must be able to view the onboarding materials but only the managers have the right to edit the materials such as add or remove materials. Overall we expect a low frequency of use. New employees will need to become familiar with onboarding material and may access material multiple times a day for the first two weeks of employment. However, we expect established employees will only access a material to reference it once each month.

### b. Functional Requirements <a name="f4-functional"></a>
ONB-1:  An authenticated employee (except delivery drivers) must be able to view the onboarding materials at any time.

ONB-2: The managers must be the only staff to edit the onboarding materials at any time.

ONB-3: The managers must be the only staff to create the onboarding materials at any time.

ONB-4: The managers must be the only staff to remove the onboarding materials at any time.

### c. Use cases associated with the feature or functional requirement <a name="f4-usecases"></a>
![Onboarding Material](https://github.com/Uvic-SENG321Spring2024/team8-developer/assets/105994651/8cccab7f-7c44-4d1a-94cb-da9e5a177b9d)

Within the framework of the onboarding material use case diagram, there exist two distinct actors. The primary actor, referred to as the "Manager," possesses comprehensive permissions, encompassing the ability to view, edit, create, and remove onboarding materials. The secondary actor, designated as the "Staff," is subdivided into specific roles, namely the Bookkeeper, Front of House Staff, and Kitchen Staff, with their access limited solely to viewing onboarding materials.

 **User Story 1: View Onboarding Materials**
 
As an authenticated employee (excluding delivery drivers), I want to be able to view the onboarding materials at any time, so that I can access the necessary information for onboarding purposes.

**Acceptance Criteria:**

There is an option 'View Onboarding Materials' available in the user interface.
Upon selecting the option, I can choose the specific onboarding materials I wish to view.
The selected onboarding materials are displayed to me.
I can exit the viewing mode when I'm done.


**User Story 2: Edit Onboarding Materials**

As an authenticated manager, I want to have exclusive rights to edit the onboarding materials, so that I can ensure the content is up-to-date and relevant for the employees.

**Acceptance Criteria:**

There is an option 'Edit Onboarding Materials' available in the user interface.
Upon selecting the option, I can choose the specific onboarding materials I want to edit.
I have the ability to make changes to the selected onboarding materials.
After editing, I can save the changes, and the system confirms that the changes have been successfully saved.
I can exit the editing mode when I'm done.

**User Story 3: Create Onboarding Material**

As an authenticated content manager, I want the capability to create new onboarding materials, so that I can provide updated and relevant content for employee onboarding.

**Acceptance Criteria:**

There is an option 'Create Onboarding Material' available in the user interface.
Upon selecting the option, I am prompted to input the necessary details for the new onboarding material, such as title, content, and any relevant metadata.
After entering the information, I can save the new onboarding material, and the system confirms its successful creation.
The newly created onboarding material is accessible in the system for other authorized users to view.
I can exit the creation mode when I'm done.

**User Story 4: Remove Onboarding Material**

As an authenticated manager, I want the exclusive authority to remove outdated or irrelevant onboarding materials, so that I can maintain the integrity and relevance of the onboarding content.

**Acceptance Criteria:**

There is an option 'Remove Onboarding Material' available in the user interface.
Upon selecting the option, I can choose the specific onboarding material I wish to remove.
The system prompts for confirmation before proceeding with the removal to prevent accidental deletions.
Upon confirmation, the selected onboarding material is removed from the system, and the system confirms the successful removal.
The removed onboarding material is no longer accessible to users in the system.
I can exit the removal mode when I'm done.

### d. Storyboards <a name="f4-storyboards"></a>



## v. Account Management <a name="feature-5"></a>

### a. Description and Priority <a name="f5-description"></a>
The Account Management feature has a high priority in the system.  It allows authenticated Managers to manage access to the system by creating and deleting accounts.  An authenticated user must be able to edit their important information to ensure it is correct, and must be able to log in and log out of their account.  This feature is expected to be used 100+ times per day due to the high frequency of logging in and logging out.

### b. Functional Requirements <a name="f5-functional"></a>

ACC-1: The system must provide Managers with the capability to delete user accounts that are no longer active within the company.

ACC-2: The system must allow Managers to create new user accounts by entering their username and role, granting them access to the system.

ACC-3: The system must allow Managers to view a users role, contact information, and username.

ACC-4: The sytem must allow Managers to edit a users role, and username

ACC-5: The system must allow users to edit their payment information, contact information, and password.

ACC-6: The system must allow users to log in to their accounts with their username and password.

ACC-7: The system must allow users to log out of their accounts.

ACC-8: The system must allow users to view their account information to ensure its accuracy and completeness.

ACC-9: The system must automatically log out users once they close the application.



### c. Use cases associated with the feature or functional requirement <a name="f5-usecases"></a>

![RMS Usecase Diagram](https://github.com/Uvic-SENG321Spring2024/team8-developer/blob/rd-5.V-account/diagrams/accounts.png)


**User Story 1: Delete Account**

As a Manager I want to delete an account so that I can remove any users that no longer work for my company from the system.

**Acceptance Criteria:**

There is an option for Managers to "Delete" an account.  This feature must remove a users access to the system, yet still retain information about their employment for legal and tax purposes.

**User Story 2: Create Account**

As a Manager I want to create an account so that my newly hired employees have access to the system.

**Acceptance Criteria:**

There is an option for a Manager to "Create" an account. After selecting this the Manager will be prompted to set the employee's role and username. This will then allow the employee to log in and set their password and payment information. 

**User Story 3: View Account Information**

As a Manager I want to view a users account information so that I can see their role and contact information.

**Acceptance Criteria:**

There is an option for a Manager to "View Account Informaton" for any selected employee. It will show their username, role, and contact information.

**User Story 4: Manage Account**

As a Manager I want to change a users role or username in order to ensure it stays up to date.

**Acceptance Criteria:**

There is an option for a Manager to "Manage Account" for any employee. It will allow them to edit a users username and role.  These changes must be reflected in the "View Account Information" use case, and the "Log In" use case.

**User Story 5: View Account Information**

As a user I want to view my account information so I can ensure it is all correct.

**Acceptance Criteria:**

There is an option for a user to "View Account Informaton" for themselves. It will show their username, role, contact information, and payment information.

**User Story 6: Edit Account Information**

As a user I want to edit my account information so I can keep my payment information, contact information, and password up to date. These changes must be reflected in the "View Account Information" use case, and the "Log In" use case.

**Acceptance Criteria:**

A user must have an option to "Edit Account Information" for themselves.  This will allow them to change their password, contact information, and payment information. These changes must be reflected in the "View Account Information" use case, and the "Log In" use case.

**User Story 7: Log In**

As a user I want to log in to my account so I can use the system.

**Acceptance Criteria:**

When a user opens the app they will have an option to "Log In" to their account.  They will be prompted to enter their account username and password.  If username and password are valid then they will be granted access to the system.

**User Story 8: Log Out**

As a user I want to log out of my account so I can ensure no one else can use my account.

**Acceptance Criteria:**

A user must have the option to "Log Out" of their account.  This will remove their access to the system until they "Log In" again. The system must automatically "Log Out" a user once they have closed the application.

### d. Storyboards <a name="f5-storyboards"></a>

### e. Dialog Map for Edit Account <a name="f5-dialogmap"></a>


# 6 Data Requirements <a name="data-requirements"></a>

## i. Logical Data Models <a name="data-model"></a>

![Entity Relationship Diagram - Ben6](https://github.com/Uvic-SENG321Spring2024/team8-developer/assets/76890860/55803d9e-2210-42c8-a900-ba137dd72789)

![UML Diagram - My Diagram (1)](https://github.com/Uvic-SENG321Spring2024/team8-developer/assets/76890860/f0cb66f4-f0bb-48d3-8bf2-adab13170f3f)

The Entity Relationship Diagram (ERD) and the UML Class Diagram serve as visual tools to represent the data structure and relationships within the Banter Ice Cream System. The purpose of these diagrams is to articulate how various data entities within the system interact and relate to each other, which is essential for understanding the flow of information and the underlying structure of the system’s data.

### Diagrams Explanation

1. **Employee to User Account:**
   - **Relationship Name:** "Operates"
   - **Relationship Type:** One-to-One
   - **Description:** Each Employee operates a single User Account to access the system. It can be read as "A User Account is operated by an Employee" or "An Employee operates a User Account."

2. **Employee to Banking Information:**
   - **Relationship Name:** "Has"
   - **Relationship Type:** One-to-One
   - **Description:** Each Employee has specific Banking Information for payroll purposes. It can be interpreted as "Banking Information is held by an Employee" or "An Employee has Banking Information."

3. **Employee to Shift:**
   - **Relationship Name:** "Assigned To"
   - **Relationship Type:** One-to-Many
   - **Description:** An employee can be assigned to many shifts, but each shift is assigned to one employee. It can be read as "A Shift is assigned to an Employee" or "An Employee is assigned to a Shift."

4. **Employee to Schedule:**
   - **Relationship Name:** "Follows"
   - **Relationship Type:** One-to-One
   - **Description:** Each employee follows one schedule, and each schedule is followed by one employee. It can be interpreted as "A Schedule is followed by an Employee" or "An Employee follows a Schedule."

5. **Schedule to Shift:**
   - **Relationship Name:** "Includes"
   - **Relationship Type:** One-to-Many
   - **Description:** A Schedule includes multiple Shifts. It can be interpreted as "A Schedule includes Shifts" or "Shifts are included in a Schedule."

6. **Employee to Message:**
   - **Relationship Name:** "Creates"
   - **Relationship Type:** One-to-Many
   - **Description:** An Employee creates multiple Messages. It can be read as "A Message is created by an Employee" or "An Employee creates Messages."

7. **Employee to Announcements:**
   - **Relationship Name:** "Authors"
   - **Relationship Type:** One-to-Many
   - **Description:** An employee authors multiple Announcements. It can be interpreted as "An Announcement is authored by an Employee" or "An Employee authors Announcements."

8. **Employee to Recipe:**
   - **Relationship Name:** "Develops"
   - **Relationship Type:** One-to-Many
   - **Description:** An employee develops multiple recipes. It can be read as "A Recipe is developed by an Employee" or "An Employee develops Recipes."

9. **Recipe to Ingredients:**
   - **Relationship Name:** "Consists of"
   - **Relationship Type:** Many-to-Many
   - **Description:** A recipe consists of multiple ingredients, and each Ingredient can be part of multiple Recipes. It can be read as "A Recipe consists of Ingredients" or "Ingredients are part of a Recipe."

10. **Ingredients to Allergens:**
    - **Relationship Name:** "Contains"
    - **Relationship Type:** Many-to-Many
    - **Description:** Ingredients may contain multiple allergens, and each allergen may be found in multiple ingredients. It can be interpreted as "An Ingredient contains Allergens" or "Allergens are contained in an Ingredient."

11. **Announcement to Reaction:**
    - **Relationship Name:** "Generates" or "Receives"
    - **Relationship Type:** One-to-Many
    - **Description:** This relationship indicates that an Announcement generates multiple Reactions or receives multiple Reactions from users. It can be read as "An Announcement generates Reactions" or "Reactions are received by an Announcement."

12. **Announcement to View:**
    - **Relationship Name:** "Attracts" or "Accumulates"
    - **Relationship Type:** One-to-Many
    - **Description:** This relationship shows that an Announcement attracts multiple Views or accumulates multiple Views over time. It can be interpreted as "An Announcement attracts Views" or "Views are accumulated by an Announcement."


## ii. Data Dictionary <a name="data-dictionary"></a>

| Data Element       | Description                                                                                          | Composition or Data Type                                                                                | Length  | Values                                                                                       |
|--------------------|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------------------|
| Account Number     | Unique number representing a personal bank account                                                   | Integer                                                                                                 | 12      | Positive numbers                                                                             |
| Allergen           | Details of an allergen found in an ingredient in a recipe                                            | Allergen ID <br>+ Allergen Name <br>+ Recipe ID                                                                 | N/A     | N/A                                                                                          |
| Allergen ID        | Unique number representing a personal bank account                                                   | Integer                                                                                                 | 12      | System-generated sequential integer, beginning with 1                                        |
| Allergen Name      | The name of a food that according to government of Canada commonly causes an allergic reaction       | String                                                                                                  | 128     | Any ASCII characters                                                                         |
| Announcement       | A message sent out to all employees of Banter Ice Cream                                              | Announcement ID <br>+ Author <br>+ Content <br>+ 0:5{File} <br>+ 0:n{Reaction} <br>+ 0:n{View} <br>+ Date Posted                | N/A     | N/A                                                                                          |
| Announcement ID    | Unique identifier for an announcement                                                                | Integer                                                                                                 | 12      | System-generated sequential integer, beginning with 1                                        |
| Author             | Key to employee who is responsible for creating the object (Announcement, Message, Recipe, Schedule) | Employee ID                                                                                             | N/A     | N/A                                                                                          |
| Banking Info       | Information about an employee’s bank account, such that the bookkeeper can pay the employee.         | Bank Info ID <br>+ Employee ID <br>+ Transit Number <br>+ Institution Number <br>+ Account Number                       | N/A     | N/A                                                                                          |
| Bank Info ID       | Unique identifier for stored bank account information                                                | Integer                                                                                                 | 10      | System-generated sequential integer, beginning with 1                                        |
| Contact            | Information used to contact an employee.                                                             | Email <br>+ Phone Number                                                                                    | 320     | Form of local@domain                                                                         |
| Content            | The text contents of a message or announcement object                                                | String                                                                                                  | 10000   | Any ASCII characters                                                                         |
| Date Posted        | The date and time that an announcement is sent to the system                                         | DateTime                                                                                                | 8 bytes | Format YYYY-MM-DD HH:MI:SS                                                                   |
| DateTime           | The date and time that a reaction occurs                                                             | DateTime                                                                                                | 8 bytes | Format YYYY-MM-DD HH:MI:SS                                                                   |
| Direction          | A description of what steps are used to follow a recipe                                              | String                                                                                                  | 1000    | Any ASCII characters                                                                         |
| Email              | An email address                                                                                     | String                                                                                                  | 320     | Form of local@domain                                                                         |
| Emoji ID           | Unique identifier for an emoji using Unicode Standard format                                         | String                                                                                                  | 10      | Form is “U+” followed by 5 alphanumeric characters. For example, U+1F37B                     |
| Employee           | Information about the individual who works at Banter Ice Cream                                       | Employee ID <br>+ Employee Name <br>+ Role <br>+ Contact <br>+ 1:2{Location} <br>+ Banking Info ID <br>+ Username <br>+ Schedule ID | N/A     | N/A                                                                                          |
| Employee ID        | Unique identifier for an employee                                                                    | Integer                                                                                                 | 20      | System-generated sequential integer, beginning with 1                                        |
| Employee Name      | Name used to address an employee of Banter Ice Cream                                                 | String                                                                                                  | 128     | Any ASCII characters                                                                         |
| End Time           | The date and time that a shift ends.                                                                 | DateTime                                                                                                | 8 bytes | Format YYYY-MM-DD HH:MI:SS                                                                   |
| File               | An attached file of an allowed file type (pdf, video, or image)                                      | File                                                                                                    | 20 MB   | File format must be pdf, avi, mov, mp3, mp4, png, jpg, heic                                  |
| Ingredient         | Details of an ingredient used in a recipe                                                            | Ingredient ID <br>+ Name <br>+ Quantity <br>+ Units <br>+ Recipe ID                                                     | N/A     | N/A                                                                                          |
| Ingredient ID      | Unique identifier for an ingredient                                                                  | Integer                                                                                                 | 20      | System-generated sequential integer, beginning with 1                                        |
| Ingredient Name    | A term used to identify an ingredient                                                                | String                                                                                                  | 32      | Any ASCII characters                                                                         |
| Institution Number | A number representing the financial institution responsible for a given bank account                 | Integer                                                                                                 | 3       | Positive number                                                                              |
| isActive           | A true or false value that indicates if a recipe is currently served at a Banter Ice Cream location. | Boolean                                                                                                 | 1       | True, False                                                                                  |
| Location           | Name for a branch of Banter Ice Cream. Currently two possibilities, Abbotsford or Chilliwack.        | String                                                                                                  | 20      | Abbotsford, Chilliwack                                                                       |
| Message            | A message sent to one or employees at Banter Ice Cream.                                              | Message ID <br>+ Author <br>+ 1:n{Recipient} <br>+ Content <br>+ 0:5{File} <br>+ Timestamp                                  | N/A     | N/A                                                                                          |
| Message ID         | Unique identifier for a message                                                                      | Integer                                                                                                 | 20      | System-generated sequential integer, beginning with 1                                        |
| Password           | A secure text that allows access to an account                                                       | String                                                                                                  | 50      | Any ASCII characters                                                                         |
| Phone Number       | A phone number                                                                                       | Integer                                                                                                 | 10      | Positive number                                                                              |
| Transit Number     | A number representing the institution branch responsible for a given bank account                    | Integer                                                                                                 | 5       | Positive number                                                                              |
| Quantity           | The amount of an ingredient used in a recipe                                                         | Integer                                                                                                 | 2       | Positive number                                                                              |
| Reaction           | A non-textual response to an announcement by an employee using an emoji                              | Reaction ID <br>+ Emoji ID <br>+ Employee ID <br>+ DateTime                                                         | N/A     | N/A                                                                                          |
| Reaction ID        | Unique identifier for a reaction                                                                     | Integer                                                                                                 | 20      | System-generated sequential integer, beginning with 1                                        |
| Recipe             | Instructions on how to make an Ice Cream Flavour.                                                    | Recipe Name <br>+ Author <br>+ isActive <br>+ 0:n{Allergen} <br>+ 1:n{Ingredient} <br>+ 1:n{Direction}                      | N/A     | N/A                                                                                          |
| Recipient          | An employee who receives a message                                                                   | Employee ID                                                                                             | N/A     | N/A                                                                                          |
| Role               | The function that is required of a given employee or shift.                                          | String                                                                                                  | 20      | Manager, Front of House Staff, Kitchen Staff, Bookkeeper, Delivery Driver                    |
| Schedule           | The shifts currently assigned to an employee.                                                        | Employee ID  <br>+ 0:n{Shift ID} <br>+ Author                                                                   | N/A     | N/A                                                                                          |
| Shift              | An assigned time for an employee to work at a given Banter Ice Cream branch location.                | Shift ID <br>+ Start Time <br>+ End Time <br>+ Role <br>+ Location                                                      | N/A     | N/A                                                                                          |
| Shift ID           | Unique identifier for a shift                                                                        | Integer                                                                                                 | 20      | System-generated sequential integer, beginning with 1                                        |
| Start Time         | The date time that a shift begins.                                                                   | DateTime                                                                                                | 8 bytes | Format YYYY-MM-DD HH:MI:SS                                                                   |
| Timestamp          | The date and time that the object was created.                                                       | DateTime                                                                                                | 8 bytes | Format YYYY-MM-DD HH:MI:SS                                                                   |
| Units              | The units for a quantity                                                                             | String                                                                                                  | 20      | Standard baking units: cups, tablespoons, teaspoons, milliliters, liters, milligrams, grams  |
| User Account       | An account that an employee using to access the system                                               | Username <br>+ Employee ID <br>+ Password                                                             | N/A     | N/A                                                                                          |
| Username           | Unique identifier for a user in the form of an email                                                 | String                                                                                                  | 320     | Form of local@domain                                                                         |
| View               | An employee who has viewed an announcement                                                           | Employee ID <br>+ Timestamp                                                                                 | N/A     | N/A                                                                                          |

The system shall have data entries as described by the data dictionary. The data dictionary has 5 columns. The first column, data element, provides an identifier for the type of data entry. The second column, description, describes in plain language, what the data entry will represent in the system. The third column, composition or data type, describes what data is included in the data entry. A composition has multiple data elements listed that make up one entry of that data element. Each data element listed is separated using a “+” sign. Some data elements may also have curly braces around them. In front of the curly braces there are numbers to represent the minimum and maximum number of the data element in curly braces that can be associated with each value saved of the data entry type, the form is "minimum number of the data element:maximum number of the data element". If the data element is not a composition it is a primitive, therefore it can be described by its data type. The fourth column, length, provides more context for a primitive data element’s data type in the form of a maximum length for the data type. The fifth column, values, provides more context for a primitive data element’s allowed values. 


## iii. Reports <a name="data-report"></a>

The system shall not generate any reports.


## iv. Data Integrity <a name="data-integrity"></a>

**Employee Data and Account**
- Adhere to Canadian laws regarding business tax documents. As a result the system must retain supporting documentation for payroll for 6 years, counted from the end of the tax year that the payroll occurred in. The supporting documentation required is employee name, contact information, and wage.
- The system must retain each employee's banking information until after employee last paycheck is recieved by employee.
- A new employee can gain access to the system after a manager adds an account for the employee.
- An employee loses access to the system when their account is deleted. 

**Scheduling and Tracked Hours**
- The system must retain each shift in employee schedule for one year after the scheduled shift date.
- The system must retain employee availability for one week after the date of the identified availability.
- The system must retain clocked hours for each employee for 6 years, counted from the end of the year the clocked hours occurred in. This requirement is necessary due to Canadian laws regarding business tax documents.

**Communication and Announcements**
- The system must retain messages for one year after the message is sent.
- The system must retain each announcement until the announcement is removed by manager.

**Recipe Management**
- The system must retain each recipe for lifetime of system.

**Onboarding Materials**
- The system must retain each onboarding material until removed by manager.


# 7 External Interface Requirements <a name="external-interfaces"></a>

## i. User Interfaces <a name="user-interfaces"></a>

A medium fidelity prototype of the system can be found here: https://www.figma.com/file/Uc9R5x3QO1j0RJcTtubefa/Prototype?type=design&node-id=0-1&mode=design&t=8ogwlELfk2Qu3Zly-0

The prototype is designed to fit the screen of an iPhone 14, so the screen layout has the dimensions 390 x 844. Upon opening the app the user is prompted to enter a username and password. <br/>
The prototype has been designed for a user with a management role. The GUI standards to be followed were based on the Banter Ice Cream website, this includes the green and orange color scheme, font and the header banner. There are 2 versions of the homepage a management version and a non-management verion. Both versions of the homepage have a header at the top of the screen and an icon bar at the bottom. The management version of the homepage includes 3 buttons on the main screen "Announcements", "Onboarding Materials", and "Account Management" (See Image 1). 

<figure>
   <img src="https://github.com/Uvic-SENG321Spring2024/team8-developer/blob/main/Prototype%20Images/NewMHS.png" width="390" height="844">
   <figcaption>Image 1: Management Home Screen.</figcaption>
</figure>

The homepage for the non-management version of the homepage includes 2 buttons on the main screen "Announcements", and "Onboarding Materials" (See Image 2). The icon bar contains the following icons from left to right calendar, communication, home, recipe menu, and personal account info. This icon bar is displayed on every screen which allows for quick access to each feature at anytime. Each page after the main page of each feature contains a back arrow in the top left where a user can go back to a previous page.

<figure>
   <img src="https://github.com/Uvic-SENG321Spring2024/team8-developer/blob/main/Prototype%20Images/NewGHS.png" width="390" height="844">
   <figcaption>Image 2: Non-Management Home Screen.</figcaption>
</figure>

The user is prompted with an error message (example in Image 3) to reduce mistakes using the application. A couple of cases that result in an error message include a user trying to login without entering both a username and password, and trying to exit without saving when creating or editing a recipe. 

<figure>
   <img src="https://github.com/Uvic-SENG321Spring2024/team8-developer/blob/main/Prototype%20Images/Error%20Message.png" width="390" height="844">
   <figcaption>Image 3: Error Message.</figcaption>
</figure>

## ii. Hardware Interfaces <a name="hardware-interfaces"></a>

### Processing
- **Memory Space:** A minimum of 40 MB of free space will be required to install application.

### Resolution
- **Adapatable:** The application must be able to adapt to different phone screen resolutions and orientations.

### Hardware Access
- **Internal Storage:** The application will need access to internal storage of files to attach allowed file types to messages, announcements, recipes, and onboarding materials. The internal storage includes any local storage, cloud storage linked to the device, and the device's camera roll. The allowed file types include images, videos, and PDFs. 
- **Internet Connection:** The application will connect to the internet to backup application data and receive updates to data stored in the application. 

## iii. Software Interfaces <a name="software-interfaces"></a>
The Banter Ice Cream system interfaces with several software components to ensure seamless operation, data integrity, and user experience. Below are the key software interfaces and their purposes:
  
### Operating System
- **Operating Systems:** Android and iOS
- **Purpose:** The mobile application is designed to run on these operating systems, utilizing their native features and capabilities for notifications, data storage, and security.
- **Services Used:** local data encryption, and background task execution.

### Database System
- **Database:** MySQL 8.0 or PostgreSQL 13
- **Purpose:** Stores and manages all application data including user accounts, schedules, recipes, announcements, and employee information.
- **Data Exchange:** CRUD (Create, Read, Update, Delete) operations on employee details, schedules, recipes, and announcements.

### Authentication Service
- **Service:** OAuth 2.0 compliant service (e.g., Auth0)
- **Purpose:** Securely authenticate users without storing passwords in the application, allowing for single sign-on (SSO) capabilities and access control based on user roles.
- **Data Exchange:** Token-based authentication and authorization data.

## iv. Communication Interfaces <a name="communication-interfaces"></a>

### Messaging Services
The system will support embedding of images, videos, and PDFs in messages and announcements. 

### Security and Privacy
Communication channels must be secure, with safeguards for sensitive information like chat logs and management of announcements. This entails encryption, controlled access, and compliance with privacy regulations.

### Network Server Communication Protocols
- **Protocol:** HTTPS for all communications between the mobile application and server backend.
- **Purpose:** Ensure the secure transmission of sensitive data between the mobile app and the backend services.
- **Data Items:** API requests and responses, including authentication tokens, user input data, server responses, and error messages.

### Electronic Forms
- **Purpose:** Collect input from users within the app, such as availability, time-off requests, and onboarding materials.
- **Data Handling:** Secure submission to the backend server with validation both on the client-side and server-side.
- **Data Items:** Form fields and values, validation rules, and submission confirmations.

# 8 Software Quality Attributes <a name="quality-attributes"></a>

**Availability**
- AVL-1: The system is available 99.99% each day during business hours.
- AVL-2: The system is available 99.0% each day outside of business hours.

**Reliability**
- REL-3: A backup of all system data is saved every night to minimize data loss. 

**Scalability**
- SCA-4: The system should be designed to easily accommodate future growth of employees with up to 200 users within the next 2 years.
- SCA-5: The system should be designed to easily accommodate new functionalities without significant changes to the system architecture
- SCA-6: The system can accommodate the addition of extra archive storage of recipes over the system lifetime. 

**Useability**
- USE-7: The system should be user-friendly and allow a new employee to learn to use system features that are relevant to their role within three shifts.
- USE-8: Shift swapping should be accessible within 3 selections. 
- USE-9: Viewing schedules should be accessible within 2 selections. 
- USE-10: Accessing announcements should be accessible within 1 selection. 
- USE-11: Viewing recipes should be accessible within 2 selections. 
- USE-12: Viewing messages should be accessible within 3 selections. 
- USE-13: Standard conventions for all user interface elements

**Performance** 
- PER-14: The system must be able to handle 30 users simultaneously accessing it without degradation in performance. 
- PER-15: Response times for loading pages and executing commands should not exceed 2 seconds under normal operational conditions.

**Security**
- SEC-16: Unauthorized employees are not be able to view another employee’s banking information
- SEC-17: Industry standard information security procedures must be used when handling user information. 
- SEC-18: The system shall ensure that no persons outside the organization can access any information stored in the system. 
- SEC-19: Recipe ingredients and instructions can only be viewed by authorized employees.
- SEC-20: Recipe ingredient allergens can only be viewed by authorized employees.


# 9 Analysis Models <a name="analysis-models"></a>

## i. Data Flow Diagram Level 0 <a name="data-flow0"></a>

![L0DFDBen drawio](https://github.com/Uvic-SENG321Spring2024/team8-developer/assets/76890860/5bf48c9e-21e6-4b2a-a399-70acf556f2ee)

The above Level 0 Data Flow Diagram depicts the Banter Ice Cream System as a centralized system interacting with four external entities: Staff, Manager, Bookkeeper, and Delivery Driver. 
The "All Users" entity in this Data Flow Diagram represents a collective group that includes every type of user in the system, providing a centralized point for data flows that are common across all user types to reduce redundancy and simplify the diagram's clarity. The system handles a variety of data flows including account updates, shift swap requests, onboarding materials, and clock-in/out data. It represents a high-level view of the system's interactions with its environment, showing how data is exchanged but not the internal workings of the system itself. The arrows indicate the direction of the data flow, meaning the data originates from the entity at the tail of the arrow and moves towards the entity at the head of the arrow. 

## ii. Data Flow Diagram Level 1 <a name="data-flow1"></a>

![DFDL1B drawio](https://github.com/Uvic-SENG321Spring2024/team8-developer/assets/76890860/702c90b2-718b-4702-89a2-59a750469ab6)

The above Level 1 Data Flow Diagram expands on the Level 0 by breaking down the system into more detailed processes: Manage User Account, Communicate, Facilitate Onboarding, Manage Schedule, Swap Shift, View Tracked Hours, and Manage Recipe. Each of these processes is a part of the Banter Ice Cream System, representing different functionalities. It shows specific interactions between the system and users, such as account creation, schedule Management, and recipe updating. The diagram includes a data store for Staff Hours Summary indicating where data is stored within the system. This Data Flow Diagram provides a more detailed understanding of the system's internal processes and their data interactions.

## iii. Data Flow Diagrams Level 2 <a name="data-flow2"></a>


# 10 Appendix <a name="appendix"></a>

No appendices for this document.
