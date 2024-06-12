# Flask-Contact-Forum
The project involves creating a responsive contact form using Flask and Python. The form will validate user input and provide error messages if any fields are not filled out correctly

#Skills Acquired:
- Backend Development: Introduction to Python programming and logical structures.
- Form Sanitization and Validation: Ensuring data integrity and security.
- HTTP Methods: Implementation of POST and GET requests.
- Template Rendering: Using Jinja to dynamically generate HTML content.
# Project Overview:
* Hackers Poulette™ specializes in selling DIY kits and accessories for Raspberry Pi. They need a solution for users to reach their technical support team. Your task is to create a Python-based application that displays a contact form and handles the form submission by sanitizing, validating, and providing feedback to the user.

# Performance Requirements:
- Error Handling: If the user makes an error, the form should be re-displayed with previously entered valid data retained in their respective fields.
- Error Messages: Display error messages near the relevant fields.
- Server-side Processing: Perform sanitization and validation on the server side.
- Success Response: Upon successful sanitization and validation, display a "Thank you for contacting us" page that summarizes the submitted information.
- Spam Prevention: Implement a honeypot technique to prevent spam.
# Form Fields:
* Mandatory Fields: First Name, Last Name, Email, Country (dropdown list), Message, Gender (radio buttons for M/F).
Optional Field: Subject (checkboxes for Repair, Order, Others; default to Others if none selected).
