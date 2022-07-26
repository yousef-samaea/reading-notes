# Roles, Claims and JWT Tokens

Authorization is a process of determining whether the user is able to access the system resource.
The identity membership system allows us to map one or more roles with the user;  based on the role, we can do authorization. In 
this article.

### Claim-based authorization
 
Claims are the user data and they are issued by a trusted source. If we are working with token-based authentication, a claim may 
be added within a token by the server that generates the token. A claim can have any kind of data such as "DateOfJoining", 
"DateOfBirth", "email", etc. Based on a claim that a user has, a system provides the access to the page, which is called Claim 
based authorization.


Claim-based authorization can be done by creating policy; i.e., create and register policy stating the claims requirement. The 
simple type of claim policy checks only for the existence of the claim but with advanced level, we can check the user claim with 
its value. We can also assign more than one value for a claim check.


### Policy-based authorization
 
The .NET Core Framework allows us to create policies to authorization. We can either use pre-configured policies or can create a 
custom policy based on our requirement.

### Authorization Requirements
 
The requirement is the collection of data which can be used to evaluate the user principal. To create the requirement, the class 
must implement interface IAuthorizationRequirement that is an empty interface. The requirement does not contain any data and
evaluation mechanism.

### Authorization handlers
 
The authorization handler contains the evaluation mechanism for properties of requirement. The handler must evaluate the 
requirement properties against the AuthorizationContext and decide if the user is allowed to access the system resources or not. 
One requirement may have multiple handlers. The authorization handler must inherit from AuthorizationHandler<T> class; here T is 
a type of requirement class.


### Handler registration
 
The handle that is using authorization must register in service collection. We can add the service collection by using "services.
AddSingleton<IAuthorizationHandler, ourHandlerClass>()" method where we need to pass handler class.

### Add a generic claim check
If the claim value isn't a single value or a transformation is required, use RequireAssertion.
 
### Multiple Policy Evaluation
If you apply multiple policies to a controller or action, then all policies must pass before access is granted.

### Multiple Identities
Hopefully at this point you have a conceptual handle on claims and how they relate to an Identity. I said at the beginning of 
this section that the User property on HttpContext is a ClaimsPrincipal, not a ClaimsIdentity.

### JWT in ASP.NET Core
 
JWT (JSON web token) has become more and more popular in web development. It is an open standard which allows transmitting data between parties as a JSON object in a secure and compact way. The data transmitting using JWT between parties are digitally signed so that it can be easily verified and trusted.

### HEADER :

We have two main algorithms(HS256/RS256) to sign our JWT,which we mention in the headers so that the producer and consumer,both should use the same algorithm to verify the token on each end. 

### PAYLOAD :
It mostly contains the claims (custom data) and some standard claims as well.

### SIGNATURE :
It is calculated by base64url encoding of header and payload and concatenating them with a period as a separator.

### How to Producer and Consumer concept of API’s :

1. Share the SECRET
2. Prepare the PAYLOAD
3. GET the TOKEN
4. Idenitify the CONSUMER





