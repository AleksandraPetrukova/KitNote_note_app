# KitNote_note_app

## [MySQL]
**- table 1 - notes**
    1. id - primary key
    2. text
    3. userID
    4. isdeleted (true/false)
    5. ischecked (true/false)
    6. timestamp
**- table 2 - users**
    1. userID - primary key
    2. email
    3. username
    4. password
    5. timestamp

## [PHP/MySQL]
- UPDATE
- INSERT
- SELECT
	
## [JS]
**User Authentication:**
1. Loading page: - Set 1.5 second to load the page
2. Login: - Authenticate users with their email address and password. - Display a greeting messages, an input field, and input data to the user. - Allow users to logout
3. Signup: - Allow users to create an account with a unique username and password. - Validate user inputs and store user information securely. - Check if email is already exists - Check if confirmation password is correct - Display a greeting messages and an input field to the user. - Allow users to logout
4. Logout: - Allow users to log out, terminating their session. - Redirect them to the login page after logout.
**Todo List Functionality:**
1. Change Color: - Change the color of a todo item to indicate its completion status (done/not done). - Update the item's status in the database upon toggling.
2. Show Data: - Display todo items, excluding deleted ones. - Fetch and display data individually from the database.
3. Show Characters Left: - Display the number of characters left while typing in a new todo.
4. Deactivate POST Button: - Disable the POST button when the character limit is exceeded.
5. Filter and Display Buttons: - Implement buttons to filter and display todo items: - Show all items - Shuffle items randomly - Show checked notes - Show in-progress items
6. Update Button: - Allow users to update a todo item's details. - Display the previous information in input fields. - Update the item and the timestamp.

## [PHP]
**- delete.php:** Update the "isDelete" field in the database to indicate deletion by setting it to true (1) from false (0). The deletion query is excluded based on a recommendation from a teacher.
**- insert.php:** Perform an insertion operation to add a new note to the database. Ensure that the note fields are not empty or contain only spaces before performing the insertion.
**- log_in.php:** Verify the existence of the user in the system. If the user exists, compare the hashed password with the stored password in the database. If both checks pass successfully, store the user's information in a session.
**- log_out.php:** Log out the user by terminating and destroying their active session.
**- select.php:** Retrieve notes from the "notes" table that are associated with the same userID as the current session.
**- sign_up.php:** Check whether there is an existing user with the same email in the database. If no such user exists, insert a new user record into the "users" table. Automatically log in the newly registered user by storing their information in the session.
**- update_checked.php:** Update the "isChecked" field in the database to toggle between true (1) and false (0).
**- update_note.php:** Update the subject or text of a note in the "notes" table. Also, update the timestamp to reflect the most recent modification.

## [Features]
- Login: If the entered email does not exist, an error message is displayed.
- Login: If the entered password does not match the one stored in the database, an error message is shown.
- Sign Up: During the registration process, the system verifies that the password contains at least 9 characters.
- Sign Up: The system ensures that the entered password and password confirmation match.
- Sign Up: It checks whether the user already exists, and if so, an error message is presented.
- Note: Any input field containing white spaces or lacking subject/text will trigger an error.
- Note: If the character count of a note exceeds 600, the send button is deactivated.
- Note: Allows users to edit existing notes.
- Note: Users can check/uncheck notes as needed.
- Note: Provides the option to delete notes.
- Note: Offers data filtering options, including shuffling, displaying checked notes, and showing notes in progress.
- Log Out: Allows users to log out of the system.
- Session keeps running even when you refresh the page
