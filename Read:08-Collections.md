# Read 08 - Collections

## Collections

- Collections are similar to *arrays* in that they store groups of data.  
- Unlike arrays Collections do not have to be a fixed size.  They can grow and shrink as needed.

**There are several different types of collections**

+ Dictionaries - Can place objects in a key/value pair
+ Lists - Can search using *index* numbers
+ Queue - FIFO (First In Last Out)
+ Stack - LIFO (Last In First Out)

```
List<Starship> federationShips = List<Starship>();
```

```
Dictionary<Cruisers> imperialClass = new Dictionary <string, Cruisers>();
```

You can use *LINQ* (Language Integrated Query) to set filters on searching through *Collections*

## Enumerations
[Microsoft Docs - Enumeration Types](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/enum)

Is a value type that is set by a series of constants.  
```
enum SuperMarioTwoChar
{
    Mario,
    Luigi,
    Toad,
    Princess Peach
}
```
Can add more functionality by an *extension* method

You can get the number of the values.
```
(int)Luigi //will equal 2
```

## C# In a Nutshell 7.0 pg 118-124

### enums

Additional *enum* properties

Use enums as differeny ata types such as bytes

```
public enum borderSide : byte
```
Use *horizontal alignment* to cast from one type to another

?? Bitwise operators?

Combine enums with flags

### Generics

These allow methods to be written that can process any data type.

```
public void Things<T>(ref T param1, ref T param2)
{

}
```
Prevent duplicate methods to same work.


## C# In a Nutshell 7.0 pgs 301-313, 324-327 
### (Scanning for Notes)

IEnumerator advances through a collection in a forward manner only

ICollection and IList interfaces allows for counting of item is the collection

IDictionary uses random access via KVP

### Array Class

If two distinct arrays are directly compared they will be false.

Can search Arrays with .Find
Can also sort Arrays with .Sort
Can use the Array class to utilize Stacks, Queues, and Set Data Structures.

