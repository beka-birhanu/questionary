# Use Cases

## Actors

- **User** (Authenticated)
- **Guest**

## Use Case 1: Guest Registration

### Main Flow

1. Guest navigates to the registration page.
2. System prompts for a unique username and a strong password.
3. Guest enters the information and submits the form.
4. System registers the Guest.

### Alternative Flow

- **Validation Error**: If the username is not unique or the password is weak, the system displays an error and prompts the Guest to correct the information.

## Use Case 2: Guest Login

### Main Flow

1. Guest navigates to the login page.
2. System prompts for username and password.
3. Guest enters the credentials and submits the form.
4. System validates the credentials, generates a JWT token, and starts a session.

### Alternative Flow

- **Invalid Credentials**: If the credentials are invalid, the system displays an error and prompts the Guest to retry.

## Use Case 3: User Logout

### Preconditions

- User is authenticated.

### Main Flow

1. User selects the logout option.
2. System terminates the session.

## Use Case 4: Create Long-Term Hierarchy

### Preconditions

- User is authenticated.
- No ongoing long-term Hierarchy exists.

### Main Flow

1. User selects the option to add a long-term Hierarchy.
2. System prompts for a title and a time duration (3 to 12 months).
3. User provides the information and submits the form.
4. System creates the long-term Hierarchy.

### Alternative Flow

- **Invalid Input**: If the title is missing, the system displays an error and prompts the User to retry.

## Use Case 5: Create Short-Term Hierarchy

### Preconditions

- User is authenticated.
- An ongoing long-term hierarchy exists.

### Main Flow

1. User selects the option to add a short-term hierarchy.
2. System prompts for a title and a time duration (1 month to the encompassing long-term hierarchy).
3. User provides the information and submits the form.
4. System creates the short-term hierarchy.

### Alternative Flow

- **Invalid Input**: If the title is missing, the system displays an error and prompts the User to retry.

## Use Case 6: Update Hierarchy's Title

### Preconditions

- User is authenticated.
- An ongoing hierarchy exists.

### Main Flow

1. User selects the option to edit the hierarchy title.
2. System prompts for the new title.
3. User provides the new title and submits the form.
4. System updates and reflects the change.

### Alternative Flow

- **Invalid Input**: If the title is missing, the system displays an error and prompts the User to retry.

## Use Case 7: Extend Hierarchy

### Preconditions

- User is authenticated.
- A closed hierarchy exists.

### Main Flow

1. User selects the closed hierarchy to extend from.
2. System prompts the user with the same form as creating a hierarchy.
3. User provides the required input and submits.
4. System creates the hierarchy and takes the progress statistics from the base hierarchy and passes it to the new one.

### Alternative Flow

- **Invalid Input**: If the title is missing, the system displays an error and prompts the User to retry.

## Use Case 8: Close Hierarchy

### Preconditions

- User is authenticated.
- An ongoing hierarchy exists.

### Main Flow

1. User selects an ongoing hierarchy.
2. User selects an option to close the hierarchy.
3. System informs the user all nested goals and hierarchy will be closed with their current state.
4. System prompts for confirmation.
5. User confirms to continue.
6. System closes the hierarchy and all the underlying goals and sub-goals.

### Alternative Flow

- **User Declines the Request**: System cancels the closure and navigates the User back.

## Use Case 9: Add a Goal to a Long-Term Hierarchy

### Preconditions

- User is authenticated.
- An ongoing long-term hierarchy exists.

### Main Flow

1. User chooses the option to add a goal.
2. System prompts for goal title, description, time allocation, priority, and scale factor.
3. User provides the information and submits the form.
4. System adds the goal.

### Alternative Flow

- **Invalid Input**: If the title is missing, the system displays an error and prompts the User to retry.

## Use Case 10: Add a Goal to a Short-Term Hierarchy

### Preconditions

- User is authenticated.
- An ongoing short-term hierarchy exists.

### Main Flow

1. User chooses the option to add a goal.
2. System previews long-term goals.
3. System prompts user to select one of the long-term goals to link this long with.
4. User select the long-term goal to link.
5. System prompts for goal title, description, time allocation, priority, and scale factor.
6. User provides the information and submits the form.
7. System adds the goal.

### Alternative Flow

- **Invalid Input**: The system displays an error and prompts the User to retry.

## Use Case 10: Add a Goal to a Weekly Hierarchy

### Preconditions

- User is authenticated.
- An ongoing short-term hierarchy exists.

### Main Flow

1. User chooses the option to add a goal.
2. System previews short-term goals.
3. System prompts the user to select one of the short-term goals to link with this goal.
4. User selects the short-term goal to link.
5. System prompts for goal title, description, time allocation, priority, and scale factor.
6. Time allocation must be from the current day to a maximum of the upcoming Sunday.
7. User provides the information and submits the form.
8. System adds the goal.

### Alternative Flow

- **Invalid Input**: The system displays an error and prompts the User to retry.

## Use Case 11: Update Goal's Values

### Preconditions

- User is authenticated.
- An ongoing goal exists.

### Main Flow

1. User selects an ongoing goal to edit.
2. System provides editable fields except for time allocation.
3. User makes the desired changes and submits the form.
4. System saves and updates the goal.

### Alternative Flow

- **Invalid Input**: The system displays an error and prompts the User to retry.

## Use Case 12: Close a Goal

### Preconditions

- User is authenticated.
- An ongoing goal exists.

### Main Flow

1. User selects an ongoing goal.
2. User selects an option to close the goal.
3. System informs the user all nested goals and schedules will be closed with their current state.
4. System prompts for confirmation.
5. User confirms to continue.
6. System closes the goal and all the underlying goals and sub-goals.

### Alternative Flow

- **User Declines the Request**: System cancels the closure and navigates the User back.

## Use Case 13: Delete Goal or Hierarchy

### Preconditions

- User is authenticated.
- A goal or hierarchy exists.

### Main Flow

1. User selects the goal or hierarchy to delete.
2. System informs the User that the action is irreversible and that all nested items will be deleted.
3. System prompts for confirmation.
4. User confirms the deletion.
5. System deletes the goal or hierarchy and all nested items and updates the system.

### Alternative Flow

- **User Declines the Request**: System cancels the deletion and navigates the User back.

## Use Case 14: Plan a Daily Schedule

### Preconditions

- User is authenticated.
- An ongoing weekly goal exists.

### Main Flow

1. User selects a day from the current weekly goals window.
2. User chooses the option to add a schedule.
3. System displays short-term goals and daily events from the calendar.
4. System prompts the user to select a weekly goal to link with this schedule.
5. User selects a weekly goal to link.
6. System prompts the user for goal title, description, time allocation, and scale factor.
7. System prompts for metric titles.
8. System checks for time allocation conflicts with other schedules.
9. User provides the required information and submits the form.
10. System adds the schedule.
11. System displays information about total working hours and free hours.

### Alternative Flow:

- **Time Allocation Conflict**: The system displays an error and prompts the user to retry.

## Use Case 15: Update a Daily Schedule

### Preconditions

- User is authenticated.
- An ongoing daily schedule exists.

### Main Flow

1. User selects the option to edit the schedule.
2. System provides editable fields and delete options for each task.
3. System checks for time allocation conflicts with other schedules.
4. User provides the updated information and submits the form.
5. System updates the schedule.
6. System displays information about total working hours and free hours.

### Alternative Flow:

- **Time Allocation Conflict**: The system displays an error and prompts the user to retry.

## Use Case 16: Mark Task as Done

### Preconditions

- User is authenticated.
- An ongoing daily schedule exists.

### Main Flow

1. User selects the option to mark a task as done.
2. System prompts the user to fill out the metrics.
3. User provides the required information and submits the form.
4. System marks the task as done.
5. System displays information about the total contribution gained from the task.

### Alternative Flow:

- **Invalid Input**: The system displays an error and prompts the user to retry.

## Use Case 17: Sending Connect Request to Users

### Preconditions

- User is authenticated.

### Main Flow

1. User selects the option to connect with users.
2. System prompts the user to enter the username of the users they want to connect with.
3. User provides the username.
4. System sends the connection request.

### Alternative Flow:

- **Username Does Not Exist**: The system displays an error and prompts the user to retry.

## Use Case 18: Managing Connect Requests

### Preconditions

- User is authenticated.
- A connection request exists.

### Main Flow

1. User navigates to the manage requests section.
2. System displays a list of connection requests with the information of who sent them.
3. User accepts or declines the request.
4. System performs the corresponding action.

## Use Case 19: Share a Goal

### Preconditions

- User is authenticated.
- An ongoing goal exists.
- User has connections.

### Main Flow

1. User navigates to the goal they want to share.
2. User selects the option to share a goal.
3. System prompts the user to select a connection from the list of connections.
4. User selects the user they want to share the goal with.
5. System prompts the user to choose one of three options: include all sub-goals and schedules by default, not include any, or interactive selection.

#### User Chooses Include All by Default:

6. User selects the "include all by default" option.
7. System shares all the sub-goals and schedules with the selected contact.

#### User Chooses Don't Include Any by Default:

6. User selects the "don't include any by default" option.
7. System shares only the selected goal with the selected contact.

#### User Chooses Interactive Selection:

6. User selects the "interactive selection" option.
7. System displays the list of sub-goals and schedules.
8. System prompts the user to select from the list.
9. User selects from the list and submits.
10. System shares only the selected goals with the selected contact.

## Use Case 20: Manage a Shared Goal

### Preconditions

- User is authenticated.
- User has connections.
- User has shared a goal.

### Main Flow

1. User navigates to the shared goals list.
2. System provides a list of connections with whom they shared a goal.
3. User selects a connection.
4. System provides the list of goals and schedules shared with that connection.
5. User selects the option to manage the shared goals.
6. System provides options to remove goals alongside the list of shared goals.
7. User manages the goals and submits.
8. System prompts the user for confirmation.
9. User confirms.
10. System updates the sharing state accordingly.
