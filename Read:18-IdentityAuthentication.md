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

ApiAuthorization.IdentityServer =>  Contains IdentityServer based support for API Authorization.
Core => Contains the main abstractions and types for providing support for Identity in ASP.NET Core applications.
EntityFrameworkCore => Contains implementations for Identity stores based on EntityFrameworkCore.
Extensions.Core => Contains the abstractions and types for general Identity concerns.
Extensions.Stores => Contains abstractions and types for Identity storage providers.
samples => Contains a collection of sample apps.
Specification.Tests => Contains a test suite for ASP.NET Core Identity store implementations.
test => Contains the unit and functional tests for Microsoft.Extensions.Identity and Microsoft.AspNetCore.Identity components.
testassets => Contains a webapp used for functional testing.
UI => Contains compiled Razor UI components for use in ASP.NET Core Identity.

