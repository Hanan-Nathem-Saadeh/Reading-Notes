# System.I.O
## File and Stream I/O
It is transfer of data either to or from a storage medium.

### the System.IO namespaces
~~~ contain types that enable reading and writing, both synchronously and asynchronously, on data streams and files.
~~~ contain types that perform compression and decompression on files, and types that enable communication through pipes and serial ports.

## Files and directories :
you can get and set properties for files and directories, and retrieve collections of files and directories based on search criteria.

**some commonly used file and directory classes:**

* File     ~~~  provides static methods for creating, copying, deleting, moving, and opening files, and helps create a FileStream object.

* FileInfo   ~~~  provides instance methods for creating, copying, deleting, moving, and opening files, and helps create a FileStream object.

* Directory    ~~~  provides static methods for creating, moving, and enumerating through directories and subdirectories.

* DirectoryInfo   ~~~  provides instance methods for creating, moving, and enumerating through directories and subdirectories.

* Path     ~~~ provides methods and properties for processing directory strings in a cross-platform manner.

**NOTE: Visual Basic users can use the methods and properties provided by the Microsoft.VisualBasic.FileIO.FileSystem class for file I/O**

## Streams
~~~ supports reading and writing bytes..
~~~ provide a common view of data sources and repositories, and isolate the programmer from the specific details of the operating system and underlying devices.

**fundamental operations**
* Reading - transferring data from a stream into a data structure, such as an array of bytes.
* Writing - transferring data to a stream from a data source.
* Seeking - querying and modifying the current position within a stream.

***some commonly used stream classes:***
~~~ FileStream ===> for reading and writing to a file.
~~~ IsolatedStorageFileStream ===> for reading and writing to a file in isolated storage.
~~~ MemoryStream ===> for reading and writing to memory as the backing store.
~~~ BufferedStream ===> for improving performance of read and write operations.
~~~ NetworkStream ===> for reading and writing over network sockets.
~~~ PipeStream ===> for reading and writing over anonymous and named pipes.
~~~ CryptoStream ===> for linking data streams to cryptographic transformations.
---



