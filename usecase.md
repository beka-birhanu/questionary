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
