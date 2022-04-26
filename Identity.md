# Identity

ASP.NET Identity is the membership system for authentication and authorization of the users by building an ASP.NET application. The ASP.NET Identity is a fresh look at what the membership system should be when you are building modern applications for the web, phone or tablet.

The Identity source code is available on GitHub. Scaffold Identity and view the generated files to review the template interaction with Identity.

**Authentication:**
is used by the server to determine who is accessing their information or website. In authentication, the user or customer must prove their identity on a web server by log-in using email and word or using various social providers.

**Authorization:**
is a process by which a server determines if the client has permission to use a resource or access a file after the successful authentication.

## Features of ASP.NET Identity:

1.Two-Factor Authentication: The Two-Factor Authentication adds one more level of security to your web application.

2.Account Lockout: If the user enters the word and two factor codes incorrectly after the specific number of invalid attempts that can be configured by the developer his or her account will be locked for a specific period of time.

3.Account Confirmation: ASP.NET Identity allows us to confirm the account by confirming the email of the user.

4.word Reset: This feature enables users to reset their word if they have forgotten their word.

5.Support IQueryable on Users and Roles: IQueryable on UsersStore and RolesStore helps to easily get the list of Users and Roles.

6.Delete User account: we can easily delete the user using UserManager.

7.Enhanced word Validator: the word validator gives you more control over the complexity of the word.

### terms :

1.*No Authentication:*-*This authentication mode doesn't require any user authentication for applications.

2.*Organizational Accounts:* This type of authentication mode will be configured to use Windows Identity Foundation (WIF) based on user accounts in Active Directory

3.*Windows Authentication:* This mode of authentication will support Windows Identity IIS module for authentication.

### important parts of the ASP.NET Identity system:

1.User
2.Role
3.User Manager
4.Role Manager
5.Authentication Manager
6.Entity Framework DBContext

### Log in

The Login form is displayed when:
The Log in link is selected.
A user attempts to access a restricted page that they aren't authorized to access or when they haven't been authenticated by the system.

### Claims:
A Claim represents a single fact about the user. and it code be any data related to the user.

### ClaimsIdentity:
An Identity represents a form of identification or, in other words, a single way of proving who you are.

**ClaimsPrincipal§**
A Principal represents the actual user.

### Verbs :
There are 5 verbs that are invoked by the auth system, and are not necessarily called in order.

1.Authenticate
Gets the user’s information if any exists

2.Challenge

Requests authentication by the user

3.SignIn
Persists the user’s information somewhere

4.SignOut
Removes the user’s persisted information

5.Forbid
Denies access to a resource for unauthenticated users or authenticated but unauthorized users

*class Startup*
When the app first starts it triggers the ConfigureServices() and Configure() methods in the Startup class.

*class ApplicationUser*
The app needs a representation of a user.

*class AccountController*
In order to do anything meaningful with the authentication middleware and handler, some actions are needed.

*Login.cshtml*
The AccountController exists, but the users need a way to see the login form and send their credentials to the Login action of the controller.

*class HomeController*
Now that there is an AccountController to log users in and out, there must be something that uses it

