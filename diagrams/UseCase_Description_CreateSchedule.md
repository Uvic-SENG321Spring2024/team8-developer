Name: Create Schedule

Actors: 
- Primary: Front of House and Kitchen Manager

Description: The actor assigns each shift to an employee for the next two weeks.

Trigger: Actor opens create schedule functionality of software.

Pre-Condition: 
- Actor is logged in to system.
- There is at least one employee in the system who is available to take shifts.

Post-Condition: 
- Each assigned shift is associated with an employee.

Primary flow: 
1. Actor selects an employee.
2. Actor assigns one or more shifts to the selected employee within employee's listed availability.
3. Actor repeats continues, selecting one employee at a time until all shifts are assigned.
4. Actor completes schedule creation.

Alternate Path: 

2A-1. If employee does not have listed availability, no shifts are assigned to them. \
2A-2. Actor moves on to step 3 of primary flow.

2B-1. If employee is working a maximum number of hours, no additional shifts are assigned to them. \
2B-2. Actor moves on to step 3 of primary flow.

2C-1. Actor does not assign any shifts to the selected employee. \
2C-2. Actor moves on to step 3 of primary flow.

3A-1. Actor selects an employee that was previously selected. \
3A-2. Actor assigns an additional one or more shifts to the selected employee.

Exception Path: 

2A-1. Actor cancels schedule creation. Plan is not saved. \
2A-2. Actor exits schedule creation functionality of app.

2B-1. Actor saves schedule creation plan. \
2B-2. Actor exits schedule creation functionality of app. 

3A-1. Actor cancels schedule creation. Plan is not saved. \
3A-2. Actor exits schedule creation functionality of app.

3B-1. Actor saves schedule creation plan. \
3B-2. Actor exits schedule creation functionality of app.

3C-1. Actor does not assign all shifts. \
3C-2. Actor moves on to step 4 of primary flow.

Priority: High

Frequency of Use: Every two weeks

Business Rules: There are a maximum number of hours that each person is allowed to work, both per day and per week.

Other information:

Assumptions: Shifts are scheduled in two week increments. All shifts are assigned for those two weeks during one interaction with system.
