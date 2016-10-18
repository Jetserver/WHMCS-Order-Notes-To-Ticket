# WHMCS-Order-Notes-To-Ticket

This WHMCS hook will open a support ticket whenever a note is added to the order.

With this hook you can forget about accepting an order without reading the client’s notes !

Once an order is placed, the hook will retrieve the order notes content, open a ticket to your staff so they will be able to take action. Ticket is automatically assigned to the user’s account for future reference.

✔ You can set any ticket subject.

✔ You can set a pre-message prior to the note for your staff.

✔ You can set the ticket priority.

✔ You can set the ticket department.

✔ You can choose if you want to send email to the client for the ticket.

# Installation

Edit the hook file with a simple code editor (notepad++ is recommended). Set your desired ticket department, admin user and more. (example below) Upload it to your WHMCS hooks folder (“includes/hooks“).

Code examples –

In the given example, a ticket will be opened for deparment id “2”, under a user name “apiuser” with a “Low” priority. The ticket subject & pre-message are set to default.

```
$output['apiuser'] = 'apiuser';
$output['ticket_subject'] = $_LANG['ordernotessubject'];
$output['ticket_pre_message'] = $_LANG['ordernotespretext'];
$output['ticket_priority'] = 'Low';
$output['ticket_department'] = '2';
$output['stop_email_to_client'] = false;
```

Same code with changed subject & pre-message will be as follows –
```
$output['apiuser'] = 'apiuser';
$output['ticket_subject'] = 'This is a new subject';
$output['ticket_pre_message'] = 'This is a new pre-message';
$output['ticket_priority'] = 'Low';
$output['ticket_department'] = '2';
$output['stop_email_to_client'] = false;
```

# More Information

https://docs.jetapps.com/category/whmcs-addons/whmcs-order-notes-to-ticket
