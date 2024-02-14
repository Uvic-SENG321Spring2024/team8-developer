Name: Post Shift Swap
Actors: Primary: Kitchen and Front of House Staff.
Description: The Actor selects a shift that they do not want to work, they post it to be available for other employees to take.
Trigger: Actor opens shift swap functionality of software.
Pre-Condition: Actor is logged in to system. Actor has selected the shift swap menu. The Actor has been scheduled for a shift.
Post-Condition: The shift is posted and available for other employees to take.
Primary flow: 1. Actor selects desired shift to post from their schedule. 2. They select the option to share the shift to all employees. 3. They select the option to post the shift now.
Alternate Path: 1. Actor selects desired shift to post from their schedule. 2. They select the option to share the shift to a specific employee. 3. They select the option to post the shift now.
Exception Path: 2. Actor selects a shift that they do not work.  2. The system informs them they do not work this shift, so they cannot post it. 3. The employee chooses a different shift to psot.
Priority: None
Frequency of Use: Daily
Business Rules: Kitchen Staff can only pick up shifts from other Kitchen Staff, and Front of House can only pick up shifts from other Front of House staff.
Other information:
Assumptions:  It has been assumed that only Front of House and Kitchen Staff need to swap shifts through the system.  
