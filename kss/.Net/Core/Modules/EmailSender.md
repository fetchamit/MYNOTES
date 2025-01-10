#Sending Email using .NET Core in C#:
---------------------------------------
## step 1:
  * Genereate an app password from your gmail account.
  * Turn on the 2-step verification in your gmail and generate an app password. This app password will be used by your program to send email.
## step 2:
  * Create a seprate class/ function in your project to write email sending code.
      * Inport 2 namespaces-
      * System.Net
      * System.Net.Mail

  * We have to create object of two below classes and perform some required settings-
      * SmtpClient
      * MailMessage

  * SmtpClient class is used to perform settings related with authentication like as `sender Email`, `app password`, `protocol`,`port number `,`hostname`, etc.
  * Note: For Gmail server port number is `587 or 465`. Host name of gmail is `smtp.gmail.com`.
  * MailMessage class is used to perform settings related with mail message. Like as send to `cc,bcc,subjet of email, body of the email, sender email,attachments `,etc.
  * Note : To add any type of email we have to use `MailAddress` class.

## Step 3:Send Email
  * After doing all settings call `Send()` method of `SmtpClient` class to send email.

## Step 4: 
  * Use above code (Class/method) in anywhere of the project as per your need.
