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

