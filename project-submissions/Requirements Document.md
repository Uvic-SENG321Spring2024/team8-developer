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
   1. [System Feature 1](#feature-1)
      -  Description and Priority
      -  Functional Requirements
      -  Use Cases
   2. [System Feature 2](#feature-2)
   3. Other Features...
6. [Data Requirements](#data-requirements)
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
The client, Banter Ice Cream, wants an improvement of the software that they are using for scheduling, communication, and payroll management. Banter's current scheduling system, Homebase, lacks certain features resulting in employees having difficulty switching shifts. One feature missing is the ability for staff to view the schedules of other employees working at their location. In addition, the scheduling system does not interface with their financial service, Quickbooks, resulting in manually recording and inputting data such as hours, holidays, overtime, and sick days which is required to manage finances. Basecamp is used for staff wide announcements and news regarding the company. Having multiple pieces of software used to receive messages results in Basecamp being checked infrequently and employees missing important announcements. The client wants a solution that will make managing finances, swapping shifts, and communicating with staff easier to accomplish.


## ii. **Business Opportunity** <a name="opportunity"></a>
The process being improved is the current employee management system at Banter Ice Cream. The client desires a system that is easy to use, has automation for certain aspects, and includes improved functionalities compared to what the old system offers. 

The new product will add enhanced functionalities to the current scheduling system. One new functionality is allowing the client to track the number of hours that each employee has on regular works days, sick days, statutory holidays, and overtime. It should also offer shift swapping and visibility of staff schedules everyday. 

The new product will also include enhanced communication functionality. It should also include message and announcement capability that is similar to the current systems, Homebase and Basecamp. It will allow employees and managers to communicate directly within the system through messages or announcements. The announcements will allow employees to provide customers with information regarding monthly ice-cream flavors, events, and other updates. 

The new product will include an automated payroll management feature, which will reduce manual errors and time associated with bookkeeping compared to the manual entry of payroll information. 

At last, onboarding and training of new employees will be easier with the new system. Staff shall have different access to the system according to their roles. 


## iii. **Business Objectives** <a name="objective"></a>

Banter Ice Cream's new system will faciliate business growth through better internal management practices. The following objectives will all contribute to the increased business growth.
* Improve employee engagement through a unified communication platform.
* Improve customer satisfaction because the employees will be better informed of ice cream flavour changes and the new scheduling system will reduce the occurances of understaffing.
* Reduce time and manual errors associated with payroll, as the new system will automatically calculate hours associated with sick days, holidays, and overtime.
* Reduce costs and time associated with onboarding new employees, as a single unified system will be easier to learn than multiple applications.


## iv. **Success Metrics** <a name="success"></a>

The following metrics will be used to measure the success of the system.

**Announcement Visibility**
      
Staff are better notified of any announcement. Interactions with the announcements are increased by 50%. This will be measured by the number of replies, reactions, and further questions to the managers.
      
**Uncovered Shifts**
      
The number of understaffed shifts due to someone picking up a shift that overlaps with their current shift is reduced by 90%. 
      
**Customer Satisfaction**
      
The system will ensure employees see the announcements about monthly ice cream flavors and provide more accurate information to the customers. There shall be less understaffed shifts. More accurate information and better staffing will increase the average score of new reviews by 0.5 stars.
      
**Bookkeeping Efficiency**
      
Better integration with Quickbooks and automatic calculation of statutory holidays, sick days, and overtime shall save the bookkeeper time. This shall save the bookkeeper at least 5 hours each pay period.


## v. **Product Vision Statement** <a name="vision"></a>
The new system intends to improve communication between staff at Banter Ice Cream. This will be accomplished by reducing scheduling confusion, minimize time spent manually calculating hours, and ensuring relevant information is passed to employees. This will be done by combining the systems that are currently used, Homebase and Basecamp; with additional features to improve the client's integration with Quickbooks. The goal of this product is to increase employee engagement with the system, streamline the creation of staff schedules, improve finance management, and improve customer satisfaction by providing accurate and up to date information.

# 3. Scope and Limitations <a name="scope"></a>

## i. **Major Features** <a name="features"></a>

The following features shall be included in the system.

**Centralized Communication and Scheduling System:**
   - Combines features of Homebase and Basecamp into a single, streamlined platform.
   - Allows company-wide announcements, shift swapping, and personal messaging.
   - Provides visibility of monthly ice cream flavors, events, and other important updates.
   - Allows image, video, and pdf embeds in announcements and messaging.

**Automated Payroll and Hours Tracking:**
   - Integrates with Quickbooks for seamless payroll management.
   - Automatically tracks employee hours, including regular, overtime, sick days, and holidays.
   - Reduces manual entry errors and streamlines the invoicing process.
 
**Enhanced Scheduling Flexibility:**
   - Offers a calendar view for managers to view and manage shifts.
   - Offers a calendar view for employees to view shifts.
   - Allows staff to clock in/out of shifts.
   - Enables easy shift swapping and visibility of staff schedules across different days.
      
**Optimized Onboarding and Training:**
   - Offers an easy way for new employees to familiarize with the software platform.
   - Simplifies learning curve with a unified system replacing multiple apps.
      
**Role-based Access and Functionality:**
   - Different access levels for managers, bookkeepers, delivery drivers, and staff, as defined in User Classes and Characteristics section of this Requirements Document.
   - Tailored interfaces and features depending on the user’s role within the company.
      
**Real-time Communication for Delivery and Logistics:**
   - Special features for delivery drivers to communicate with management and clock in/out.
   - Ensures smooth coordination between different locations.


## ii. **Project Scope** <a name="project-scope"></a>

The software being developed is a comprehensive employee management and communication system designed specifically for Banter Ice Cream. Its purpose is to consolidate existing systems Homebase and Basecamp into one centralized platform that integrates with Quickbooks, improving internal communication, scheduling efficiency, and payroll management. The anticipated benefits include better-informed employees, streamlined shift management, reduced manual errors in payroll, and an overall increase in operational efficiency. This directly aligns with the client's objectives of enhancing customer satisfaction, improving employee engagement, and facilitating business growth through better internal management practices.


## iii. **Limitations and Exclusions** <a name="limitations"></a>


The following features will be excluded from the system.

**Inventory Management System**
   - Inventory Management was mentioned as a desired feature, but it does not fit in with the rest of the system requested.

**Automated Data Migration**
   - Automated Data Migration to the new system may be a difficult feature to implement. It will be implemented if possible but may be more practical to do manually since it’s a one-time action.



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
 
## i. System Feature 1 <a name="feature-1"></a>

State the feature name in just a few words.

### a. Description and Priority
Provide a short description of the feature and indicate whether it is high, medium, or low priority.

### b. Functional Requirements
Where applicable - Itemize the detailed functional requirements associated with this feature. These are the software capabilities that must be present in order for the user to carry out the services provided by the feature, or to execute related use case(s). Include how the product should respond to anticipated error conditions or invalid inputs. Requirements should be concise, complete, unambiguous, verifiable, and necessary. Use “TBD” as a placeholder to indicate when necessary information is not yet available. Each requirement should be uniquely identified with a sequence number or a meaningful tag of some kind. These could be requirements that the clients provided directly or were defined by the designer group as a result of rendering the feature. Each requirement should also include information a(1) bout Backward Traceability (the rationale for the requirements and the source – RFP and which section in it, client meeting and which notes from that meeting, etc.. and (2) Forward Traceability (how the requirement can be verified by the users.

REQ-1:

REQ-2:

### c. Use cases associated with the feature or functional requirement

This is the use case specification. For each Use Case, list the dialog elements in the use case that elaborates or is related to this feature or one of its functional requirements, i.e. sequences of user actions and system responses that stimulate the behavior defined for this feature/functional requirement.

## ii. System Feature 2 (and so on) <a name="feature-2"></a>

# 6 Data Requirements <a name="data-requirements"></a>
(e.g., formatting)

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
