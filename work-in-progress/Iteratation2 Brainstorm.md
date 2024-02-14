# Iteration 2 Brainstorm

Sections 5, 6, and 8

Date: Started February 12, 2024 (in class) and continued throughout week

## Use Case Diagrams
### Schedule System
| Use Case              | Actor(s)  | Includes     | Extends |
|-----------------------|-----------|--------------|---------|
| View Schedule         | All Staff |              |         |
| Manage Schedule       | Manager   |              |         |
| Swap Shifts           | All Staff | Approve Swap |         |
| Indicate Availability | All Staff |              |         |
| Clock In           | All Staff (except Manager?) |          |         |
| Clock Out          | All Staff (except Manager?) |          |         |
| View Tracked Hours | Bookkeepers                 |          |         |
|                    |                             |          |         |

### Communication System
| Use Case                      | Actor(s)  | Includes | Extends |
|-------------------------------|-----------|----------|---------|
| Send Message                  | All Staff |          |         |
| Receive Message               | All Staff |          |         |
| Edit Message                  | All Staff |          |         |
| View Message                  | All Staff |          |         |
| Send Announcement             | Manager   |          |         |
| Receive Announcement          | All Staff |          |         |
| Edit Announcement             | Manager   |          |         |
| View Announcement             | All Staff |          |         |
| View Announcement Information | Manager?  |          |         |
| React Announcement            | All Staff |          |         |
|                               |           |          |         |

### Recipe Management System
| Use Case    | Actor(s)                                        | Includes | Extends |
|-------------|-------------------------------------------------|----------|---------|
| View Recipe | Front of House (limited), Kitchen, and Managers |          |         |
| Add Recipe  | Manager                                         |          |         |
| Edit Recipe | Manager                                         |          |         |
|             |                                                 |          |         |

### Onboarding Materials System
| Use Case    | Actor(s)                                        | Includes | Extends |
|-------------|-------------------------------------------------|----------|---------|
|  | All staff |          |         |

## Entity Relationship Diagram
- Current Entities:
   - Employee (Name, Role, Location(s), Banking Info, ?)
   - Shift (Start Date/Time, End Date/Time, Employee, Role?, Location, ?) 
   - Schedule (Employee, Shifts, ?)
   - Announcement (Author, Contents, Files, Reacts, Views, ?)
   - Message (Author, Contents, Files, ?)
   - Recipe (Author, isActive, Name, Ingredients, Allergens, Directions, ?)
