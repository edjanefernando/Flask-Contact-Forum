# Flask-Contact-Forum
The project involves creating a responsive contact form using Flask and Python. The form will validate user input and provide error messages if any fields are not filled out correctly

# Skills Acquired:
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

# Flask Web Framework
What is Flask?
Flask is a lightweight web framework for Python, often referred to as a microframework. This is because it doesn’t require any particular tools or libraries to operate. Unlike larger frameworks, Flask doesn’t come with built-in components for database management or form validation. Instead, it relies on extensions to add these functionalities, integrating them seamlessly as if they were part of the core framework. There are extensions available for various tasks, including database operations, form validation, file uploads, and authentication. Flask's design philosophy is to enable developers to quickly start building web applications, offering flexibility to choose the tools and libraries that best suit their needs.

Key Features of Flask
- Minimalistic: Flask offers the essential tools to set up a web server with minimal configuration. It doesn’t include default components like databases or form handling, providing developers the freedom to include only the necessary features.

- Modular and Extensible: Flask is designed to be extended through the use of extensions. These extensions add functionality such as database integration, form validation, and file handling, as if they were native to Flask.

- Built-in Development Server and Debugger: Flask comes with an integrated development server and debugger, streamlining the development process and enhancing productivity.

- RESTful Request Handling: Flask simplifies the creation of RESTful APIs by providing tools for managing HTTP requests and routing URLs to specific code functions.

- Jinja2 Templating: Flask utilizes the Jinja2 templating engine, allowing developers to separate HTML from Python code effectively.

  ![image](https://github.com/edjanefernando/Flask-Contact-Forum/assets/141014730/740883aa-569f-4381-92ca-0480b2b042a6)


# How to Run a Flask Application
Ensure Python is Installed:
Make sure you have Python installed on your system.

Install Flask:
Use pip to install Flask by running the following command:

bash
Copier le code
pip install Flask
Save Your Code:
Save your Flask code in a file named app.py.

Run the Application:
Execute the following command to start your Flask application:

bash
Copier le code
python app.py
View the Application:
Open a web browser and navigate to http://127.0.0.1:5000/ to see your application in action. If you are using Visual Studio Code, you can simply click on the link displayed in the terminal.


# Flask and Web Security
Flask provides several mechanisms to enhance web security and protect against common vulnerabilities such as Cross-Site Scripting (XSS) and Server-Side Template Injection (SSTI):

Input Sanitization and Validation:

It's crucial to sanitize and validate all user inputs on the server side to prevent malicious input from compromising your application.
Output Escaping with Jinja2 Templating:

Flask's default templating engine, Jinja2, automatically escapes user inputs when rendering templates. This helps prevent XSS attacks by converting potentially dangerous characters into their HTML entity equivalents.
CSRF Protection:

Cross-Site Request Forgery (CSRF) attacks can be mitigated using Flask extensions like Flask-WTF, which generates and verifies CSRF tokens for forms. This ensures that form submissions originate from your own site and not from a malicious source.
Content Security Policy (CSP):

Implementing a Content Security Policy (CSP) header helps mitigate XSS attacks by specifying which resources (scripts, stylesheets, etc.) can be loaded by the browser. Flask allows you to set HTTP headers, including CSP, to restrict the sources from which certain types of content can be loaded.

# Project Setup
- Install Flask using your terminal: pip install Flask
- Setting Up Your Project in Visual Studio Code:
* Create a directory structure for your Flask project.
* Link this directory to Visual Studio Code for easy editing and management.
- Creating Necessary Files:

* Prepare your project files such as app.py (for your Flask application logic), contact.html (for the contact form), and thank_you.html (for the confirmation page).

- Development Process:

* Write the necessary code in app.py to handle routes, form submissions, and rendering templates using Flask and Jinja2.
* Implement server-side validation and sanitization for form inputs to ensure data integrity and security.
* Use Flask-WTF or manual CSRF protection techniques to safeguard your forms from CSRF attacks.
* Set appropriate security headers, including CSP, to enhance your application's security posture.

Here below you can see the results:

![image](https://github.com/edjanefernando/Flask-Contact-Forum/assets/141014730/5c921be9-bfe2-4a54-9762-30ff11e509c3)

![image](https://github.com/edjanefernando/Flask-Contact-Forum/assets/141014730/7f718c34-7336-4d90-9ac6-8228e6a90fa4)



Miscellaneous
Understanding POST and GET Requests
POST Request:

In a POST request, data is sent within the body of the HTTP request. It's suitable for transmitting sensitive information like passwords or credit card details. This method is typically used for operations that modify server state, such as submitting forms.
GET Request:

A GET request sends data via the URL as request parameters. It's used to fetch resources from the server and is less secure for sensitive data because the data is visible in the URL. GET requests are typically used for non-destructive operations like retrieving data.
Protecting Against XSS Vulnerabilities
What is XSS?

- Cross-Site Scripting (XSS) is a security vulnerability that allows attackers to inject malicious scripts into web pages viewed by other users. These scripts can execute arbitrary code in the victim's browser, potentially compromising their data or session.
# Types of XSS Attacks:

- Stored XSS: Malicious scripts are stored on the server and served to users when they access a page. Example: injecting a script into a forum post.
- Reflected XSS: Scripts are reflected off a web server, often through URLs or form inputs, and executed immediately. Example: sending a victim a link containing a script.
- DOM-based XSS: The vulnerability lies in client-side JavaScript that modifies the Document Object Model (DOM), allowing scripts to execute in the browser.

** Protecting Against XSS:

* Sanitize and Validate Inputs: Always sanitize and validate user inputs on the server side to prevent malicious input from compromising your application.
* Escape Outputs: Use Flask’s capabilities to automatically escape user inputs before rendering them in HTML, mitigating XSS risks.
* Content Security Policy (CSP): Implement CSP headers to restrict which resources can be loaded by the browser, thereby reducing XSS attack surface.

# Using Flask for Web Security
# Flask Security Measures:

- Sanitizing and Validating Inputs: Flask enables developers to sanitize and validate user inputs to prevent malicious data from entering the application.
- Output Escaping: Flask's templating system ensures that user inputs are automatically escaped when rendered in HTML, preventing XSS vulnerabilities.
- CSRF Protection: Implement CSRF tokens with Flask-WTF or similar extensions to protect against Cross-Site Request Forgery attacks, ensuring that form submissions originate from trusted sources.
- HTTP Headers: Set appropriate HTTP headers, including Content Security Policy (CSP), to enhance security by controlling how resources are loaded in the application.
** Example of Protecting Against XSS in Flask:
![image](https://github.com/edjanefernando/Flask-Contact-Forum/assets/141014730/b21efccd-36cd-403f-b147-2408ddde4951)


In this example, the html_sanitizer library is used within a Flask route to sanitize user inputs (first_name and last_name) before processing them, thereby mitigating potential XSS vulnerabilities.


# Protecting Against Server-Side Template Injection (SSTI) Attacks
** What is SSTI?

- Server-Side Template Injection (SSTI) is a security vulnerability where attackers inject malicious code into a template. This code is then executed on the server, potentially compromising sensitive data or gaining control over the server.
How SSTI Works:

- Templating Engines: Web applications use templating engines (like Jinja2, Twig, or EJS) to dynamically generate HTML pages.
- User Input: If user input is not properly sanitized or validated before being included in templates, it can lead to SSTI.
- Execution: Malicious code injected into a template is executed on the server, allowing attackers to access sensitive information or perform unauthorized actions.
** Example of Vulnerable Code:
  ![image](https://github.com/edjanefernando/Flask-Contact-Forum/assets/141014730/5f127773-549c-4ef4-b77b-eb887ba3155c)

  # Why is it Vulnerable?

- User Input: The code retrieves user input (name) from a query parameter without proper validation.
- Template Injection: User input is directly inserted into the template string (template = f"Hello, {name}!").
- Rendering: The template is rendered using render_template_string, which processes the input as part of the template.
This allows attackers to inject malicious template code via the name parameter, potentially executing it on the server.

** Consequences of SSTI Attacks:

- Data Theft: Access sensitive information such as database credentials or server files.
- Remote Code Execution: Execute arbitrary code on the server, gaining full control.
- Defacement: Modify the appearance or content of the website to deceive or disrupt users.

** Prevention and Mitigation:

- Input Validation: Validate and sanitize all user inputs before incorporating them into templates.
- Use Safe Functions: Use templating engine functions designed to handle user inputs securely.
- Template Escaping: Escape special characters in templates to prevent them from being interpreted as code.
Example of Prevention Using Flask:

![image](https://github.com/edjanefernando/Flask-Contact-Forum/assets/141014730/24dfc845-143c-4d05-870b-e2b6df7ce8ca)

** In this example:

The escape function from the html module is used to sanitize the name parameter by escaping special characters.
This ensures that any user input is treated as plain text and not executable code within the template, thereby preventing SSTI vulnerabilities.





