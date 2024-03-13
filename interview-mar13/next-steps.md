# Tasks to Improve RD

## GitHub Issues
Issue 67
- Go through entire document and use staff consistently
   - Where appropriate use individual user classes
- Reword glossary definition to make is less confusing/contradictory
   - ie. referring to staff as containing 3 different user classes unless otherwise stated makes reading parts of the document confusing

Issue 68
- Replace "scheduler" with "Scheduling and Time Tracking System" or "system"
- SCH-3 remove the word only 
- SCH-6/18 remove or rewrite negative functional requirements
   - possible fix SCH-6: The system must allow modification of a shift if the shift is in the future.
   - possible fix SCH-18: Only allow shift swaps when the employee is free to take the shift from start time to end time.
- SCH-11 make sentence more clear
- SCH16/17 use "a Manager" instead of just "Manager"
- User Story 6: fix type of duplicate "accurately" in acceptance criteria
- Update user story 3
   - Add acceptance criteria that changes made to schedule must be consistent with changes made by manager
   - Split into different user stories? One for each edit schedule to update, add, and remove shifts? (or justify why not)
- Split user story 10
   - Seeing monthly and weekly are different user stories
   - Seeing personal and all employees schedules are different user stories
- Storyboard not as screenshot of prototype? TODO Discuss 

Issue 69
- COM-2 specify company-wide meaning (ie. send to all employees of Banter Ice Cream)
- Add requirements for send accouncements grouped by location or user classes
- COM-5 what "tailored interfaces and features" are necessary in communication system? Which user classes have access?
- Storyboards add details of which users/what steps they are taking to navigate prototype

Issue 70
- Spelling mistakes in Recipe Management (5.iii) (consider spell checking entire document?)
- UC-1 Why is this manager authenticated but others are not?
- Add preconditions to first storyboard panel? TODO Discuss

Issue 71
- When specifying an action check capitalizing words including, but not limited to such as "Delete", "Create"
- Specify "user"
- Respond to ACC-9 as determined in demo/interview TODO Discuss
- User Story 5 respond as determined in demo/interview TODO Discuss

Issue 76
- Explain that "n" means an unlimited number in description (according to textbook)

Issue 77
- UML class diagram: where appropriate replace "1..\*" with "0..\*"? 
   - Note that the 1 or 0 represents the number of associated entities. eg. Announcement can have 0 to many Reactions, but Reaction is only to 1 Announcement
- Is it possible to identify specific users that can take action in UML Class and ER Diagrams? TOOD Discuss
   - It may be possible, see this: https://www.visual-paradigm.com/guide/uml-unified-modeling-language/how-to-model-constraints-in-uml/ 

Issue 78
- DFD0/1: "If I look at an entity, I should see all data flow from the entity without having to refer to another entity?" as determined in demo/interview TODO Discuss
- Explain "All Users" (Note this is already in the description of the diagram)
   - Explain Delivery Drivers do have scheduled shifts, just accessed through "All Users"
- Consider adding clock in/clock out to Bookkeeper/Manager as determined in interview/demo TODO Discuss
- DFD2 View Tracked Hours and DFD1, are they consistent?

## Prototype Demo/Walkthroughs
- Add here
