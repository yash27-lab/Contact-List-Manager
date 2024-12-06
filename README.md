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
