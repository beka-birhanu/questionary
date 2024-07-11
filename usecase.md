# Use Cases

## Actors:

- User (Authenticated)
- Guest

## Use Case 1: Guest Registration

### Main Flow:

1. Guest navigates to the registration page.
2. System prompts for a unique username and a strong password.
3. Guest enters the information and submits the form.
4. System registers the Guest.

### Alternative Flow (Validation Error):

- If the username is not unique or the password is weak, the system displays an error and prompts the Guest to correct the information.

## Use Case 2: Guest Login

### Main Flow:

1. Guest navigates to the login page.
2. System prompts for username and password.
3. Guest enters the credentials and submits the form.
4. System validates the credentials, generates a JWT token, and starts a session.

### Alternative Flow (Invalid Credentials):

- If the credentials are invalid, the system displays an error and prompts the Guest to retry.

## Use Case 3: User Logout

### Preconditions:

- User is authenticated.

### Main Flow:

1. User selects the logout option.
2. System terminates the session.

## Use Case 4: Create Long-Term Goal Hierarchy

### Preconditions:

- User is authenticated.
- No ongoing long-term goal exists.

### Main Flow:

1. User selects the option to add a long-term goal.
2. System prompts for a title and a time duration (3 to 12 months).
3. User provides the information and submits the form.
4. System creates the long-term goal.

### Alternative Flow (Invalid Input):

- If the title is missing, the system displays an error and prompts the User to retry.

## Use Case 5: Update Long-Term Goal Hierarchy's Title

### Preconditions:

- User is authenticated.
- An ongoing or completed long-term goal hierarchy exists.

### Main Flow:

1. User selects the option to edit the hierarchy title.
2. System prompts for the new title.
3. User provides the new title and submits the form.
4. System updates and reflects the change.

### Alternative Flow (Invalid Input):

- If the title is missing, the system displays an error and prompts the User to retry.

## Use Case 6: Add a Goal to a Hierarchy

### Preconditions:

- User is authenticated.
- An ongoing hierarchy exists.

### Main Flow:

1. User selects an ongoing hierarchy to add the goal to.
2. User chooses the option to add a goal.
3. System prompts for goal title, description, time allocation, priority, and scale factor.
4. User provides the information and submits the form.
5. System adds the goal and updates the hierarchy.

### Alternative Flow (Invalid Input):

- If the title is missing, the system displays an error and prompts the User to retry.

## Use Case 7: Update Goal's Values

### Preconditions:

- User is authenticated.
- An ongoing goal exists.

### Main Flow:

1. User selects an ongoing goal to edit.
2. System provides editable fields except for time allocation.
3. User makes the desired changes and submits the form.
4. System saves and updates the goal.

### Alternative Flow (Invalid Input):

- If the title is missing, the system displays an error and prompts the User to retry.

## Use Case 8: Delete Goal or Hierarchy

### Preconditions:

- User is authenticated.
- A goal or hierarchy exists.

### Main Flow:

1. User selects the goal or hierarchy to delete.
2. System informs the User that the action is irreversible and that all nested items will be deleted.
3. System prompts for confirmation.
4. User confirms the deletion.
5. System deletes the goal or hierarchy and updates the system.

### Alternative Flow (User Declines the Request):

- System cancels the deletion and navigates the User back.
