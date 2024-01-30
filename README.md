# ProtonMail API

This is a basic implementation of a ProtonMail-like API using Flask and Flask-RESTful.

## Installation

1. Clone the repository.
2. Install the required dependencies using `pip install -r requirements.txt`.
3. Run the application with `python app.py`.

## Endpoints

### Send Mail
- **Endpoint:** `/send_mail`
- **Method:** `POST`
- **Request Payload:**
  ```json
  {
    "email_to": "recipient@example.com",
    "email_subject": "Your Subject",
    "email_message": "Your message content"
  }
Response:
Successful: {"status": "success", "message": "Email sent successfully"}
Error: {"status": "error", "message": "Error details"}
List Mails
Endpoint: /list_mails
Method: GET
Response:
json
Copy code
{"emails": ["email1", "email2", "email3"]}
Get Mail
Endpoint: /get_mail/<mail_id>
Method: GET
Response:
json
Copy code
{"content": "Email content for mail_id: <mail_id>"}
Read Mail
Endpoint: /read_mail/<mail_id>
Method: POST
Response:
json
Copy code
{"status": "success", "message": "Email <mail_id> marked as read"}
Mark as Read
Endpoint: /mark_as_read/<mail_id>
Method: POST
Response:
json
Copy code
{"status": "success", "message": "Email <mail_id> marked as read"}
Mark as Unread
Endpoint: /mark_as_unread/<mail_id>
Method: POST
Response:
json
Copy code
{"status": "success", "message": "Email <mail_id> marked as unread"}
Feel free to extend and modify the API according to your requirements.
This README provides a brief overview of the API's endpoints and how to set up and run the application. You can customize it based on additional features or details specific to your implementation.
