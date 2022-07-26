# File Manipulation / System.IO

## File and Stream I/O
File and stream I/O (input/output) refers to the transfer of data either to or from a storage medium.

### commonly used file and directory classes:

File - provides static methods for creating, copying, deleting, moving, and opening files, and helps create a FileStream object.

FileInfo - provides instance methods for creating, copying, deleting, moving, and opening files, and helps create a FileStream object.

Directory - provides static methods for creating, moving, and enumerating through directories and subdirectories.

DirectoryInfo - provides instance methods for creating, moving, and enumerating through directories and subdirectories.

Path - provides methods and properties for processing directory strings in a cross-platform manner.

## Streams
The abstract base class Stream supports reading and writing bytes. 

Streams involve three fundamental operations:

Reading - transferring data from a stream into a data structure, such as an array of bytes.

Writing - transferring data to a stream from a data source.

Seeking - querying and modifying the current position within a stream.

###commonly used stream classes:

FileStream – for reading and writing to a file.

IsolatedStorageFileStream – for reading and writing to a file in isolated storage.

MemoryStream – for reading and writing to memory as the backing store.

BufferedStream – for improving performance of read and write operations.

NetworkStream – for reading and writing over network sockets.

PipeStream – for reading and writing over anonymous and named pipes.

CryptoStream – for linking data streams to cryptographic transformations.

For an example of working with streams asynchronously, see Asynchronous File I/O.

## Readers and writers

commonly used reader and writer classes:

BinaryReader and BinaryWriter – for reading and writing primitive data types as binary values.

StreamReader and StreamWriter – for reading and writing characters by using an encoding value to convert the characters to and from bytes.

StringReader and StringWriter – for reading and writing characters to and from strings.

TextReader and TextWriter – serve as the abstract base classes for other readers and writers that read and write characters and strings, but not binary data.

## Compression
Compression refers to the process of reducing the size of a file for storage.

classes are frequently used when compressing and decompressing files and streams:

ZipArchive – for creating and retrieving entries in the zip archive.

ZipArchiveEntry – for representing a compressed file.

ZipFile – for creating, extracting, and opening a compressed package.

ZipFileExtensions – for creating and extracting entries in a compressed package.

DeflateStream – for compressing and decompressing streams using the Deflate algorithm.

GZipStream – for compressing and decompressing streams in gzip data format.


## How to: Write text to a file

classes and methods are typically used to write text to a file:

StreamWriter contains methods to write to a file synchronously (Write and WriteLine) or asynchronously (WriteAsync and WriteLineAsync).

File provides static methods to write text to a file, such as WriteAllLines and WriteAllText, or to append text to a file, such as AppendAllLines, AppendAllText, and AppendText.

Path is for strings that have file or directory path information. It contains the Combine method and, in .NET Core 2.1 and later, the Join and TryJoin methods, which allow concatenation of strings to build a file or directory path.

## How to: Read and write to a newly created data file
The System.IO.BinaryWriter and System.IO.BinaryReader classes are used for writing and reading data other than character strings. The following example shows how to create an empty file stream, write data to it, and read data from it.

