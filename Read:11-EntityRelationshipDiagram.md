# ERD (Entity Relationship Diagram)
### Customize the Data model
### The DataType attribute**
- The DataType attribute is used to specify a data type that's more specific than the database intrinsic type.
- The DataType Enumeration provides for many data types, such as Date, Time, PhoneNumber, Currency, EmailAddress, and more.
- The DataType attribute can also enable the application to automatically provide type-specific features.
- DataType.Date doesn't specify the format of the date that's displayed. By default, the data field is displayed according to the default formats based on the server's CultureInfo.

```
[DisplayFormat(DataFormatString = "{0:yyyy-MM-dd}", ApplyFormatInEditMode = true)]
```
- The ApplyFormatInEditMode setting specifies that the formatting should also be applied when the value is displayed in a text box for editing. (You might not want that for some fields).

### The StringLength attribute
- The StringLength attribute sets the maximum length in the database and provides client side and server side validation for ASP.NET Core MVC. 
- You can also specify the minimum string length in this attribute, but the minimum value has no impact on the database schema.
- The StringLength attribute won't prevent a user from entering white space for a name. You can use the RegularExpression attribute to apply restrictions to the input.

### The Column attribute
- The Column attribute specifies that when the database is created, the column of the Student table that maps to the FirstMidName property will be named FirstName.
### The Required attribute
- The Required attribute makes the name properties required fields.
- The Required attribute isn't needed for non-nullable types such as value types (DateTime, int, double, float, etc.). Types that can't be null are automatically treated as required fields.

### The Display attribute
- The Display attribute specifies that the caption for the text boxes should be "First Name", "Last Name", "Full Name", and "Enrollment Date" instead of the property name in each instance (which has no space dividing the words).

### The Key attribute
-  the Key attribute is used to identify it as the key.
-  You can also use the Key attribute if the entity does have its own primary key but you want to name the property something other than classnameID or ID.
-  
