# Requirements Document - Banter Ice Cream (January 28, 2024)

# Revision History

| Name | Date | Reason for Changes | Version |
| ----------- | ----------- | ------------- | ---------- | 
|  |  | | |
|  |  | | |
|  |  | | |
|  |  | | |

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

        Describe the environment in which the software will operate, including the hardware platform, operating system and versions, and any other software components or applications with which it must peacefully coexist.


   4. **Design and Implmentation Constraints**

        Describe any items or issues that will limit the options available to the developers. These might include: corporate or regulatory policies; hardware limitations (timing requirements, memory requirements); interfaces to other applications; specific technologies, tools, and databases to be used; parallel operations; language requirements; communications protocols; security considerations; design conventions or programming standards (for example, if the customer’s organization will be responsible for maintaining the delivered software).


   5. **Assumptions and Dependencies**

        List any assumed factors (as opposed to known facts) that could affect the requirements stated in the RD. These could include third-party or commercial components that you plan to use, issues around the development or operating environment, or constraints. The project could be affected if these assumptions are incorrect, are not shared, or change. Also identify any dependencies the project has on external factors, such as software components that you intend to reuse from another project.
   6. **Glossary of Terms**

      Define all the terms necessary to properly interpret the RD, including acronyms and abbreviations.


   7. **References**

      List any other documents or Web addresses to which this RD refers. These may include user interface style guides, contracts, standards, system requirements specifications or use case documents. Provide enough information so that the reader could access a copy of each reference, including title, author, version number, date, and source or location.


5. **System Features** (Due Iteration 2 and beyond)

    This template illustrates organizing the functional requirements for the product by system features, the major services provided by the product. You may prefer to organize this section by use case, mode of operation, user class, object class, functional hierarchy, or combinations of these, whatever makes the most logical sense for your product.
   
   1. **System Feature 1**

      State the feature name in just a few words.

      1. **Description and Priority**

      Provide a short description of the feature and indicate whether it is high, medium, or low priority.
  
      2. **Functional Requirements**

      Where applicable - Itemize the detailed functional requirements associated with this feature. These are the software capabilities that must be present in order for the user to carry out the services provided by the feature, or to execute related use case(s). Include how the product should respond to anticipated error conditions or invalid inputs. Requirements should be concise, complete, unambiguous, verifiable, and necessary. Use “TBD” as a placeholder to indicate when necessary information is not yet available.
      Each requirement should be uniquely identified with a sequence number or a meaningful tag of some kind. These could be requirements that the clients provided directly or were defined by the designer group as a result of rendering the feature.
      Each requirement should also include information a(1) bout Backward Traceability (the rationale for the requirements and the source – RFP and which section in it, client meeting and which notes from that meeting, etc.. and (2) Forward Traceability (how the requirement can be verified by the users.

       REQ-1:

       REQ-2:

      3. **Use cases associated with the feature or functional requirement**

          This is the use case specification. For each Use Case, list the dialog elements in the use case that elaborates or is related to this feature or one of its functional requirements, i.e. sequences of user actions and system responses that stimulate the behavior defined for this feature/functional requirement.



   3. **System Feature 2 (and so on)**

6. **Data Requirements**  (e.g., formatting)


7. **External Interface Requirements**
   1. User Interfaces

      Describe the logical characteristics of each interface between the software product and the users. This may include sample screen images, any GUI standards or product family style guides that are to be followed, screen layout constraints, standard buttons and functions (e.g., help) that will appear on every screen, keyboard shortcuts, error message display standards, and so on. Define the software components for which a user interface is needed.
      
   2. Hardware Interfaces
   
       Describe the logical and physical characteristics of each interface between the software product and the hardware components of the system. This may include the supported device types, the nature of the data and control interactions between the software and the hardware, and communication protocols to be used.
   
   3. Software Interfaces

       Describe the connections between this product and other specific software components (name and version), including databases, operating systems, tools, libraries, and integrated commercial components. Identify the data items or messages coming into the system and going out and describe the purpose of each. Describe the services needed and the nature of communications. Identify data that will be shared across software components.
       
   4. Communication Interfaces  

      Describe the requirements associated with any communications functions required by this product, including e-mail, web browser, network server communications protocols, electronic forms, and so on.

8. **Software Quality Attributes**

    Sepcify requirements that include performance, security, reusability, maintainability, usability, availability, interoperability, etc.

9. **Analysis Models**


10. **Appendix**   
