# CH1 -- structure of a Document
## objectives
In this chapter, you will learn 

+ introduction of OOXML
+ how to look at xml content in an Office file
+ basic structure of an Office file
+ root node about Document in OOXML

## CH1.1 -- introduction of OOXML
`OOXML` (stands for `Office Open Xml`) is a zipped, XML-based file format developed by Microsoft.

The term `Office Open Xml`, is self-planatory, indicating that all Office files can be represented as Xml tag 

> [!IMPORTANT]
> You can NOT directly see the xml content of an Office file by opening it with webbrowser.
>
> If you do so, it will try to download the Office file in the webbrowser.
>
> Howerver, there are many ways to see the xml content that is covered in next section.

### reference
+ [OOXML](https://en.wikipedia.org/wiki/Office_Open_XML)

## CH1.2 -- how to look at xml content in an Office file
### Coding
#### C# with .NET Framework
You can write code snippets in C# with these assemblies to fetch xml content.

+ `System.IO.Packaging` (developed by Microsoft, but NOT built-in, you have to download it at [nuget](https://www.nuget.org/packages/System.IO.Packaging/10.0.0-preview.3.25171.5))
+ assemblies about Xceed (third-party assemblies developed by Xceed, you can visit [Xceed.com](https://xceed.com/)

> [!NOTE]
> There is a [property in Xceed.Document.Net assembly](https://doc.xceed.com/xceed-document-libraries-for-net/Xceed.Document.NET~Xceed.Document.NET.DocumentElement~Xml.html) to get xml content of an Office Word file.
>
> However, in my experience, I can NOT use the property possibly due to the license is NOT correctly configured. And we can apply that it is NOT free to look at xml content.

### rename the extension of file so that it to zip file.
You can see xml content of Office file through these steps.

Step 1:
Copy the file.

Step 2:
Rename the copied file to original file name but with file extension to `.7z`.

> [!NOTE]
> The main purpose of doing so instead of change the original file extension to `.7z` is to
>
> make a backup, avoiding that after changing the renamed file's extension from `.7z` to the file extension of Office (such as `.docx`),
>
> we can NOT open the file.
>
> Doing so is my habit.
   
## CH1.3 -- basic structure of an Office file
Since Office 2013, it supports OOXML for files with file extension that ends with `x` (such as `*.docx`, `*.pptx`,`*.xlsx`)



## CH1.4 -- root node about Document in OOXML
