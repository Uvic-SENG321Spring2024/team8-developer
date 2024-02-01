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
   Summarize the rationale and context for the new product or for changes to be made to an existing one. 

   2. **Business Opportunity**
   Describe the business problem that is being solved or the process being improved. Describe the needs of typical customers or of the target market. Present customer problems that the new product will address. 

   3. **Business Objectives**
   Summarize the important business benefits the product will provide in a quantitative and measurable way. Organizations generally undertake a project to solve a problem or exploit an opportunity. Business objectives define ways to measure achievement of business goals. 

   4. **Success Metrics**
   Indicators that stakeholders will use to define and measure success on the project. What are the factors that will have the greatest impact on achieving success (i.e., could include aspects within and external to the organization).

   5. **Product Vision Statement**
   Write a concise vision statement that summarizes the long-term purpose and intent of the product.   Describe the context and origin of the product being specified in this RD. For example, state whether this product is a follow-on member of a product family, a replacement for certain existing systems, or a new, self-contained product. If the RD defines a component of a larger system, relate the requirements of the larger system to the functionality of this software and identify interfaces between the two. A simple diagram that shows the major components of the overall system, subsystem interconnections, and external interfaces can be helpful but not required.




3. Scope and Limitations
   1. **Major Features**
      Summarize the major features the product contains or the significant functions that it performs or lets the user perform. Details will be provided in Section 5, so only a high level summary is needed here. Organize the functions to make them understandable to any reader of the RD. Think about how users will use the features to ensure the list is complete. Also ensure that it does not include unnecessary features that sound interesting, but does not provide customer value.     

   2. **Project Scope**
   Provide a short description of the software being specified and its purpose, including relevant benefits, objectives, and goals. Relate the software to corporate goals or business strategies.

   3. **Limitations and Exclusions**


      **Inventory Management System**
            - Inventory Management was mentioned as a desired feature, but it does not fit in with the rest of the system requested.

      **Recipe Management**
            - Recipe Management was a desired feature but it will not be a priority to include in the system. This is because it may not integrate well with the other features, and             there are alternate solutions outside of the system.

        **Automated Data Migration**
              - Automated Data Migration to the new system may be a difficult feature to implement. It will be implemented if possible, but may be more practical to do manually                   since it’s a one-time action.
 
4. **Context Description**

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

        The ideal environment for software is a versatile mobile-based platform, compatible with both Android and iOS systems. In contrast, for the managers, a robust desktop application, supporting Windows 10 or 11, is most effective.


   4. **Design and Implmentation Constraints**

        - Employees can only access their own information, such as banking, payroll, and employee files (progress reports). They are able to see schedules for other employees (at same location). Managers also have access to employee files. Bookkeepers are able to use payroll information to pay employees.
        - More than 70 people need to be able to access the software.



   5. **Assumptions and Dependencies**

        - We assume that all employees working at Banter have smartphones that are capable of connecting to the internet to update. 
        - The new system will interface with existing systems except Quickbooks and will need to connect all departments and customers to a centralized database. And we assume there is no encryption protocol, which is required so that data can be transmitted securely between departments.

   6. **Glossary of Terms**

     | **Word**  | **Definition** |
     | ------------- | ------------- |
     |  Banter |  An Ice Cream shop located in Abbotsford, BC and Chilliwack, BC. |
   

   7. **References**

      No references used in this document.
