# Questions for Second Client Interview

Date: February 7, 2024

Initial Draft

---

## Followup to GitHub Issues

### Business Opportunity
(issue 19 and 20)
- Please clarify the potential contradtion about two issues. Wouldn't adding quantifiers for business objectives result in all the objectives being a redundant success metric?

### Major Features
(issue 20)
- How would you prefer features be phrased? What do you as a difference between a feature and a goal? (to ensure we can follow the feedback correctly, and not miss other examples of this instance)

### Limitations and Exclusions
(issue 23)
- Could you please expand on what you would like in a recipe management feature? 
   - Our understanding is there are two access levels (kitchen employees/kitchen managers vs. other employees)? How does that affect front of house managers? Delivery drivers?
   - Should this feature just store recipes? What information should be included in each recipe? Any expectations for formatting?
   - Who is adding/editing recipes?
   - Do you want to store recipes indefinetely? Remove every month? Are the permissions for who can remove recipes different than creating?
   - How often do you except these recipes to be accessed?
   - Does recipe management involve searching or filtering through the recipes?
- Are any of the currently included features a lower priority than recipe management? The scope is already quite large, and we doubt we can include recipe management without other aspects of the system being incomplete.

### User Classes
(issue 24)
- Could you please expand on the differences between front of house managers and kitchen managers?
- Do they need different access to the system? 
(issue 26)
- Including "New Employees" was intended to give gradual access to the system for employees after the initial onboarding?
- Could you please expand on your expectations for adding new employees to the system? How does the onboarding process work? 
- Should current employees retain access to onboarding documents?

### Operating Environment
(issue 28)
- Would you accept if the environment is defined as mobile, but a desktop accessible version is out of scope? Would you prefer a web application, primarily designed for mobile screens? An alternative?

### Constraints
(issue 29)
- Could you please expand on the expected number of users in the system? Your RFP mentioned 70+ users?
- Do you expect that to be all year, every year?
- How many of those users do you anticipate using the system at one time?
- Would that change at peak times (example: schedule updates)?

##Things to change
- (1)Background: Last sentence "The client wants a solution that will make managing finances, swapping shifts, and communicating with staff easier to accomplish." before the and add section about onboarding new employees. and add section about information being transferred to customers.

## Additional Questions
- We had talked about potentially including a notification feature? Unfortunately that was missed in the requirements document, but is that something you're still interested in?
   - What actions would you want notifications for (eg. schedule updates, onboarding documents, messages)?
- Do all employees clock in and out? So far all staff/users are included, is that desired? Do both types of managers also clock in and out? Bookkeepers?
- We are assuming delivery drivers do not have scheduled shifts in the system, is that correct?
- Who initiates shift swaps?
   - Once two employees have agreed, are they able to initiate the process in the system? Or does the manager make those changes?
   - Is manager approval required?
   - Does that shift swap need to occur before shift begins? What if the shift swap occurs at shift start time?
- How does it work for employees to book vacation time?
- How does it work for employees to call out sick or for call-out-of-work types of emergencies?
- How would you prefer contacting everyone on a specific shift to work?
   - Are shift groups created by default? Can you create a group when you would like to contact specific people?
   - How does that work with shift swaps?
- Do you have a preference for how security is implemented (eg. login)?
   - What information is stored about each emmployee? (We assumed: name, role, banking information, scheduled shifts, employee progress reports -> could add start date, something else?)
   - Does that information change depending on their role? (eg. manager, bookkeeper, delivery driver, etc.)
   - What information would you like employees to see about eachother?
- How long should shift information be stored in the past? How far in advance should shifts be scheduled? 
