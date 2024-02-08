# Next Steps After Interview

## Actionable Steps for Each Section

### Overall
Issue 27
- Remove adverbs ("fluffy language") from the document where possible

### 2.1 Background
Issue 17
- Please ensure that the following issues are included in the section
   - onboarding new staff it is difficult for new employees to learn multiple platforms
   - there are problems with information being passed on to customers (specifically accurate ice cream flavours due to missed announcements)
 
### 2.2 Business Opportunity
Issue 18
- Expand on reasoning for why each goal is important to address
- Ensure that all goals are high-level and independent of solution
- Remove "One new functionality is allowing the client to track the number of hours that each employee has on regular works days, sick days, statutory holidays, and overtime. It should also offer shift swapping and visibility of staff schedules everyday."

### 2.3 Business Objectives
- Clarify understanding of this section if possible (ask TA)

Issue 19 and 20
- Quantify goals (see below in Interview Summary for the goals we discussed in interview)
- Ensure that the details in this section are not a success metric, but are still quantified?

### 2.4 Success Metrics
Issue 21
- Remove ambiguous terms (listed in issue)
- Focus on the quantifiable details

### 3.1 Major Features
Issue 22
- Reword "Centralized Communication and Scheduling System" to something like "Communication" or "Messaging"
- Remove "Combines features of Homebase and Basecamp into a single, streamlined platform."
- Focus on action, not goal of feature
   - Specifically mentioned was "Optimized Onboarding and Training"

Issue 23
- Include Recipe Management in Major Features (see details in Interview Summary below)
   - Also need to remove from Limitations and Exclusions
- Reduce Quickbooks Integration to Automatic Hour Summary (see details in Interview Summary below)

Other Features we Discussed
- Employees must be able to initiate a shift swap, then manager must approve, before change is made
   - One employee initiates and selects employee they are swapping with, the other employee agrees, sent to manager for approval
- Scheduling should include a section to list availability (ie. employees are able to enter when they are available to work)
- Must be basic security for app (such as a login) 

### 3.3 Limitations and Exclusions
Issue 23
- Move Recipe Management to Major Features (coordinate who has this task)

Other Features we Discussed (do these all go in exclusions?)
- Notifications
- Emergency calling out of shift
- Desktop view? (this could just go in Operating Environment section)
- Automatic Integration to Quickbooks (again, coordinate who has this task as it is being modified in Major Features)
- Messaging a specific shift

### 4.1 User Classes
Issue 24
- Separate "Front of House Employees" and "Kitchen Employees" as recipe access is different
- Acceptable to leave "Front of House Managers" and "Kitchen Managers" as one user class

Issue 25
- Remove Customers (indirect users are not a user)

Issue 26
- Remove New Employees (access is same as other employees)

Other Points
- Onboarding material accessible to all employees
- All employees (except managers) need to be able to clock in/out
- All employees (except bookkeepers) need to view their shift schedule
- Information stored about employees: name, role, banking info, shift schedule, messages
   - Bookkeeper can access all employees banking information
   - All employees can access name, role, shift schedule

### 4.2 Operating Environment
Issue 28
- Specify that we are designing a mobile application
- Out of scope is a desktop view for managers and bookkeepers, perhaps in future iterations

### 4.3 Design and Implmentation Constraints
Issue 29
- Separate first point into multiple constraints
- Remove access to progress reports (not a feature of the system)
- Remove access to payroll (not a feature of the system, just banking information is - payroll is handled by Quickbooks)
- Expand on "At least 70 people need to be able to access the software."
   - Max of 30 simultaneous users (determined based on estimate for users during peak time such as the start of shift)
   - There are between 50-70 employees at any time
   - The lifetime of system must not limit number of employees


## Interview Summary

Issue 19/20:
- Rewrite Business Opportunity, Business Objectives, and Success Metrics so they have distinct purpose
- Opportunity should be high level goal with reasoning
- Objectives should be quantified, and are an extension of goals/opportunity
   - Include: employee engagement, customer satisfaction, reduced payroll errors
   - Don't include: cost 
- Success Metrics are smaller milestones that are also quantified

Issue 22: 
- Remove the term "centralized"
- Features should be actions that can be taken
    - Ensure all current features are worded as actions, not goals
- Separate "Centralized Communication and Scheduling" because communication and scheduling are separate features

Issue 23:
- Include recipe management as a major feature
   - Four levels of access (managers need view/edit, kitchen need to view, front of house need limited view to allergens, delivery driver/bookkeepers no access)
   - Recipes have name, ingredients list, steps
   - All recipes stored indefinetely
   - Two sections, currently served and out of service
   - No search features requested
- Simplify Quickbooks integration, just produce a summary of hours (with shift, holiday, overtime, sick day, etc. automatically calculated)
   - Bookkeeper can still enter into Quickbooks, just with more accurate information than current system
 
Issue 24: 
- Front of house and kitchen manager have same access

Issue 26:
- Onboarding material should be accessible to all employees
- Remove new employee class

Issue 28:
- Implementing mobile
- Desktop is out of scope (perhaps future iteration)

Issue 29:
- Employees fluctuate between 50-70
- Max 30 simultaneous users
- Reword "at least 70"

Extra Questions
- Notification feature out of scope
- Managers are salary, everyone else is clock in/out
- Bookkeepers work infrequently (not scheduled shifts)
- Delivery drivers work twice a week (scheduled shifts)
- Employees initiate shift swaps, managers approve
- Scheduling has an option for employees to add availability and select designated vacation days
- Short notice to unable to make shift, bookkeepers will need to manually make change and be informed
- Low priority to message a specific shift
- Basic security, login for whole app
- Stored info about employees: name, role, banking info, shifts, communication
    - do not include progress reports
- Store shifts for minimum of one year for tax purposes
- Shifts scheduled two weeks out
