# Matcha ♡

Matcha is a group project by École 42. The goal of this project is to build a dating app which consists of functionalities specified in the instruction PDF (find included).

Language: Python.
Framework: Flask.
DB: MongoDB

## General Instructions

• For this project you are free to use the language you want.
• You can use micro-frameworks, and all the libraries in the world for this project.
• We will consider that a “micro-framework” has a router, and eventually templating, but no ORM, validators or User Accounts Manager

As long as you respect these constraints you are free to use what you like.

If you require inspiration, we will suggest a few main languages:

◦ Sinatra for Ruby.
◦ Express for Node (yes, we consider this to be micro-framwork).
◦ Flask for Python.
◦ Scalatra for Scala.
◦ Slim for PHP (Silex is not authorized because of doctrine integration).
◦ Nickel for Rust.
◦ Goji for Golang.
◦ Spark for Java.
◦ Crow for C++.

• You’re free to use the web server you like most may it be Apache, Nginx or a built-in web server.
• Your whole app must be compatible at least with Firefox (>= 41) and Chrome (>= 46).
• Your website must have a decent layout: at least a header, a main section and a footer.
• Your website must be usable on a mobile phone and keep an acceptable layout on small resolutions.

All your forms must include all the correct validations, and the whole website must be secure. This part is mandatory and will be checked extensively in defense. To give you an idea, here are a few elements that are not considered secure:

◦ To have a “plain text” password stored in your database.
◦ To be able to inject HTML of “user” Javascript code in unprotected variables.
◦ To be able to upload unwanted content.
◦ To be able to alter a SQL request.

You can ask your questions on public forums, or ask your colleagues via Slack.

## Mandatory Section

You will need to create a Web App with the following features:

### Registration and Signing-in

The app must allow a user to register asking at least an email address, a username, a last name, a first name and a password that is somehow protected. After the registration, an e-mail with an unique link must be sent to the registered user to verify his account.

The user must then be able to connect with his/her username and password. He/She must be able to receive an email allowing him/her to re-initialize his/her password should the first one be forgotten and disconnect with 1 click from any pages on the site.

### User profile

Once connected, a user must fill his or her profile, adding the following information:
◦ The gender.
◦ Sexual preferences.
◦ A biography.
◦ A list of interests with tags (ex: #vegan, #geek, #piercing etc...). These tags must be reusable.
◦ Pictures, max 5, including 1 as profile picture.
◦ The user must be able to check who looked at his/her profile as well as who “liked” him/her.
◦ The user must have a public “fame rating”. It is up to you to define what “fame rating” means, as long as your criteria are consistant.
◦ The user must be located using GPS positionning, up to his/her neighborhood. If the user does not want to be positionned, you must find a way to locate him/her, even without his/her knowledge. 
◦The user must be able to modify his/her GPS position in his/her profile.

Note: At any time, the user must be able to modify the above fields of information, including the first name, last name, and email address.

### Browsing

The user must be able to easily get a list of suggestions that match his/her profile.

• You will only propose relevant profiles, for example, only men for a heterosexual female.
• You must manage bisexuality. If the orientation isn’t specified, the user will be considered bi-sexual by default.

You must cleverly match3 profiles:
◦ Same geographic area as the user.
◦ With a maximum of common tags.
◦ With a maximum “fame rating”.
◦ You must show in priority people from the same geographical area.
◦ The list must be sortable by age, localization, “fame rating” and common tags.
◦ The list must be filterable by age, localization, “fame rating” and common tags.

### Research
The user must be able to run an advanced research selecting one or a few criterias such as:
• A age gap.
• A “fame rating” gap.
• A location.
• One or multiple interests tags.

As per the suggested list, the resulting list must be sortable and filterable by age, location, “fame rating” and tags.

### Profile of other users

A user must be able to consult the profile of other users. Profiles must contain all the information available about them, except for the email address and the password. When a user consults a profile, it must appear in his/her visit history.

The user must also be able to:
◦ If he has at least one picture “like” another user. When two people “like” each other, we will say that they are “connected” and are now able to chat. 
◦ If the current user does not have a picture, he/she cannot complete this action.
◦ Check the “fame rating”.
◦ See if the user is online, and if not see the date and time of the last connection.
◦ Report the user as a “fake account”.
◦ Block the user. A blocked user won’t appear anymore in the research results and won’t generate additional notifications.
◦ A user must be able to clearly see if the consulted profile is connected or “like” his/her profile and must be able to “unlike” or be disconnected from that profile.

### Chat

When two users are connected,they must be able to “chat” in real time. How you will implement the chat is totally up to you. The user must be able to see from any page if a new message is received.

### Notifications

A user must be notified in real time of the following events:
◦ The user received a “like”.
◦ The user’s profile has been checked.
◦ The user received a message.
◦ A “liked” user “liked” back.
◦ A connected user “unliked” you.
◦ A user must be able to see, from any page that a notification hasn’t been read.
