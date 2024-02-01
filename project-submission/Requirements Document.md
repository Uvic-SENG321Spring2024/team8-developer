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

1. **Overview**

      This document will explore an opportunity to centralize Banter Ice Cream’s internal management. First, we will discuss Banter’s business requirements and illustrate the goal of the project. Second, the document will discuss the major features, scope, and limitations of the project. Third, more context for the project will be provided such as user classes, operating environment, and constraints. These sections are outlined in the list below.

1 Overview \
2 Business Requirements \
&nbsp;&nbsp;&nbsp;&nbsp;i. Background \
&nbsp;&nbsp;&nbsp;&nbsp;ii. Business Opportunity \
&nbsp;&nbsp;&nbsp;&nbsp;iii. Business Objectives \
&nbsp;&nbsp;&nbsp;&nbsp;iv. Success Metrics \
&nbsp;&nbsp;&nbsp;&nbsp;v. Product Vision Statement \
3 Scope and Limitations \
&nbsp;&nbsp;&nbsp;&nbsp;i. Major Features \
&nbsp;&nbsp;&nbsp;&nbsp;ii. Project Scope \
&nbsp;&nbsp;&nbsp;&nbsp;iii. Limitations and Exclusions \
4 Context Description \
&nbsp;&nbsp;&nbsp;&nbsp;i. User Classes and Characteristics \
&nbsp;&nbsp;&nbsp;&nbsp;ii. Operating Environment \
&nbsp;&nbsp;&nbsp;&nbsp;iii. Design and Implementation Constraints \
&nbsp;&nbsp;&nbsp;&nbsp;iv. Assumptions and Dependencies \
&nbsp;&nbsp;&nbsp;&nbsp;v. Glossary of Terms \
&nbsp;&nbsp;&nbsp;&nbsp;vi. References 
   
2. Business Requirements

   1. **Background**
   The client wants an improvement of the software that they are using for scheduling, communication, and payroll management. Banter's current scheduling system, Homebase, lacks certain features resulting in employees having difficulty switching shifts. One feature missing is the ability for staff to view the schedules of other employees working at their location. In addition, the scheduling system does not interface with their financial service, Quickbooks, resulting in manually recording and inputting data such as hours, holidays, overtime, and sick days is required to manage finances. Basecamp is used for staff wide announcements and news regarding the company. Having multiple pieces of software used to receive messages results in Basecamp being checked infrequently and employees missing important announcements. The client wants a solution that will make managing finances, swapping shifts, and communicating with staff easier to accomplish.

   2. **Business Opportunity**
   Describe the business problem that is being solved or the process being improved. Describe the needs of typical customers or of the target market. Present customer problems that the new product will address. 

   3. **Business Objectives**
   Summarize the important business benefits the product will provide in a quantitative and measurable way. Organizations generally undertake a project to solve a problem or exploit an opportunity. Business objectives define ways to measure achievement of business goals. 

   4. **Success Metrics**
      
      **Announcement Accesses**
      
      Staff are better notified of the announcements.  Interactions with the announcements are increased by 50%. This will be measured by replies, reactions, and further questions to the managers.
      
      **Uncovered Shifts**
      
      The number of understaffed shifts due to someone picking up a shift that overlaps with their current shift is reduced by 90%. 
      
      **Customer Satisfaction with the System**
      
      This will ensure employees see the announcements about monthly ice cream flavors and provide better service to the customers. There should also be less understaffed shifts. This will increase the average of new customer reviews by 0.1 stars.
      
      **Bookkeeping Efficiency**
      
      Better integration with Quickbooks and automatic calculation of statutory holiday and overtime pay should save the bookkeeper time. This will ideally save the bookkeeper over 5 hours per pay period.

# 3 Scope and Limitations
## 3.1 Major Features

1. **Centralized Communication and Scheduling System:**
   - Combines features of Homebase and Basecamp into a single, streamlined platform.
   - Allows company-wide announcements, shift swapping, and personal messaging.
   - Provides visibility of monthly ice cream flavors, events, and other important updates.

2. **Automated Payroll and Hours Tracking:**
   - Integrates with Quickbooks for seamless payroll management.
   - Automatically tracks employee hours, including regular, overtime, sick days, and holidays.
   - Reduces manual entry errors and streamlines the invoicing process.

3. **Enhanced Scheduling Flexibility:**
   - Offers a calendar view for both managers and employees to view and manage shifts.
   - Enables easy shift swapping and visibility of staff schedules across different days.

4. **Optimized Onboarding and Training:**
   - Offers an easy way for new employees to familiarize with the software platform.
   - Simplifies learning curve with a unified system replacing multiple apps.

5. **Role-based Access and Functionality:**
   - Different access levels for managers, bookkeepers, delivery drivers, and staff.
   - Tailored interfaces and features depending on the user’s role within the company.

6. **Real-time Communication for Delivery and Logistics:**
   - Special features for delivery drivers to communicate with management and clock in/out.
   - Ensures smooth coordination between different locations.
      

## 3.2 Project Scope

The software being developed is a comprehensive employee management and communication system designed specifically for Banter Ice Cream. Its purpose is to consolidate various existing systems (Homebase, Basecamp, Quickbooks) into one centralized platform, improving internal communication, scheduling efficiency, and payroll management. The anticipated benefits include better-informed employees, streamlined shift management, reduced manual errors in payroll, and an overall increase in operational efficiency. This directly aligns with the company's objectives of enhancing customer satisfaction, improving employee engagement, and facilitating business growth through better internal management practices.

## 3.3 Limitations and Exclusions

1. **Inventory Management System**

      - Inventory Management was mentioned as a desired feature, but it does not fit in with the rest of the system requested.

2. **Recipe Management**

      - Recipe Management was a desired feature but will not be a priority to include in the system. This is because it may not integrate well with the other features, and there are alternate solutions outside of the system.

3. **Automated Data Migration**

      - Automated Data Migration to the new system may be a difficult feature to implement. It will be implemented if possible but may be more practical to do manually since it’s a one-time action.

5. **Context Description**

   1. **User Classes and Characteristics**

        When creating a centralized platform for Banter Ice Cream, understanding the diverse user classes is crutial to craft an efficient and user-centric platform that seamlessly integrates with Banter Ice Cream's opperational needs.
      
      * **Front of House / Kitchen Managers:**
         * **Characteristics:**
            * High frequency of use (daily or weekly)
            * Responsible for scheduling, training, announcements, and managing staff
            * Has a supervisory role
            * Moderate to high technical expertise
         * **Requirements:**
            * Advanced scheduling functionalities (creation, editing, approval, etc)
            * Access to training modules and documents
            * New employee account creation
            * Announcement creation and management
            * Communication channels for group or individual messaging
         * **Importance:** Favored user class since there role is critical for staff management and communication
      * **Bookkeeper:**
         * **Characteristics:**
            * Moderate frequency use (mostly during payroll periods)
            * Focus on accounting, payroll, and tracking work hours
            * High technical expertise in accounting software
         * **Requirements:**
            * Integration with Quickbooks for payroll
            * Hours need to be summarized with overtime, holiday, etc
            * Data export capabilities for accounting purposes (export hours worked, etc)
         * **Importance:** Critical for financial management (favored class during specific periods)
      * **Delivery Drivers:**
         * **Characteristics:**
            * Use during sporadic weekly shifts
            * Main focus on clocking in/out and communication
            * May have different levels of technical expertise
         * **Requirements:**
            * Simple and efficient clock-in/clock-out features
            * Communication channel for shift-related updates
            * Real-time schedule accessibility
         * **Importance:** Frequent users which have direct impact on customer satisfaction (favored user class)
      * **Front of House / Kitchen Staff:**
         * **Characteristics:**
            * Daily use during shifts
            * Main focus on clocking in/out, receiving updates, and managing shifts
            * May have different levels of technical expertise
         * **Requirements:**
            * Intuitive clock-in/clock-out features
            * User-friendly interface for shift management
            * Communication channels for shift coverage and updates
         * **Importance:** Frequent users with direct impact on customer satisfaction (favored user class)
      * **Customers (Indirect Users):**
         * **Characteristics:**
            * Infrequent interaction
            * Interacts with the system indirectly through the accuracy of information provided by employees
            * Little technical expertise
         * **Requirements:**
            * Able to see accurate and up-to-date information about products
            * Limited access to internal system functionalities
         * **Importance:** customer satisfaction is crucial (favored user in terms of customer impact)
      * **New Employees (During Onboarding):**
         * **Characteristics:**
            * Limited initial interaction
            * Low technical expertise during onboarding phase
         * **Requirements:**
            * Clear and concise onboarding information
            * Notifications for new schedules or training sessions 
         * **Importance:** Critical during onboarding phase (favored for ease of learning)
      * **Favored User Classes:**
         * **Priority Users:** Front of House / Kitchen Managers, Bookkeeper, Front of House / Kitchen Staff
         * **Critical Impact Users:** Customers (Indirect Users)
         * **Support Users:** New Employees (During Onboarding)
         * **Transactional Users:** Delivery Drivers

   3. **Operating Environment**

        Describe the environment in which the software will operate, including the hardware platform, operating system and versions, and any other software components or applications with which it must peacefully coexist.


   4. **Design and Implmentation Constraints**

        Describe any items or issues that will limit the options available to the developers. These might include: corporate or regulatory policies; hardware limitations (timing requirements, memory requirements); interfaces to other applications; specific technologies, tools, and databases to be used; parallel operations; language requirements; communications protocols; security considerations; design conventions or programming standards (for example, if the customer’s organization will be responsible for maintaining the delivered software).


   5. **Assumptions and Dependencies**

        List any assumed factors (as opposed to known facts) that could affect the requirements stated in the RD. These could include third-party or commercial components that you plan to use, issues around the development or operating environment, or constraints. The project could be affected if these assumptions are incorrect, are not shared, or change. Also identify any dependencies the project has on external factors, such as software components that you intend to reuse from another project.
   6. **Glossary of Terms**

      Define all the terms necessary to properly interpret the RD, including acronyms and abbreviations.


   7. **References**

      No references used in this document.
