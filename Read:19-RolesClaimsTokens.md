# Read: 19 - Roles, Claims, Tokens
# Claims-based authorization

- A claim is a name value pair that represents what the subject is, not what the subject can do
- Claims based authorization, at its simplest, checks the value of a claim and allows access to a resource based upon that value
- An identity can contain multiple claims with multiple values and can contain multiple claims of the same type
- Claim based authorization checks:
     - Are declarative.
     - Are applied to Razor Pages, controllers, or actions within a controller.
     - Can not be applied at the Razor Page handler level, they must be applied to the Page.

- The simplest type of claim policy looks for the presence of a claim and doesn't check the value.

```
builder.Services.AddAuthorization(options =>
{
   options.AddPolicy("EmployeeOnly", policy => policy.RequireClaim("EmployeeNumber"));
});
```

# Introduction to Authentication with ASP.NET Core

- Authentication is the process of determining who you are, 
- Authorisation revolves around what you are allowed to do, i.e. permissions. 

* Authentication

  * The process of determining WHO you are

* Authorisation

  * What you are ALLOWED to do

* Claims Based Authentication

  * A statement about, or a property of, a particular identity which contains a name and a value

    * E.G. Name, Date of birth, Email, etc

  * The identity itself represents a single declaration that may have many claims associated with it

* Multiple Identities

  * It is possible to have multiple forms of identification. Think a passport and an ID, or a piece of mail specific to your household, or a specific email and password

  * The key points here are that a principal can have multiple identities, these identities can have multiple claims, and the ClaimsPrincipal inherits all the claims of its Identities

## [JWT Authentication](https://codeburst.io/jwt-to-authenticate-servers-apis-c6e179aa8c4e)

* JSON Web Token

  * In simple terms, it is just another way of encoding JSON object and use that encoded object as access tokens for authentication from the server

  * There are 3 parts to the JWT

    * Header

    * Payload

    * Signature

* Two parties involved

  * Producer

    * The one who gives a service. It will be the provider(Server) of the API(s) which are JWT protected

  * Consumer

    * The one who uses it. It will be the customer(Server/Mobile App/ Web App/ Client) who will be providing the valid JWT token to consume the API(s) being provided by the Producer

### Additional Resources

* Some information taken from the links provided above

