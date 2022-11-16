# Remind-Me React application
Application allows people to create reminders, set the time/date they would like to be remined and have a notification sent to them to remind them.

#### How to send mail using JS
1) Create HTML from with id for:
- Name
- Email
- Body
2) Create Send button with { onclick=”JSfunction()" }
3) Add to HTML: {  <"\script src="https://smtpjs.com/v3/smtp.js"><\/script> }
4) Add JS:
- first get input data using getElementById()
- second send mail securely with:
Email.send({
    SecureToken : "8c2798ce-3285-4bdf-9d1a-8bbf75d90f97",
    To : email.value,
    From : "remindme.application2022@gmail.com",
    Subject : "RemindMe Application",
    Body : body.value
}).then(
    message => alert(message)
);

- What is “Secure Token”:
    1) Create SMTP token @ https://app.elasticemail.com/marketing/settings/new/create-smtp 
    2) Use this SMTP token to encrypt the credentials @ https://smtpjs.com/