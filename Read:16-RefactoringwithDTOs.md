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
