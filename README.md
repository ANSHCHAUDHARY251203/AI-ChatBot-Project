# AI-ChatBot-Project
This project implements a basic AI chatbot functionality that automates email notifications for room booking requests using Python. The chatbot collects user input such as phone number, booking date, and time, then constructs and sends a structured email to a designated recipient via SMTP (Simple Mail Transfer Protocol) using Gmail's SMTP server.


Overview:
This project is a Python-based AI chatbot component designed to automate the process of notifying hotel or room booking staff about new customer reservations. When a user provides booking details (such as date, time, and contact number) via a chatbot interface, this system automatically generates and sends an email containing those details to a designated recipient (e.g., hotel front desk or booking team). The objective is to streamline communication and reduce the delay between a user’s booking request and administrative action.

Objectives:
Automate email notifications for room bookings made via chatbot or online form.

Minimize manual intervention and errors in processing booking requests.

Ensure reliable and secure communication using standard email protocols.

Build a lightweight, easily integrable module for larger chatbot systems.

Key Features:
Email Integration via SMTP:

Connects to Gmail’s SMTP server using TLS encryption.

Authenticates the sender using Gmail App Password (ensures secure login).

Sends well-formatted emails with booking details to a specified recipient.

Dynamic Message Generation:

Retrieves dynamic inputs: customer phone number, booking date, and booking time.

Formats a human-readable message with relevant details.

Modular Function Design:

Implemented in a Python function (main(args)) that accepts arguments as a dictionary.

Easily extendable and integrable with chatbot platforms like Dialogflow, Rasa, Microsoft Bot Framework, etc.

MIME-based Email Composition:

Uses the email.mime library to build multipart email messages with headers and body text.

Clear separation of content (subject, sender, receiver, message body).

Project Flow:
User Interaction:

A user interacts with a chatbot on a website, mobile app, or messaging platform.

The chatbot collects the user's phone number, desired booking date, and time.

Data Processing:

The chatbot or backend service passes the collected data as a dictionary to the main() function.

Email Construction:

The main() function sets up the SMTP server and login credentials.

Creates an email with the booking details.

Sends the email to the designated recipient.

Confirmation:

The function returns a success message (Email Sent) after the email is delivered.

Technologies Used:
Technology	Purpose
Python 3.x	Core programming language
smtplib	Send emails using SMTP
email.mime	Format email content (MIMEText, MIMEMultipart)
Gmail SMTP (smtp.gmail.com)	Mail server for sending email securely

Security Considerations:
Do not hardcode credentials (email ID and password) in production.

Use environment variables, encrypted secrets, or secure vaults for storing sensitive data.

Gmail users must enable 2FA and use App Passwords instead of regular passwords.

Future Enhancements:
Integrate with third-party APIs (e.g., Twilio for SMS notifications).

Add logging and error-handling for failed deliveries.

Allow attachments (like booking confirmations in PDF).

Use OAuth2 for safer Gmail integration.

Create a user-friendly admin dashboard to view and track booking notifications.

Support for multilingual email content.

Use Cases:
Hotels, guest houses, or homestays receiving room booking requests through a chatbot.

Co-working spaces confirming room/slot reservations.

Healthcare clinics managing appointment bookings via chatbots.

Event venues tracking booking inquiries automatically.
