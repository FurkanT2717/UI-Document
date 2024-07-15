# User Management Screen UI Specification

## Overview
This document provides the user interface (UI) specification for the User Management screen. The screen allows administrators to manage user accounts, including adding new users, editing existing users, and enabling or disabling users.

## Initial State
Upon loading, the User Management screen displays the following components:
- A table listing all users with columns for ID, User Name, Email, and Enabled status.
- A checkbox to toggle the visibility of disabled users.
- A button to add a new user.
- A form to enter details for a new user or to edit an existing user.

## UI Components

### 1. User Table
- **ID Column**: Displays the unique identifier for each user.
- **User Name Column**: Displays the username of each user.
- **Email Column**: Displays the email address of each user.
- **Enabled Column**: Displays the enabled status of each user as a boolean value (`true` or `false`).

### 2. Checkbox: Hide Disabled User
- **Function**: Toggles the visibility of users whose `Enabled` status is `false`.
- **Initial State**: Checked by default, meaning disabled users are hidden.

### 3. Button: New User
- **Function**: Opens the New User form on the right side of the screen.
- **Behavior**: Clicking this button clears the New User form if it contains any pre-filled data.

### 4. Form: New User / Edit User
- **Components**:
  - **Username Field**: Text input for the user's username.
  - **Display Name Field**: Text input for the user's display name.
  - **Phone Field**: Text input for the user's phone number.
  - **Email Field**: Text input for the user's email address.
  - **User Roles Dropdown**: Dropdown menu to select one or more roles for the user (Guest, Admin, SuperAdmin).
  - **Enabled Checkbox**: Checkbox to set the user's enabled status.

- **Behavior**:
  - **Username**: Required field.
  - **Display Name**: Optional field.
  - **Phone**: Optional field.
  - **Email**: Required field.
  - **User Roles**: At least one role must be selected.
  - **Enabled**: Default state is checked (enabled).

### 5. Button: Save User
- **Function**: Saves the new user or updates the existing user with the details entered in the form.
- **Behavior**: 
  - Validates required fields.
  - Displays error messages for any missing required fields.
  - Updates the user table with the new or edited user details.
  - Clears the form upon successful save.

## User Interaction

### Adding a New User
- Click the "New User" button.
- Fill in the required fields in the New User form.
- Click the "Save User" button to save the new user.
- The user table updates to include the new user.

### Editing an Existing User
- Click on a user row in the user table.
- The form populates with the selected user's details.
- Edit the user details as needed.
- Click the "Save User" button to update the user details.
- The user table updates with the edited user details.

### Hiding/Showing Disabled Users
- Check or uncheck the "Hide Disabled User" checkbox.
- The user table updates to show or hide users based on their enabled status.

## Initial Display
- The user table displays all enabled users.
- The "Hide Disabled User" checkbox is checked.
- The New User form is empty and ready for input.
- The "New User" button is visible and clickable.

## Validation Rules
- **Username**: Must be unique and not empty.
- **Email**: Must be in a valid email format and not empty.
- **User Roles**: At least one role must be selected.

## Error Handling
- Display error messages near the relevant form fields if validation fails.
- Prevent saving if any required field is invalid or empty.
- Highlight the form fields with errors.

## Accessibility Considerations
- Ensure all form fields have associated labels.
- Provide clear and concise error messages.
- Make sure the UI is navigable via keyboard.

This specification serves as a guideline for developers to implement the User Management screen. Any changes to the UI components or behavior should be documented and approved before implementation.
