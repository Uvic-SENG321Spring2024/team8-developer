# Tasks to Improve RD

## Overall
- Use "Staff", "Employee", and "User" consistently (RE: Issue 67)
   - User if all users of system regardless of user class, otherwise specify user class
   - Don't use staff/employee
   - Update glossary accordingly
- Spellcheck entire document

## Section 5 
### Schedule
- Replace "scheduler" in functional requirements with "system" (RE: Issue 68)
- SCH-3 remove the word only (RE: Issue 68)
- SCH-6/18 remove or rewrite negative functional requirements (RE: Issue 68)
   - possible fix SCH-6: The system must allow modification of a shift if the shift is in the future.
   - possible fix SCH-18: Only allow shift swaps when the employee is free to take the shift from start time to end time.
- SCH-11 make sentence more clear (RE: Issue 68)
- SCH16/17 use "a Manager" instead of just "Manager" (RE: Issue 68)
- User Story 6: fix type of duplicate "accurately" in acceptance criteria (RE: Issue 68)
- Update user story 3 (RE: Issue 68)
   - Add acceptance criteria that changes made to schedule must be consistent with changes made by manager
   - Split into different user stories? One for each edit schedule to update, add, and remove shifts? (or justify why not)
- Split user story 10 
   - Seeing monthly and weekly are different user stories (RE: Issue 68)
   - Seeing personal and all employees schedules are different user stories (RE: Issue 68)
   - Add seeing a day view (RE: prototype feedback)
- Allow bookkeeper to clock in/out (Use Case Diagram, Requirements, User Story, Storyboard Descriptions) (RE: prototype feedback)
- Add more detail to download of tracked hours in functional requirement/use cases? (RE: prototype feedback)
- Resume draft in create workflow in storyboard? (RE: prototype feedback)
- Update storyboards to focus on user role/intentions, not the specifics of the prototyped UI (RE: Issue 68, prototype feedback)

### Communication and Announcement
- COM-2 specify company-wide meaning (ie. send to all employees of Banter Ice Cream) (RE: Issue 69)
- Add requirements for send accouncements grouped by location or user classes (RE: Issue 69)
- COM-5 what "tailored interfaces and features" are necessary in communication system? Which user classes have access? (RE: Issue 69)
- Prototype should show reactions (RE: prototype feedback)
   - any user can react with an emoji
   - manager can see all reactions/who reacted/when they reactions (similar to views)
- Prototype should be more clear that announcements have newest on top (RE: prototype feedback)
   - Consider if unread announcements are on top?
- Update storyboards to focus on user role/intentions, not the specifics of the prototyped UI (RE: Issue 69, prototype feedback)

### Recipe
- UC-1 Why is this manager authenticated but others are not? (RE: Issue 70)
- Update storyboards to focus on user role/intentions, not the specifics of the prototyped UI (RE: Issue 70, prototype feedback)

### Onboarding
- Remove "only" from functional requirements (RE: Issue 73)
- Update storyboards to focus on user role/intentions, not the specifics of the prototyped UI (RE: Issue 73, prototype feedback)
- Update prototype and related documents with below (RE: Issue 73, prototype feedback)
   - create/edit flows can assign materials to user's positions, then only those positions can view
   - Manager can view all when creating/editing? 

### Accounts
- When specifying an action check capitalizing words including, but not limited to such as "Delete", "Create" (RE: Issue 71)
- Specify "user" meaning? - should be added to glossary in another task (RE: Issue 67, 71)
- Change ACC-9 requirement to logout automatically after 1 hour of application being closed (RE: Issue 71, prototype feedback)
- User Story 5 include details of what payment information (RE: Issue 73, prototype feedback)
   - Add user story/requirement for bookkeeper to access payment information
   - Consider other ways to make clear that not even the user inputting the payment info can view it after it is saved

## Section 6
### Entity Relationship Diagram and UML Class Diagram
- UML class diagram: where appropriate replace "1..\*" with "0..\*" (RE: Issue 77)
   - Note that the 1 or 0 represents the number of associated entities. eg. Announcement can have 0 to many Reactions, but Reaction is only to 1 Announcement
- Identify specific users that can take action/be related to certain entities in UML Class and ER Diagrams? (RE: Issue 77, prototype feedback) 
   - Try this: https://www.visual-paradigm.com/guide/uml-unified-modeling-language/how-to-model-constraints-in-uml/ 

### Data Dictionary
- Explain that "n" means an unlimited number in description (according to textbook) (RE: Issue 76)

## Section 9
### Data Flow Level 0/1
- Consider alternatives to "All Users" if possible
   - Explain Delivery Drivers do have scheduled shifts, just accessed through "All Users"
- Add clock in/clock out flows to bookkeepers

### Data Flow Level 2
- DFD2 View Tracked Hours and DFD1, are they consistent?
