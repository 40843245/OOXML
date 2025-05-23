# CH1 -- structure of a Workbook
## objectives
In this chapter, you will learn 

+ introduction of OOXML
+ how to look at xml content in an Office file
+ basic structure of an Office file
+ typical structure of a Workbook

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

Step 3:

Under the `.7z`, file, you can found lots of `.xml` file.

> [!NOTE]
> About zip file knowledgement.
>
> For a zip file, you can directly see the children and open it.
>
> But you can NOT move, rename, or delete the children or edit its content without unzipping.
>
> Before doing that, you have to unzip the file.

## CH1.3 -- basic structure of an Office file
Since Office 2013, it supports OOXML for files with file extension that ends with `x` (such as `*.docx`, `*.pptx`,`*.xlsx`)

Here, `x` stands for `xml`.

### Excel file (`*.xlsx`)
Let's look at the basic structure of an Office Excel file

A newly created `*.xlsx` file that contains only one worksheet with no data in the workbook must contain these directories and files. Shown as following hierarchy tree.

![Structure of Excel (1)](https://github.com/user-attachments/assets/6e932070-6866-44c6-91a4-2364b4539314)

> [P.S.]
> 
> About background of node, it indicates the type of file, as follows:
> 
> a node with dark green background: the Office Word file (`*.xlsx`)
> 
> a node with light yellow background: the directory
>
> a node with light blue background: the xml file (`*.xml`)
> 
> a node with light gray background: the relationship file (`*.rels`)
>
> a node with white background: the relationship file (`*.dat`)

> [!IMPORTANT]
> All Office Excel files must contain at least directories and files, shown as above hierarchy tree.
>
> However, some Office Excel files may contain
>
> + `sheet2.xml` , and more (for worksheets) 
>
> under the directory `~/xl/worksheets` when there are worksheets in the workbook. How many worksheets in the workbook are there, how many files are there under the directory `~/xl/worksheets`. 
>
>
> Similarly, some Office Excel files may contain
>
> + `image1.png`, and more (for image) 
>   
> under the directory `~/xl/media` when there are images in the workbook. How many images in the workbook are there, how many files are there under the directory `~/xl/media`. 
>
> And more.
>
> I will NOT discuss it here.
>
> I will discuss it in

### reference
+ [Office File Formats (MSDS)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-offfflp/8aea05e3-8c1e-4a9a-9614-31f71e679456)

### CH1.4 -- typical structure of a Document
![image](https://github.com/user-attachments/assets/08332380-e0b7-4a88-8d11-0abcce1a44b2)

refered to last section [Typical Document Scenario](https://learn.microsoft.com/en-us/office/open-xml/word/structure-of-a-wordprocessingml-document?tabs=cs#typical-document-scenario)

which provided by MSDS.

### reference
[Structure of a WordprocessingML document (MSDS)](https://learn.microsoft.com/en-us/office/open-xml/word/structure-of-a-wordprocessingml-document?tabs=cs)
