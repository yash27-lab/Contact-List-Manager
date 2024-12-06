# Overview

The Contact List program is a simple command-line application that allows users to manage their personal contacts. The program supports adding, deleting, listing, and searching contacts, and all contact information is stored persistently in a JSON file. The application ensures that each contact is unique by requiring a unique combination of first and last names.

# Features

The application provides the following commands:

add: Adds a contact to the contact list.

delete: Deletes a contact from the contact list using the first and last name.

list: Lists all contacts in alphabetical order by the first name.

search: Searches for contacts by their first and last name.

q: Quits the program and saves all of the current contacts to a JSON file.

Data Persistence

Contacts are stored persistently in a contacts.json file, allowing the data to be retained between program executions. This is achieved by reading the contacts from the JSON file when the program starts and saving them when the program ends.


# Commands and Validation

Add a Contact:

Prompts the user for first name, last name, mobile phone number, home phone number, email address, and physical address.

Ensures phone numbers are valid (10 digits) and email addresses are properly formatted.

Rejects duplicate contacts with the same first and last name.

Delete a Contact:

Prompts for first and last name to identify the contact.

Asks for confirmation before deletion.

List Contacts:

Displays all saved contacts in alphabetical order by first name.

Shows optional details such as phone numbers, email, and address if they are available.

Search Contacts:

Allows searching by partial or full first and last name.

Displays the matching contacts in alphabetical order.

# Code Overview

The program is structured into several functions to modularize the tasks:

load_contacts(): Loads the contact list from the contacts.json file.

save_contacts(): Saves the contact list to the contacts.json file.

is_valid_phone_number(phone_number): Validates that a phone number contains exactly 10 digits.

is_valid_email(email): Validates that an email address is in a valid format.

add_contact(contacts): Adds a new contact to the list, ensuring that all data is valid.

delete_contact(contacts): Deletes a contact based on the first and last name.

list_contacts(contacts): Lists all contacts in alphabetical order.

search_contacts(contacts): Searches for contacts using the given first and last name.

main(): The main loop that runs the command-line interface.

# Validations and Error Handling

Phone Numbers: Must contain exactly 10 digits; otherwise, the program will reject the input.

Emails: Must follow a standard email format; otherwise, the program will reject the input.

Duplicate Contacts: The program ensures that no two contacts have the same first and last names.

Confirmation Prompts: For deleting a contact, the user must confirm the action.

# Future Enhancements

User Authentication: Add a login system to allow multiple users to manage their own contacts.

Graphical User Interface (GUI): Implement a GUI to make the program more user-friendly.

Export/Import Contacts: Allow exporting contacts to CSV or importing contacts from external files.
