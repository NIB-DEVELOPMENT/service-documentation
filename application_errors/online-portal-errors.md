## Admin User Authentication and Authorization

| Service Origin    | Error                                        | Reason                                                                                  | Resolution                                                                                    |
| :----:            | :----:                                       | :----:                                                                                  | :----:                                                                                        |
| Admin Auth/Roles  | User does not have the required permissions  | User's role does not allow access.                                                      | Update user's role if permitted                                                                            |
| Admin Auth        | Invalid username or password                 | Credentials the user entered may be incorrect or an account may not exist for the user. | Determine if account exists. If yes, have user ensure correct credentials enter or reset password         |
| Admin Auth        | Username is required                         | User did not enter username in login form                                               | Have user ensure username entered in form                                                     |
| Admin Auth        | Password is required                         | User did not enter username in login form                                               | Have user ensure password entered in form                                                     |

##Demographics

| Service origin    | Error                                      | Reason                                               | Resolution                                           |
| ----------------- | ---------------------------------- | ------------------------------------------ | ---------------------------------------------------- | ---------------------------------------------------- |
| Bank branches             | No Bank Branches Found                     | No bank branches are found - internally              | None                                                 |
| Claimaint address      | Invalid address type                       | Invalid address type for a claimaint                 | Choose a valid address type (Mailing or Residential) |
| Claimaint address  Start date cannot be before current date   | The beginning date is before the current date        | Choose a later calandar date                         |
| Claimaint address | This state does not belong to this country | The chosen state is not located in the chose country | Choose a state within the selected country           |
| Claimaint address                  | No States Found                            | No states are found - internally                     | None                                                 |
| Claimaint address          | No Address Types Found                     | No address types found - internally                  | None                                                 |
| Claimaint contact                | No Countries Found                         | No countries found - internally                      | None                                                 |
| Claimaint contact                | Phone type is invalid                      | Not a valid phone type                               | Choose a valid phone type (Home, Mobile, Work)       |
| Claimaint contact             | No Phone Types Found                       | No phone types found - internally                    | None                                                 |
| Local office               | No Local Offices Found                     | No local offices found - internally                  | None                                                 |
| User                                 | User not found                             | User not found with inputted nib address             | Ensure that NIB number is correct                    |
| User Local Office                 | User is required                           | User object is required - internally                 | None                                                 |
| User Local Office        | Local Office is required                   | Local office is required - internally                | None                                                 |


##Email

<h1 style="text-align:center">Email Service Error Messages</h1>

| Service Origin         | Error                                                       | Reason                                                                                  | Resolution                                                                                    |
| :----                  | :----                                                       | :----                                                                                   | :----                                                                                        |
| Template Upload        | Only files with .html extension are allowed                 | File type upoaded is not html or htm                                                    | Ensure file has .html or .htm extension                                                                          |
| Template Upload        | Something is wrong with the uploaded template               | There is a syntax issue with uploaded html file.                                        | Check the file for errors relating to Jinja syntax (e.g. {{{data.first_name}} has an unexpected curly bracket.)        |
| Template Upload        | A template already exists with that name                    | A html file exists in the template repository with the same name.                       | Choose a different name if existing template is still in use because it then cannot be overwritten.                                               |
| Template Upload        | There are no existing templates                             | The template directory is empty                                                         | Re-upload all required templates.                                                    |
| Template Upload        | Template does not exist                                     | A specific template was not found in the template directory                             | Re-upload the template                                                                        |
| Template Upload        | Template ID is required                                     | Template ID is required when searching for specific templates                           | List all the template to get ID of the template you need       |
| Template Upload        | template_name is required                                   | Name is required for each template uploaded                                             | Enter name in form                                                   |
| Template Upload        | template is required                                        | No template uploaded                                                                    | Upload template                                               |
| Email Request        | email_from is required                                        | Sender email addresses was not sent in email request                                          | Upload template                                               |
| Email Request        | email_to is required                                          | Recipient information was not sent in email request                                          | Information such as recipient email, name, and application type required                                            |
| Email Request        | subject is required                                           | No subjet was sent in email request                                         | Subject required for email                                            |
| Email Request        | template_id is required                                       | Email template ID was not sent in email request                                          | Specify template that the email to be sent with                                             |
| Email Request        | email_address is required for email_to                        | Recipient email addresses was not sent in request                                          | Add email address for recipient                                              |
| Email Request        | data is required for email_to                                | Sender email addresses was not sent in request                                          | Add email address the email is to be sent from                                               |
| Email Request        | Maximum recipients is set to 500. Please reduce the number of recipients for this email request                                   | Too many recipienets for one email request                                         | Split requests, with each having 500 or less recipients                                            |
| Email Send           | Email template not found                                   | Template for email needs to be specified                                         | Add template for email to be sent with                                           |
| API Access     | Application already exist                                 | An attempt is made to generate an access key for an application that exists with the name entered                                        | Verify whether an attempt is being made to generate an access key for an exisiting application. No action neccesary if it is the same application. |
| API Access       | Application does not exist                                   | An attempt is made regenerate key for non-existent application                                      | None                                          |
| API Access       | Api key is not valid                                  | Wrong API access key in application header                                        | Re-check access key or generate new key                                           |
| API Access       | No App-Name found in header                                   | Application name (e.g. ONLINE_CLAIMS) must be in header                                        | Add template for email to be sent with                                           |
| API Access       | No Api-Key found in header                                  | API Access Key missing                                        | Place key in aplication header                                           |


## Cards Admin

| Service origin     | Error                                                           | Reason                                                        | Resolution                                                       |
| ------------------ | --------------------------------------------------------------- | ------------------------------------------------------------- | ---------------------------------------------------------------- |
| Online cards admin | From Inserted Date cannot be greater than To Inserted Date      | User chose a "to" date that is after the "from" date          | "From" date must be before "To" date                             |
| Online cards admin | Application Not Found                                           | Application cannot be found - internally                      | None / Submit a new application                                  |
| Online cards admin | Only pending applications can be approved                       | An application must be worked on before being approved        | Update the status of the application to pending before approving |
| Online cards admin | Reason for denial is required                                   | Reason for denial is a required field                         | Must have a reason for denying an application                    |
| Online cards admin | Reason for denial is not valid                                  | Not a valid reason to deny an application                     | Must be one of the listed reasons of denying an application      |
| Online cards admin | Only pending applications can be denied                         | Application must be worked on before being denied             | Update the status of an application to pending before denying    |
| Online cards admin | Application is already marked ready for pickup                  | Application is currently already marked for pick up           | None                                                             |
| Online cards admin | Only approved applications can be marked ready for pickup       | Application is not currently approved                         | Approve the application before marking ready for pick up         |
| Online cards admin | Application has already been routed to a user                   | Application already assigned to someone else                  | Assign another application                                       |
| Online cards admin | Only applications that have been assigned can be reassigned     | Application doesn't have an assignee currently                | Assign application to a user                                     |
| Online cards admin | Application is outside of your local office                     | Applications must be assigned to the local office of the user | Submit application to currently assigned local office            |
| Online cards admin | Application cannot be routed to the owner of the application    | A person cannot process their own application                 | Assign application to another user                               |
| Online cards admin | R4 form is not eligible for reupload                            | R4 form not allowed - already generated                       | None                                                             |
| Online cards admin | App File Upload ID required                                     | Upload id cannot be blank - internally                        | None                                                             |
| Online cards admin | No NIB user Provided                                            | User ID cannot be blank - Internally                          | None                                                             |
| Online cards admin | Please provide a reason for why a reupload has been requested   | Reason is required                                            | Provide a reason for reupload                                    |
| Online cards admin | A request to have the document reuploaded has already been sent | An existing request has already been made                     | None / Resolve previous request                                  |
| Online cards admin | Invalid reason for reupload reques                              | Upload reason is not a valid reason                           | Choose another reupload reason                                   |
| Online cards admin | This application has already been routed to this user           | Application is already assigned to this user                  | None                                                             |

## User service


| Service Origin           | Error                                                                            | Reason                                                                                  | Resolution                                                          |
| :----                    | :----                                                                            | :----                                                                                   | :----                                                               |
| User Service (Sign Up and Account Update)   | NIB# is already tied to a user account                                           | Account exists already for user with that NIB# registered                               | Sign into existing account. Reset password if necessary             |
| User Service (Sign Up and Account Update)   | Email Address is already tied to a user account                                  | Account exists already for user with that email registered                              | Sign into existing account. Reset password if necessary                                 |
| User Service (Account Update)   | This email address is already tied to your account                                  | Email addressing being added is already in your records                              | No action to take                                 |
| User Service (Sign In)   | NIB# not found Click the register link if you have not yet created an account    | User is not yet registered on the online portal                                         | Create account             |
| User Service (Sign In and Password Reset)            | User Account has not been activated                                              | User account needs to be confirmed                                                      | Check email for activation link to confirm user and account will be activated.            |
| User Service (Sign In)            | Password is Incorrect                                             | Wrong password entered                                                      | Have user ensure correct password entered, reset password if necessary           |
| User Service (Password Reset)            | NIB# not found                                            | NIB# is not registered to any account                                                      | Create user account           |
| User Service (Password Reset)            | User Account has not been activated                                             | Wrong password entered                                                      | Have user ensure correct password entered, reset password if necessary           |
