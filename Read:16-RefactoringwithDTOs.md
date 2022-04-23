# Read: 16 - Refactoring with DTOs (Data Transfer Objects)
 Sometimes you want to change the shape of the data that you send to client. For example, you might want to:

- Remove circular references.
- Hide particular properties that clients are not supposed to view.
- Omit some properties in order to reduce payload size.
- Flatten object graphs that contain nested objects, to make them more convenient for clients.
- Avoid "over-posting" vulnerabilities. 
- Decouple your service layer from your database layer.

**A DTO is an object that defines how the data will be sent over the network.**
**EXAMPLE**

```
namespace BookService.Models
{
    public class BookDto
    {
        public int Id { get; set; }
        public string Title { get; set; }
        public string AuthorName { get; set; }
    }
}

namespace BookService.Models
{
    public class BookDetailDto
    {
        public int Id { get; set; }
        public string Title { get; set; }
        public int Year { get; set; }
        public decimal Price { get; set; }
        public string AuthorName { get; set; }
        public string Genre { get; set; }
    }
}
```

## Use DTOs for abstraction
- You can take advantage of DTOs to abstract the domain objects of your application from the user interface or the presentation layer.
- In doing so, the presentation layer of your application is decoupled from the service layer.
- So if you would like to change the presentation layer, you can do that easily while the application will continue to work with the existing domain layer.
- Similarly, you can change the domain layer of your application without having to change the presentation layer of the application.

## Immutability of DTOs

- A DTO is often serialized so that it can be independent of the technology used in the receiver. In most cases, the receiver of the data does not need to modify that data after receipt — ideally it shouldn’t!

- You could use a ReadOnlyCollection or the thread-safe immutable collection types present in the System.Collections.Immutable namespace. You can take advantage of record types in C# 9 to implement immutable DTOs as well.


