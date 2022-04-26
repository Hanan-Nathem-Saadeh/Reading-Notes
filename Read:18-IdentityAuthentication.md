# Read: 18 - Identity / Authentication
# ASP.NET Core Identity:
- Is an API that supports user interface (UI) login functionality.
- Manages users, passwords, profile data, roles, claims, tokens, email confirmation, and more.
- Identity can be configured using a SQL server and store a username, passwords, and profile data.
- ASP.NET Core Identity is a system that allows user login / accounts in an ASP.NET Core web application.

## Microsoft identity platform is:
- An evolution of the Azure Active Directory (Azure AD) developer platform.
- Unrelated to ASP.NET Core Identity.

## The following contains a description of each sub-directory in the Identity directory: 

- ApiAuthorization.IdentityServer =>  Contains IdentityServer based support for API Authorization.

- Core => Contains the main abstractions and types for providing support for Identity in ASP.NET Core applications.

- EntityFrameworkCore => Contains implementations for Identity stores based on EntityFrameworkCore.

- Extensions.Core => Contains the abstractions and types for general Identity concerns.

- Extensions.Stores => Contains abstractions and types for Identity storage providers.

- samples => Contains a collection of sample apps.

- Specification.Tests => Contains a test suite for ASP.NET Core Identity store implementations.

- test => Contains the unit and functional tests for Microsoft.Extensions.Identity and Microsoft.AspNetCore.Identity components.

- testassets => Contains a webapp used for functional testing.

- UI => Contains compiled Razor UI components for use in ASP.NET Core Identity.

## Installing and Configuring "Identity"
- Add Dependency: Microsoft.AspNetCore.Identity.EntityFrameWorkCore

- Installs libraries as well as models for identities

# ASP.NET Core 2.0 Authentication and Authorization System Demystified

- Identity
Key to understanding how authentication works is to first understand what an identity is in ASP.NET Core 2.0. 

- Claims
A Claim represents a single fact about the user. It could be the user's first name, last name, age, employer, birth date, or anything else that is true about the user.

- ClaimsIdentity
An Identity represents a form of identification or, in other words, a single way of proving who you are. 

- ClaimsPrincipal
A Principal represents the actual user. It can contain one or more instances of ClaimsIdentity.

## Verbs
There are 5 verbs (these can also be thought of as commands or behaviors) that are invoked by the auth system, and are not necessarily called in order. These are all independent actions that do not communicate among themselves:

- Authenticate
Gets the user’s information if any exists (e.g. decoding the user’s cookie, if one exists)
- Challenge
Requests authentication by the user (e.g. showing a login page)
- SignIn
Persists the user’s information somewhere (e.g. writes a cookies)
- SignOut
Removes the user’s persisted information (e.g. deletes the cookies)
- Forbid
Denies access to a resource for unauthenticated users or authenticated but unauthorized users (e.g. displaying a “not authorized” page)



