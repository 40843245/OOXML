# Appendix 1.1 -- xml tag in Document
## Prequisite
See [`Prequisite.md`](https://github.com/40843245/OOXML/blob/main/Prequisite/Prequisite.md)

## Suggestion
See [`Suggestion.md`](https://github.com/40843245/OOXML/blob/main/Suggestion/Suggestion.md)

## NOTICE
> [!WARNING]
> Most content of these table are refered from Google Gemini's answer or from non-official website, which BOTH may be incorrect.
>
> Read with caution.

## Important concept
> [!IMPORTANT]
> In OOXML,
>
> For those value of attribute that needs to be specified with a string containing a boolean value (i.e. `"true"` or `"false"`),
>
> + `"0"` is equivalent to `"false"`
> 
> + `"1"` is equivalent to `"true"`

## processing instruction
See `Appendix 1 -- tags in xml`[^3]

But in OOXML, there are many ways added to process a file that will be parse with OOXML preprocessor.

I just list some of them that commonly seen in Word file.

| target of the processing instruction | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `mso-application` | | targets Microsoft Office applications. | | |

#### children in `mso-application`
none

#### attributes in `mso-application`
| attributes name | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `progid` | *Pr*ogrammatic *Id*entifier | It's a string that uniquely identifies a COM (Component Object Model) component or application. | | |

#### examples and explanation
##### example 1.1 -- processing instruction
`Docx1.docx` file

```
<?mso-application progid="Word.Document"?>
```

In above example, we can know that

+ `Docx1.docx` file targets to Microsoft Office.
+ it is a Document.
+ Thus, it targets to Microsoft Office Word and you can open it with Microsoft Office Word.

### namespace under `xmlns` namespace
| namespace under `xmlns` namespace | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `aml` | *A*nnotation *M*arkup *L*anguage | used for comments and revisions. | | |
| `a` | *A*nnotation | specifies which core DrawingML elements will be used for graphical objects. | | |
| `w` | *W*ordProcessingML | assign a value to it determine which WordprocessingML elements is used. | | |
| `w14` | *W*ordProcessingML | assign a value to it determine which WordprocessingML (with version id 14) elements is used. | | |
| `w15` | *W*ordProcessingML | assign a value to it determine which WordprocessingML (with version id 15) elements is used. | | |
| `w16cid` | *W*ordProcessingML *C*ontent *Id*entifiers | assign a value to it determine which Content Identifiers of WordprocessingML (with version id 16) elements is used. | | |
| `w16se` | *W*ordProcessingML *S*ymbol *E*xtensibility | assign a value to it determine which Symbol Extensibility of WordprocessingML (with version id 16) elements is used. | | |
| `wpg` | *W*ordProcessingML *G*rouping  | assign a value to it determine which Symbol Extensibility of WordprocessingML Grouping is used. | | |
| `wpi` | *W*ordProcessingML *I*nk  | assign a value to it determine which Symbol Extensibility of WordprocessingML Ink is used. | At intial release of WordprocessingML Ink (in Microsoft Office 2010), its namespace is named as `wpi` but it is named as `aink` at later release. | |
| `wps` | *W*ord*P*rocessing *S*hapes | assign a value to it determine which Wordprocessing Shapes is used. | | |
| `wp` | *W*ord*P*rocessing | assign a value to it determine which WordProcessing is used. | | |
| `wp14` | *W*ord*P*rocessing version id 14 | assign a value to it determine which WordProcessing with version id 14 is used. | | |
| `wpc` | *W*ord*P*rocessing *C*anvas | assign a value to it determine which WordProcessing Canvas is used, WordProcessing Canvas is for drawing and layout within the Word document (particularly newer drawing features). | | |
| `c` | *C*harts | specific which `DrawingML Charting Schema` is used. It is used for defining properties for charts. | | |
| `cx` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (main extension) is used. | | |
| `cx1` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (sub extension 1) is used. | | |
| `cx2` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (sub extension 2) is used. | | |
| `cx3` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (sub extension 3) is used. | | |
| `cx4` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (sub extension 4) is used. | | |
| `cx5` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (sub extension 5) is used. | | |
| `cx6` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (sub extension 6) is used. | | |
| `cx7` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (sub extension 7) is used. | | |
| `cx8` | *C*harts E*x*tension | specific which extension of `DrawingML Charting Schema` (sub extension 8) is used. | | |
| `aink` | Ink | specific which `DrawingML Ink Schema` is used. It is used for defining properties for inks, provide Digital Ink Support, and provide DrawingML Integration  | | |
| `am3d` | *M*odel *3D* | specific which `DrawingML 3D Model Schema` is used. It is used for defining properties for 3D model, embed 3D models, and provide DrawingML Integration  | | |
| `dt` | *D*ata *T*ypes | often used for properties or values within the document. | | |
| `mc` | *Markup* *C*ompatibility | determine which version of documents are allowed to be able to be compatible with different versions of Office Open XML. | | |
| `ve` | *Markup* *C*ompatibility | Same as above | a convention of `mc` in `~/word/document.xml` file under a Office Word file | |
| `o` | *O*ffice | it is for Office-specific elements, often related to general Office document properties. | | | 
| `v` | *V*ector Markup Language | it is for Vector Markup Language, which is a legacy format for vector graphics in Office documents. | | |
| `w10` | *W*ord *10*-specific elements | it is for Word 10-specific elements, indicating features or settings from that version. | | |
| `w` | *W*ord 2003 elements | it is the primary namespace for Word 2003 XML. | reason about why it is for Word 203 XML see following history. | |
| `wx` | *W*ord 2003 Au*x*iliary Hints | it is for Word 2003 Auxiliary Hints, which might contain additional information for specific Word features. | The word `Auxiliary` has a meaning of the word `Extension`, but its usage of the word `Auxiliary` is narrower and more concise than that of the word `Extension`, and we usually abbreviates the word `Extension` to `X`. And I guess this is the reason why the namespace is declared as `wx`. | |
| `wne`| WNE | it points to elements from which version (according to the value of `xmlns:wne`). Its presence suggests potential compatibility features or elements used across versions. | See `WNE class`[^5] for more details. | | 
| `wsp` | *W*ord *S*ervice *P*ack | This namespace might relate to Word xxx (version according to value of `xmlns:wsp` ) Service Pack 2 specific elements or extensions. | | | 
| `sl` | *S*chema *L*ibrary | This namespace could be for a Schema Library, possibly related to document templates or components. | | | 
| `r` | *R*elationship | it specifies which relationship will be used. | | | 
| `m` | *M*ath | it specifies which tools about math (its functionalities contain `Equation`) will be used. | | | 
| `ignorable` | ignorable | it specifies which namespace declaration in this tag will be ignored. | it must be string, seperated by exactly one space. (To represent that many of them will be ignored.) | | 

> [!NOTE]
> History of Office and OOXML.
>
> + In year 2000, Microsoft released Microsoft Office 2000 which is the intial release that uses XML tag.
>
> + In year 2003, Microsoft released Microsoft Office 2003 which is the intial release that uses XML tag cooperate with OOXML,
> 
> making the Office file in cross-platform (before that, to view the Office file or access it, you must use Office products which is developed by Microsoft)
>
> and more sharable.

#### examples and explanation
##### example 1.1 -- wordDocument tag as root node in `~/word/document.xml`
root node of `~/word/document.xml` file under `Docx1.docx` file.

```
<w:wordDocument
xmlns:aml="http://schemas.microsoft.com/aml/2001/core"
xmlns:wpc="http://schemas.microsoft.com/office/word/2010/wordprocessingCanvas"
xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"
xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
xmlns:o="urn:schemas-microsoft-com:office:office"
xmlns:v="urn:schemas-microsoft-com:vml"
xmlns:w10="urn:schemas-microsoft-com:office:word"
xmlns:w="http://schemas.microsoft.com/office/word/2003/wordml"
xmlns:wx="http://schemas.microsoft.com/office/word/2003/auxHint"
xmlns:wne="http://schemas.microsoft.com/office/word/2006/wordml"
xmlns:wsp="http://schemas.microsoft.com/office/word/2003/wordml/sp2"
xmlns:sl="http://schemas.microsoft.com/schemaLibrary/2003/core"
w:macrosPresent="no"
w:embeddedObjPresent="no"
w:ocxPresent="no"
xml:space="preserve">
```

In above example, we can know that

+ The tag is a root node in an Office Word file.
+ In `xmlns:aml="http://schemas.microsoft.com/aml/2001/core"`, its *A*nnotation *M*arkup *L*anguage refers the url `http://schemas.microsoft.com/aml/2001/core`.
+ In `xmlns:wpc="http://schemas.microsoft.com/office/word/2010/wordprocessingCanvas"`, it uses the url `http://schemas.microsoft.com/office/word/2010/wordprocessingCanvas` as WordProcessing Canvas.
+ In `xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"`, its data type is UUID where its UUID is `C2F41010-65B3-11d1-A29F-00AA00C14882`.
+ In `xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006`, for markup language, it is compatible with version 2006 or above.
+ In `xmlns:o="urn:schemas-microsoft-com:office:office"`, it declares a namespace named `o` and alias the namespace `urn:schemas-microsoft-com:office:office` as `o`.
+ In `xmlns:v="urn:schemas-microsoft-com:vml"`, its Vector Markup Language uses `urn:schemas-microsoft-com:vml`
+ In `xmlns:w10="urn:schemas-microsoft-com:office:word`, its Word 10-specific elements targets to the namespace `urn:schemas-microsoft-com:office:word`.
+ In `xmlns:w="http://schemas.microsoft.com/office/word/2003/wordml"`, its Word 2003 elements targets to the url `http://schemas.microsoft.com/office/word/2003/wordml`.
+ In `xmlns:wx="http://schemas.microsoft.com/office/word/2003/auxHint"`, its Word 2003 Auxiliary Hints targets to the url `http://schemas.microsoft.com/office/word/2003/auxHint`, simply said, it uses `http://schemas.microsoft.com/office/word/2003/auxHint` as an extension for Word 2003 elements.
+ In `xmlns:wne="http://schemas.microsoft.com/office/word/2006/wordml"`, its wne targets to the url `http://schemas.microsoft.com/office/word/2006/wordml`.
+ In `xmlns:wsp="http://schemas.microsoft.com/office/word/2003/wordml/sp2"`, its Word Service Pack targets to the url `http://schemas.microsoft.com/office/word/2003/wordml/sp2`, and its Word Service Pack uses version 2003.
+ In `xmlns:sl="http://schemas.microsoft.com/schemaLibrary/2003/core"`, its Schema Library targets to the url `http://schemas.microsoft.com/schemaLibrary/2003/core` and the Word file uses Schema Library in version 2003.
+ In `w:macrosPresent="no"`, the Word file does NOT execute the macros (written in VBA or VB)
+ In `w:embeddedObjPresent="no"`, the Word file does NOT embed object.
+ In `w:ocxPresent="no"`, the Word file does NOT use Active Control.
+ In `xml:space="preserve"`, the Word file does fully preserve the space.

##### example 1.2 -- document tag as root node in `~/word/document.xml`
root node of `~/word/document.xml` file under `Docx1.docx` file.

```
<w:document
    xmlns:ve="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:o="urn:schemas-microsoft-com:office:office"
    xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships"
    xmlns:m="http://schemas.openxmlformats.org/officeDocument/2006/math"
    xmlns:v="urn:schemas-microsoft-com:vml"
    xmlns:wp="http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing"
    xmlns:w10="urn:schemas-microsoft-com:office:word"
    xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main"
    xmlns:wne="http://schemas.microsoft.com/office/word/2006/wordml"
    xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main"
    xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart"
    xmlns:wpc="http://schemas.microsoft.com/office/word/2010/wordprocessingCanvas"
    xmlns:cx="http://schemas.microsoft.com/office/drawing/2014/chartex"
    xmlns:cx1="http://schemas.microsoft.com/office/drawing/2015/9/8/chartex"
    xmlns:cx2="http://schemas.microsoft.com/office/drawing/2015/10/21/chartex"
    xmlns:cx3="http://schemas.microsoft.com/office/drawing/2016/5/9/chartex"
    xmlns:cx4="http://schemas.microsoft.com/office/drawing/2016/5/10/chartex"
    xmlns:cx5="http://schemas.microsoft.com/office/drawing/2016/5/11/chartex"
    xmlns:cx6="http://schemas.microsoft.com/office/drawing/2016/5/12/chartex"
    xmlns:cx7="http://schemas.microsoft.com/office/drawing/2016/5/13/chartex"
    xmlns:cx8="http://schemas.microsoft.com/office/drawing/2016/5/14/chartex"
    xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
    xmlns:aink="http://schemas.microsoft.com/office/drawing/2016/ink"
    xmlns:am3d="http://schemas.microsoft.com/office/drawing/2017/model3d"
    xmlns:wp14="http://schemas.microsoft.com/office/word/2010/wordprocessingDrawing"
    xmlns:w14="http://schemas.microsoft.com/office/word/2010/wordml"
    xmlns:w15="http://schemas.microsoft.com/office/word/2012/wordml"
    xmlns:w16cid="http://schemas.microsoft.com/office/word/2016/wordml/cid"
    xmlns:w16se="http://schemas.microsoft.com/office/word/2015/wordml/symex"
    xmlns:wpg="http://schemas.microsoft.com/office/word/2010/wordprocessingGroup"
    xmlns:wpi="http://schemas.microsoft.com/office/word/2010/wordprocessingInk"
    xmlns:wps="http://schemas.microsoft.com/office/word/2010/wordprocessingShape"
    mc:Ignorable="w14 w15 w16se w16cid wp14">
</w:document>
```

In above example, we can know that

+ In `<w:document>` tag, we define a document and configure metedata about the `Docx1.docx` file.
+ In `xmlns:ve="http://schemas.openxmlformats.org/markup-compatibility/2006"`, `ve` is a convention of `mc` namespace. This namespace indicates that markup compatibility targets to the url `http://schemas.openxmlformats.org/markup-compatibility/2006"`, indicating that it is compatible with markup language released in 2006.
+ In `xmlns:o="urn:schemas-microsoft-com:office:office"`, it targets to `urn:schemas-microsoft-com:office:office`
, indicating the office refers to Microsoft Office. 
+ In `xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships"`, it targets to the namespace `http://schemas.openxmlformats.org/officeDocument/2006/relationships`, indicating the relationship targets to `http://schemas.openxmlformats.org/officeDocument/2006/relationships` (in version Office 2006).
+ In `xmlns:m="http://schemas.openxmlformats.org/officeDocument/2006/math"`, it targets to `http://schemas.openxmlformats.org/officeDocument/2006/math`, indicating that it refers to math tool in version Office 2006.
+ In `xmlns:v="urn:schemas-microsoft-com:vml"`, it targets to `urn:schemas-microsoft-com:vml`, indicating the vml refers to vml developed by Microsoft.
+ In `xmlns:wp="http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing"`, it targets to `http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing`, indicating that it refers WordprocessingML Drawing in version Office 2006.
+ In `xmlns:w10="urn:schemas-microsoft-com:office:word"`, it targets to `urn:schemas-microsoft-com:office:word`, indicating that it is Word-10 specific.
+ In `xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main"`, it targets to `http://schemas.openxmlformats.org/wordprocessingml/2006/main`, indicating that its main functionality of WordProcessingML refers to that in version Office 2006.
+ In `xmlns:wne="http://schemas.microsoft.com/office/word/2006/wordml"`, it targets to `http://schemas.microsoft.com/office/word/2006/wordml`, indicating that its WNE refers to WordML in version Office 2006.
+ In `xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main"`, it targets to `http://schemas.openxmlformats.org/drawingml/2006/main`, indicating that its DrawingML refers to that in version Office 2006.
+ In `xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart"`, it targets to `http://schemas.openxmlformats.org/drawingml/2006/chart`, indicating that the chart refers that in version Office 2006.
+ In `xmlns:wpc="http://schemas.microsoft.com/office/word/2010/wordprocessingCanvas"`, it targets to `http://schemas.microsoft.com/office/word/2010/wordprocessingCanvas`, indicating that the WordProcessing Canvas refers that in version Office 2006.
+ In `xmlns:cx="http://schemas.microsoft.com/office/drawing/2014/chartex"`, it indicates the extension of chart package (with highest preceedence) refers to the release at 2014 from Microsoft Office.
+ In `xmlns:cx1="http://schemas.microsoft.com/office/drawing/2015/9/8/chartex"`, it indicates the extension of chart package refers to the release at 2015/09/08 from Microsoft Office.
+ In `xmlns:cx2="http://schemas.microsoft.com/office/drawing/2015/10/21/chartex"`, it indicates the extension of chart package refers to the release at 2015/10/21 from Microsoft Office.
+ In `xmlns:cx3="http://schemas.microsoft.com/office/drawing/2016/5/9/chartex"`, it indicates the extension of chart package refers to the release at 2016/5/9 from Microsoft Office.
+ In `xmlns:cx4="http://schemas.microsoft.com/office/drawing/2016/5/10/chartex"`, it indicates the extension of chart package refers to the release at 2016/5/10 from Microsoft Office.
+ In `xmlns:cx5="http://schemas.microsoft.com/office/drawing/2016/5/11/chartex"`, it indicates the extension of chart package refers to the release at 2016/5/10 from Microsoft Office.
+ In `xmlns:cx6="http://schemas.microsoft.com/office/drawing/2016/5/12/chartex"` , it indicates the extension of chart package refers to the release at 2016/5/12 from Microsoft Office.
+ In `xmlns:cx7="http://schemas.microsoft.com/office/drawing/2016/5/13/chartex"`, it indicates the extension of chart package refers to the release at 2016/5/13 from Microsoft Office.
+ In `xmlns:cx8="http://schemas.microsoft.com/office/drawing/2016/5/14/chartex"`, it indicates the extension of chart package refers to the release at 2016/5/14 from Microsoft Office.
+ In `xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"`, its other convention is `ve`. But it has higher preceedence.
+ In `xmlns:aink="http://schemas.microsoft.com/office/drawing/2016/ink"`, it targets to `http://schemas.microsoft.com/office/drawing/2016/ink`, indicating that the Drawing ink refers that in version Office 2016.
+ In `xmlns:am3d="http://schemas.microsoft.com/office/drawing/2017/model3d"`, it targets to `http://schemas.microsoft.com/office/drawing/2017/model3d`, indicating that the 3D Model Drawing refers that in version Office 2017.
+ In `xmlns:wp14="http://schemas.microsoft.com/office/word/2010/wordprocessingDrawing"`, it targets to `http://schemas.microsoft.com/office/word/2010/wordprocessingDrawing`, indicating that, for Office 2014 ,WordProcessing Drawing refers that in version Office 2010.
+ In `xmlns:w14="http://schemas.microsoft.com/office/word/2010/wordml"`, it targets to `http://schemas.microsoft.com/office/word/2010/wordml`, indicating that, for Office 2014, WordProcessingML refers that in version Office 2017.
+ In `xmlns:w15="http://schemas.microsoft.com/office/word/2012/wordml"`, it targets to `http://schemas.microsoft.com/office/word/2012/wordml`, indicating that, for Office 2015, WordProcessingML refers that in version Office 2012.
+ In `xmlns:w16cid="http://schemas.microsoft.com/office/word/2016/wordml/cid"`, it targets to `http://schemas.microsoft.com/office/word/2016/wordml/cid`, indicating that, for Office 2016, WordProcessingML Content Identifiers refers that in version Office 2016.
+ In `xmlns:w16se="http://schemas.microsoft.com/office/word/2015/wordml/symex"`, it targets to `http://schemas.microsoft.com/office/word/2016/wordml/cid`, indicating that, for Office 2015, WordProcessingML Symbol Extensibility refers that in version Office 2015.
+ In `xmlns:wpg="http://schemas.microsoft.com/office/word/2010/wordprocessingGroup"`, it targets to `http://schemas.microsoft.com/office/word/2016/wordml/cid`, indicating that WordProcessingML Grouping refers that in version Office 2010.
+ In `xmlns:wpi="http://schemas.microsoft.com/office/word/2010/wordprocessingInk"`, `wpi` is an old alternative name of `aink`. But it has lower preceedence.
+ In `xmlns:wps="http://schemas.microsoft.com/office/word/2010/wordprocessingShape"`,  it targets to `http://schemas.microsoft.com/office/word/2010/wordprocessingShape`, indicating that WordProcessingML Shapes refers that in version Office 2010.
+ In `mc:Ignorable="w14 w15 w16se w16cid wp14"`, it ignores the following namespace in this tag.</br>`xmlns:w14`</br>`xmlns:w15`</br>`xmlns:w16se`</br>`xmlns:w16cid`</br>`xmlns:wp14`.
  
### namespace in xml tag in OOXML
| namespace in xml tag | stands for (represented as tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w` | | Microsoft Word | indicates that it describes xml content of a Microsoft Word file.| w stands for Microsoft *W*ord | |

### namespace declared in `<w:wordDocument>`
You can know which namespaces in `xmlns` namespace are declared through finding `xmlns` in `<w:wordDocument>`.

| namespace in xml tag | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `o` | *O*ffice-specific namespace | it contains metadata about the Word document itself. | | |

### namespace and its attribute in OOXML
#### about `xmlns` namespace
##### attribute in `xmlns` namespace
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `xmlns:space` | | space | assign a value to determine how to deal with whitespace (i.e. ` `, `\t`,`\n`). | | |
| `xmlns:a` | | | specifies the namespace of `a` for DrawingML. | It usually in `<a:theme>`. | |

#### about `xml` namespace
##### attribute in `xml` namespace
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `xml:space` | | space | assign a value to determine how to deal with whitespace (i.e. ` `, `\t`,`\n`).

#### about `v` namespace
##### attribute in `v` namespace
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `v:ext` | | | specifies editing behavior for shapes created with these defaults. | | |

#### about `a` namespace
##### elements in `a` namespace
| elements in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| | | | | | |
| `<a:ln>` | | *l*i*n*e | defines the properties of a line. | | |
| `<a:prstDash>` | | *pr*e*s*e*t* dash | specifies a preset dash pattern. | | |
| `<a:custDash>` | | *cust*om dash | defines a custom dash pattern. | | |
| | | | | | |
| `<a:round>` | | | indicates that the join between these lines should be rounded. | | |
| `<a:bevel>` | | | specifies how the edges of a 3D shape or table cell should be rounded or angled, creating a visual depth effect. | | |
| | | | | | |
| `<a:txBody>` | | *t*e*x*t body | adds and formats text within a graphical object. | | |
| | | | | | |
| `<a:theme>` | | | defines the theme. | It is usually in `~/word/theme/theme1.xml` file. | |
| `<a:themeElements>` | | | acts a container that defines theme elements. | | |
| `<a:clrScheme>` | | | clear the color scheme and defines the color palette for the theme. | | |
| | | | | | |
| `<a:dk1>` | | dark 1 | dark 1. | | |
| `<a:lt1>` | | light 1 | light 1. | | |
| `<a:sysClr>` | | system color | configure something to system color. | | | 
| `<a:srgbClr>` | | *s*econdary *RGB* *c*olor | set's secondary RGB color. | | |
| `<a:accent1>` | | accent color 1 | defines the accent color 1.
| `<a:hlink>` | | *h*yper*link* | defines the properties of hyperlink. | | |
| `<a:folHlink>` | | *fol*lowed *h*yper*link* | defines the properties of followed hyperlink. | | |
| `<a:majorFont>` | | major font | defines the properties of major font. | | |
| `<a:minorFont>` | | *fol*lowed *h*yper*link* | defines the properties of minor font. | | |
| `<a:fmtScheme>` | | *f*or*m*a scheme | defines the properties of format scheme. | | |
| `<a:objectDefaults>` | | | default settings for objects. | | |
| `<a:extraClrSchemeLst/>` | | | would contain definitions for additional color schemes beyond the main "Office" scheme. | | |
| `<a:extLst>` | | | defines an extension list. | | |
| | | | | | |
| `<a:graphic>` | | | servers a container about an actual graph. | | |
| `<a:graphicData>` | | | configure properties about the actual graph. | | |
| `<a:graphicFrameLocks>` | | | specifies the locking properties for the graphic frame | | |
| `<a:blip>` | | blip | points to the actual image data that is stored elsewhere within the OOXML package. | | |
| `<a:stretch>` | | stretch | acts as a container whose child will be stretched to fit its content. | | It can have exactly one child. |
| `<a:fillRect>` | | fill *rect*angle | fills the rectangle | | It can have exactly one child. |
| | | | | | |
| `<a:xfrm>` | | transform | transforms the graphical object. | | |
| `<a:off>` | | *off*set | offsets the graphical object | | |
| `<a:ext>` | | *ext*ent | defines the width and height of the object's bounding box. | | |
| `<a:prstGeom>` | | *pr*e*s*e*t* *geom*etry | configures preset geometry, is used in DrawingML to define the basic shape of an object by referencing a predefined geometric form. | |
| `<a:custGeom>` | | *cust*om *geom*etry | defines your own custom geometry. | |
| `a:avLst` | | *a*djustment *v*alue *l*i*st* | specifies adjustment values for preset shapes that have adjustable parameters. | | |
| | | | | | |

### elements
##### namespace declaration about `a` namespace
###### namespace declaration in `<a:blip>`
| namespace declaration | description | notes | notice |
| :---------- | :----------- | :----- | :--- |
| `xmlns:r` | | | as discussed above |

##### attribute in `a` namespace
###### attribute in `<a:theme>`
| elements in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `name` | | | specifies the name of theme. | | |

###### attribute in `<a:graphic>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `a:spid` | | *s*ha*p*e *id*entifier | specifies shape identifier of the actual graph. | It is required. | |

###### attribute in `<a:graphicData>`
> [!NOTE]
> there are extensibility attributes (which is optional) in `<a:graphicData>` tag.

| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `a:uri` | | uri | specifies uri of the actual graph. | It is required. | |

###### attribute in `<a:graphicFrameLocks>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `a:noChangeAspect` | | No Change Aspect Ratio | a boolean value indicating whether the aspect ratio of the graphic frame is locked and cannot be changed. | | |
| `a:noResize` | | | a boolean value indicating whether graphic frame cannot be resized. | | |
| `a:noMove` | | |  a boolean value indicating whether the graphic frame cannot be moved. | | |
| `a:noRotate` | | |  a boolean value indicating whether the graphic frame cannot be rotated. | | |
| `a:noSelect ` | | |  a boolean value indicating whether the graphic frame cannot be selected. | | |
| `a:noChangeArrowheads` | | |  a boolean value indicating whether the arrowheads of any lines within the graphic frame can not be changed. | | |
| `a:noEditPoints` | | |  a boolean value indicating whether the points of any shapes within the graphic frame can not be editable. | | |
| `a:noAdjustHandles` | | |  a boolean value indicating whether the points of within the graphic frame can not be modified by adjustment handles. | | |
| `a:noChangeShapeType` | | |  a boolean value indicating whether the type of within the graphic frame can not be changed. | | |

> [!NOTE]
> Specifying the value `"false"` or `"0"` (in attributes of `<a:graphicFrameLocks>`) means the action can be done.
>
> Otherwise, specifying the value `"true"` or `"1"` (in attributes of `<a:graphicFrameLocks>`) means the action can NOT be done.
>
> For example,
>
> In `<a:graphicFrameLocks noResize="true">`, the graphic frame can not be resized.

###### attribute in `<a:blip>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `r:embed` | | | specifies the relationship ID of the embedded image. | the relationship ID usually resides in `~/rel/rels.xml` file under a Word file. | |
| | | | | | | |
| `a:cstate` | | *c*ompression state | determines how to compress the image. | | |
| `a:alphaBiLevel` | | alpha bi-level threshold | specifies alpha bi-level threshold | | |
| `a:alphaCeiling` | | alpha ceiling | speficies alpha ceiling (i.e. the upper limit of alpha values) in the image | | |
| `a:alphaFloor` | | alpha floor | speficies alpha floor (i.e. the lower limit of alpha values) in the image | | |
| `a:alphaInverse` | | | a boolean value that determines whether the alpha value of the image is inversed. | | |
| `a:alphaMod` | | alpha *mod*ulation (調變) | multiplies the alpha values in the image by a specified percentage. | | |
| `a:alphaModFix` | | alpha *mod*ulation (調變) *fix*ed (修正後的結果) | sets a fixed alpha value (percentage) for the entire image | | overrides any existing alpha values. |
| | | | | | | |
| `a:blueOff` | | blue *off*set | offset (i.e. add additional) color blue value | | |
| `a:blueMod` | | blue *mod*ulation (調變) | multiplies the color blue values in the image by a specified percentage. | | |
| | | | | | | |
| `a:greenOff` | | green *off*set | offset (i.e. add additional) color green value | | |
| `a:greenMod` | | green *mod*ulation (調變) | multiplies the color green values in the image by a specified percentage. | | |
| | | | | | | |
| `a:redOff` | | red *off*set | offset (i.e. add additional) color red value | | |
| `a:redMod` | | red *mod*ulation (調變) | multiplies the color red values in the image by a specified percentage. | | |
| | | | | | | |
| `a:hue` | | hue | shifts the hue of the image by a specified angle (in degrees) | its unit is degrees. | |
| `a:hueMod` | | hue *mod*ulation (調變) | multiplies the color hue values in the image by a specified percentage. | | |
| | | | | | | |
| `a:brightness` | | brightness | adjusts the brightness of the image by a percentage. | | |
| `a:contrast ` | | contrast  | adjusts the contrast of the image by a percentage. | | |
| `a:gamma` | | gamma correction | applies the gamma correction of the image using a value represented as percentage. | | |
| `a:saturation` | | saturation | adjusts the color saturation of the image by a percentage. | | |
| `a:tint ` | | tint | applies a tint to the image | | |
| | | | | | | |
| `a:gray` | | grayscale mode | a boolean value that determines whether the image is in grayscale. | | |

###### attribute in `<a:fillRect>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `a:l` | | left | specifies the position of the **left** edge of the rectangle within the original fill, as a percentage. | For example, a value of "10%" means the left edge of the stretching region starts at 10% of the original fill's width from the left. | |
| `a:t` | | top | specifies the position of the **top** edge of the rectangle within the original fill, as a percentage. | For example, "20%" means the top edge starts at 20% of the original fill's height from the top. | |
| `a:r` | | right | specifies the position of the **right** edge of the rectangle within the original fill, as a percentage. | For instance, "90%" means the right edge of the stretching region is at 90% of the original fill's width from the left (or 10% from the right edge). | |
| `a:b` | | bottom | specifies the position of the **bottom** edge of the rectangle within the original fill, as a percentage. | For example, "80%" means the bottom edge is at 80% of the original fill's height from the top (or 20% from the bottom edge).| |

> [!IMPORTANT]
> If any of these attributes are omitted, the corresponding edge of the fill rectangle defaults to the edge of the original fill
>
> (i.e., l and t default to 0%, and r and b default to 100%).

###### attribute in `<a:xfrm>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `a:flipH` | | flip *h*orizontally | a boolean value to determine whether flips horizontally a graphical object | | |
| `a:flipV` | | flip *v*ertically | a boolean value to determine whether flips vertically a graphical object | | |
| `rot` | | rotation | rotates the graphical object clockwisely in degrees. | <ol><li>its unit is in sixtieths of a degree.</li><li>positive values indicate clockwise rotation, and negative values indicate counter-clockwise rotation.</li></ol> | The default value is `"0"`. |

###### attribute in `<a:off>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `a:x` | | horizontal offset | sets horizontal offset | its unit is EMU. | coordinates of the top-left corner of a graphical object's bounding box relative to its parent. |
| `a:y` | | vertical offset | sets vertical offset | its unit is EMU. | coordinates of the top-left corner of a graphical object's bounding box relative to its parent. |

###### attribute in `<a:ext>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `a:cx` | | *c*oordinate *X* | sets width of the bounding box | its unit is EMU. | |
| `a:cy` | | *c*oordinate *Y* | sets height of the bounding box | its unit is EMU. | |

###### attribute in `<a:prstGeom>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `a:prst` | | *pr*e*s*e*t* | specific predefined shape  | | It is required |

###### example 1.1 -- a simple drawing object
```
<w:drawing>
          <wp:inline distT="0" distB="0" distL="0" distR="0" wp14:anchorId="56C264D6" wp14:editId="7AA34E44">
            <wp:extent cx="5486400" cy="3200400" />
            <wp:effectExtent l="0" t="0" r="0" b="0" />
            <wp:docPr id="1" name="圖表 1" />
            <wp:cNvGraphicFramePr />
            <a:graphic xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main">
              <a:graphicData uri="http://schemas.openxmlformats.org/drawingml/2006/chart">
                <c:chart xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart" xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships" r:id="rId4" />
              </a:graphicData>
            </a:graphic>
          </wp:inline>
</w:drawing>
```

In above example, we can know that

+ In `<w:drawing>`, it defines the presence of a drawing object.
+ In `<wp:inline distT="0" distB="0" distL="0" distR="0" wp14:anchorId="56C264D6" wp14:editId="7AA34E44">`, it defines an inline drawing object.

    - the distance (in points) between the drawing object and the surrounding text on the top, bottom, left, and right are BOTH set to zero respectively.
    - it is specific to WordprocessingML version 2010 and later (indicated by the wp14 namespace prefix) and sets its edit id as `7AA34E44`.

+ In `<wp:extent cx="5486400" cy="3200400" />`, it specifies the size ( in this order -- (width, height)) of the drawing object is (5486400,3200400) EMUs.
+ In `<wp:effectExtent l="0" t="0" r="0" b="0" />`, it indicates no additional space is needed for effects.
+ In `<wp:docPr id="1" name="圖表 1" />`, it holds document-level properties for the drawing object whose id is `1` and name is `圖表 1`.
+ In `<wp:cNvGraphicFramePr />`, it defines Common Non-Visual Graphic Frame Properties. Since it has no child, it suggest no specific locking. 

> [!TIP]
> When `<wp:cNvGraphicFramePr />` element has no child,
>
> it can be assumed that there is a `<a:graphicFrameLocks>` element whose value of all attributes are BOTH set to `"false."`,
>
> thus, the graphic frame has no specific locking.

+ In `<a:graphic xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main">`, it contains the actual graphical content.
+ In `<a:graphicData uri="http://schemas.openxmlformats.org/drawingml/2006/chart">`, it specifies the type of graphic data

      - In `uri="http://schemas.openxmlformats.org/drawingml/2006/chart"`, it specifies the graph data is a chart.

+ In `<c:chart xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart" xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships" r:id="rId4" />`, it comes from the ChartML namespace (c:), references the actual chart data. And its id is `rId4`, we can found the actual chart definition according to the `r:id` whose value os `rId4`.
  
###### example 1.2 -- a complex drawing object
part content of `~/word/document.xml` file under `PictureExample1.docx` file.

```
<!-- other tags omitted -->
<w:p>
    <w:pPr>
        <!-- tags inside is omitted -->
    <w:pPr/>
        <w:r>
            <w:rPr>
                <w:lang w:val="zh-TW"/>
            </w:rPr>
            <w:t>Here is Ai</w:t>
        </w:r>
        <w:r>
            <w:br/>
        </w:r>
        <w:r xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">
            <w:drawing>
                <wp:inline xmlns:wp="http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing" distT="0" distB="0" distL="0" distR="0">
                    <wp:extent cx="5080000" cy="5080000"/>
                    <wp:effectExtent l="0" t="0" r="0" b="0"/>
                    <wp:docPr id="1" name="" descr=""/>
                    <wp:cNvGraphicFramePr>
                        <a:graphicFrameLocks xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main" noChangeAspect="1"/>
                    </wp:cNvGraphicFramePr>
                    <a:graphic xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main">
                        <a:graphicData uri="http://schemas.openxmlformats.org/drawingml/2006/picture">
                            <pic:pic xmlns:pic="http://schemas.openxmlformats.org/drawingml/2006/picture">
                                <pic:nvPicPr>
                                    <pic:cNvPr id="0" name=""/>
                                    <pic:cNvPicPr/>
                                </pic:nvPicPr>
                            <pic:blipFill>
                                <a:blip xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships" r:embed="R530625ccf2364ebb"/>
                                <a:stretch>
                                    <a:fillRect/>
                                </a:stretch>
                            </pic:blipFill>
                            <pic:spPr>
                                <a:xfrm flipH="0" flipV="0">
                                    <a:off x="0" y="0"/>
                                    <a:ext cx="5080000" cy="5080000"/>
                                </a:xfrm>
                                <a:prstGeom prst="rect">
                                    <a:avLst/>
                                </a:prstGeom>
                            </pic:spPr>
                        </pic:pic>
                    </a:graphicData>
                </a:graphic>
            </wp:inline>
        </w:drawing>
    </w:r>
</w:p>
```

In above example, we can know that

+ In `<w:p>`, it defines a paragraph.
+ In first occurence of `<w:r>`, it defines a run.
+ In `<w:rPr>` (inside first occurence of `<w:r>`), it defines the properties of the run.
+ In `<w:lang w:val="zh-TW"/>` (inside `<w:rPr>`), it speficies the text that uses this run is in language Traditional Chinese (that used in Taiwan).
+ In `<w:t>Here is Ai</w:t>` (inside first occurence of `<w:r>`), the text `Here is Ai` is applied to this run.
+ In third occurence of `<w:r xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">`, it defines a run and its `xmlns:w` namespace targets to `http://schemas.openxmlformats.org/wordprocessingml/2006/main`, which means it uses WordPrcoessingML in Office 2006.
+ In `<w:drawing>`, it defines a drawing object.
+ In `<wp:inline xmlns:wp="http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing" distT="0" distB="0" distL="0" distR="0">`,</br>it defines a inline drawing object.</br>Its `xmlns:wp` namespace targets to `http://schemas.openxmlformats.org/drawingml/2006/wordprocessingDrawing`,</br>which meaning that it use an extension of WordProcessing DrawingML in Office 2006.</br></br>On the other hand, the distance between the top edge of the inlined drawing object and the top edge of the drawing object (defined in `<w:drawing>`) is zero.</br>Similarly, the distance between the left edge of the inlined drawing object and the left edge of the drawing object (defined in `<w:drawing>`) is zero.</br>The distance between the bottom edge of the inlined drawing object and the bottom edge of the drawing object (defined in `<w:drawing>`) is zero.</br>Similarly, the distance between the right edge of the inlined drawing object and the right edge of the drawing object (defined in `<w:drawing>`) is zero.</br>These four attributes indicates that they are overlapped.
+ In `<wp:extent cx="5080000" cy="5080000"/>`, the inlined drawing object is set to 5080000 width (in EMUs) and 7 `5080000` height (in EMUs).
+ In `<wp:effectExtent l="0" t="0" r="0" b="0"/>`, the inlined drawing object (add additionals to any edge by zero), mean ing that it does NOT add additionals to any edge.
+ In `<wp:docPr id="1" name="" descr=""/>`, we can know the properties of inline drawing object. Its id is `1`> Its name is an empty string. Its description is also an empty string.
+ In `<wp:cNvGraphicFramePr>`, it defines the properties for the common non-visual graphic frame.
+ In `<a:graphicFrameLocks xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main" noChangeAspect="1"/>`, it speficies the behaviour of the graphic frame lock for this inline drawing object.</br></br>Its `xmlns:a` namespace targets to `http://schemas.openxmlformats.org/drawingml/2006/main`, which means that it is applied to DrawingML in Office 2006.</br>The inlined drawing object can not change aspect ratio.
+ In `<pic:pic xmlns:pic="http://schemas.openxmlformats.org/drawingml/2006/picture">`, it defines a picture which uses DrwaingML in Office 2006.
+ In `<pic:nvPicPr>`, it defines the properties to non-visual picture.
+ In `<pic:cNvPr id="0" name=""/>`, it defines the properties of the common non-visual. It also sets its id to `0` and name to an empty string.
+ In `<pic:blipFill>`, it is the bridge between the abstract shape defined for the picture and the concrete image data that gets rendered within that shape.
+ In `<a:blip xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships" r:embed="R530625ccf2364ebb"/>`, it defines a binary large object picture7. Its `xmlns:r` targets to `http://schemas.openxmlformats.org/officeDocument/2006/relationships` which means that it is applied to Relationships of Office 3006. It embeded id is `rR530625ccf2364ebb`.
+ In `<a:stretch>`, the child element must be strecthed to fit its content.
+ In `<a:fillRect/>`, it will stretched as a filed rectangle.
+ In `<pic:spPr>`, it defines the properties of shape.
+ In `<a:xfrm flipH="0" flipV="0">`, sets its transform, 4it will be flio horizontally and veritcally.
+ In `<a:off x="0" y="0"/>`, it sets the offest of x-coordinaate and y-coordinate is 0.
+ In `<a:ext cx="5080000" cy="5080000"/>`, the width and height is set to `5080000` and  `5080000`, respectively.
+ In <a:prstGeom prst="rect">, it sets the preset goemetry is `rectangle`.
+ In `<avLst/>`, specific preset geometry being used (in our case, a rectangle), no adjustments are being applied,

The above example may output:

<img width="371" alt="image" src="https://github.com/user-attachments/assets/458af2fd-4c32-4b33-aad3-69b227a17cb0" />

### element and its attribute in xml tag in OOXML
#### about `c` namespace
> [!NOTE]
>
> Convention about phrase definition:
> 
> For convience,
>
> about the phrase `this file`, if `this file` is not explicited discussed in this record, `this file` refers to `~/word/charts/chart1.xml file under a Word file.`

##### elements in `c` namespace
| elements | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `<c:chartSpace>` | | chart space | the root tag that contains many charts and its configuration. | It usually resides in `~/word/charts/chart1.xml` file under a Word file. | |  
| `<c:roundedCorners>` | | rounded corners | determines whether all charts in this file should be rounded shape. | | |
| | | | | | |  
| `<c:chart>` | | chart | defines a chart | | | 
| `<c:autoTitleDeleted>` | | auto-generated deleted title | indicates whether the user has deleted the auto-generated title.  | | |
| `<c:plotArea>` | | plot area | defines a plot area | | |
| `<c:layout/>`| | layout | defines a layout for the plot area | | |
| `<c:barChart>` | | bar chart | configure the chart is bar chart | | |
| `<c:pieChart>` | | pie chart | configure the chart is pie chart | | |
| | | | | | |
| `<c:barDir>` | | bar *dir*ection | configure the orientation of bars. | This tag must be defined inside a bar chart (i.e. `<c:barChart>` tag) | |
| `<c:grouping>` | | grouping | specifies how multiple data series within the same category should be grouped together visually. | | |
| `<c:overlap>` | | overlap | specifies, for different data series that belong to the same category, the degree that it will overlap each other. | It is relevant when you have multiple data series in a bar chart (or column chart) and the value of the attribute `val` in `<c:grouping>` tag is set to something other than `stacked` or `percentStacked`. | |
| | | | | | |
| `<c:gapWidth>` | | gap width | specifies the gap width (i.e. the distance between two bars) | | |
| | | | | | |
| `<c:dLbls>` | | *d*ata *l*a*b*e*l**s* | a container that contains data labels. | | |
| `<c:showLegendKey/>` | | show legend key | determines whether show legend for each series | | |
| `<c:showVal/>` | | show *val*ue | determines whether show value for each series | | |
| `<c:showCatName/>` | | show *cat*gory name | determines whether show category name for each series | | | 
| `<c:showSerName/>` | | show *ser*ies name | determines whether show name of data series for each series | | | 
| `<c:showPercent/>` | | show percentage | determines whether show percentage that a data point takes of its total for each series | For more knowledgment about data point, see following `IMPORTANT` annotation. | |
| `<c:showBubbleSize/>` | | show bubble size | determines whether show bubble size for each series. | | |
| `<c:showLeaderLines/>` | | show leader lines | determines whether show leader lines for each series. | | |
| | | | | | |
| `<c:ser>` | | *ser*ies | defines a series. | | |
| `<c:idx>` | | *i*n*d*e*x* | specifies the index of the data point. | | It is zero-based. |
| `<c:order>` | | plotting order | specifies the plotting order of the series (inside `<c:ser>` tag). | | It is zero-based. |
| `<c:order>` | | plotting order | specifies the plotting order of the series (inside `<c:ser>` tag). | | It is zero-based. | 
| `<c:val>` | | value | specifies the actual data value of the series (inside `<c:ser>` tag). | | | 
| `<c:extLst>` | | *ext*ension *l*i*st* | defines an extensibility point for future additions. | | | 
| `<c:tx>` | | series *t*e*x*t | specifies the name of series. | it appears in the legend and</br>might be used in data labels. | |
| `<c:errBars>` | | error bars | defines error bars for the data points in this series. | |  This is available for</br><ol><li>bar charts</li><li>column (bar) charts</li></ol> |
| `<c:spPr>` | | *s*ha*p*e *pr*operties | specifies visual properties for the series as a whole. | | |
| `<c:cat>` | | *cat*egory | specifies the categories or labels for the data points in this series. | | |
| `<c:bubbleSize>` | | bubble size | specifies the size of bubbles. | | |
| `<c:trendline>` | | trend line | defines trendlines for this specific series | | |
| `<c:marker>` | | marker | defines the appearance of marker of data point. | | This is available for</br><ol><li>line charts</li><li>scatter charts</li></ol> |
| `<c:invertIfNegative>` | | | determines whether the color (of bar charts or column charts) will be inverted when its value it represents is negative. | | This is available for</br><ol><li>bar charts</li><li>column charts</li></ol>  |
| | | | | | |
| `<c:strRef>` | | *str*ing *ref*erence | defines a reference to string data in a spreadsheet. | | |
| `<c:f>` | | *f*ormula | contains the formula that specifies the range of cells in the spreadsheet. | | |
| | | | | | |
| `<c:strCache>` | | *str*ing cached | contains a cached copy of the string values from the referenced range.  | this is often included for performance reasons, so the charting application doesn't have to always access the spreadsheet to get the labels | |
| `<c:ptCount>` | | *p*oin*t* count | the number of point in cached copy of string values or numerical values (according to the value of `val` attribute) | | |
| `<c:pt>` | | *p*oin*t* | defines a point in cached copy of string values or numerical values | | |
| `<c:v>` | | value | the actual data value of a point in cached copy of string values or numerical values | | |
| | | | | | |
| `<c:numCache>` | | *num*ber cached | contains a cached copy of the numerical values from the referenced range.  | this is often included for performance reasons, so the charting application doesn't have to always access the spreadsheet to get the labels | |
| `<c:formatCode>` | | number formatting code | specifies the number formatting code that was applied to the original data in the spreadsheet. | |
| | | | | | |
| `<c:catAx>` | | *cat*egory *ax*is | defining the category axis for some types of charts. | | |
| `<c:axId>` | | *ax*is id | specifies axis id | | |
| `<c:scaling>` | | scaling | controls scaling for axis | | |
| `<c:orientation>` | | orientation | controls orientation for axis | | |
| | | | | | |
| `<c:delete>` | | manually deleted | stores the data labels is manually deleted by users. | | |
| `<c:axPos>` | | | specifies the defined axis should be positioned at somewhere of the chart's plot area. | somewhere is according to value of `val` attribute, see [`<c:axPos>` -> `val` attribute section in Appendix 2](https://github.com/40843245/OOXML/blob/main/Word/structure/Appendix%202%20--%20available%20options%20of%20attribute%20of%20tag%20in%20xml%20for%20Word.md#caxpos---val-attribute) for available value of `val` attribute.  | |
| `<c:majorTickMark/>` | | major tick mark | specifies the type and placement of the major tick marks. | | |
| `<c:minorTickMark/>` | | minor tick mark | specifies the type and placement of the minor tick marks. | | |
| `<c:tickLblPos/>` | | position of the tick labels | controls the position of the tick labels relative to the tick marks on the axis. | | |
| `<c:crossAx/>` | | cross *ax*is | establishes a relationship between the current axis and another axis in the chart. | The point at which they cross can be further defined by the <c:crossAt> element. | |
| `<c:auto/>` | | | determines the axis settings are automatic or manual by given boolean value. | | |
| `<c:lblAlgn>` | | *l*a*b*e*l* *a**l*i*g**n*ment | determines alignment of the text within the axis labels. | | |
| `<c:lblOffset>` | | *l*a*b*e*l* offset | specifies the offset of the axis labels from the axis line. | | |
| `<c:noMultiLvlLbl>` | | no multi-*l*e*v*e*l* *l*a*b*e*l* | determines whether multi-level labels are disabled on the category axis. | | |
| | | | | | |
| `<c:valAx>` | | *val*ue *ax*is | acts like a container that defines the one or many value axes (plural of axis) | | |
| `<c:axPos/>` | | *ax*is *pos*iton | specifies the position of the axis relative to the plot area of the chart | | |
| `<c:numFmt/>` | | *num*ber *f*or*m*a*t*ting  | specifies the number formatting of the axis labels of the chart | | |
| | | | | | |
| `<c:majorGridlines/>` | | major grid lines | indicates the presence or formatting of major grid lines in a chart. | | |
| `<c:minorGridlines/>` | | minor grid lines | indicates the presence or formatting of minor grid lines in a chart. | | |
| `<c:crosses/>` | | | specifies how the axes cross each other.  | | |
| `<c:crossBetween/>` | | | specifies how category axes are crossed by value axes in a chart.  | | |
| | | | | | |
| `<c:legend>` | | | acts like a container that contains all legend. | | |
| `<c:legendPos>` | | | specifies the position of the legend. | | |
| `<c:legendEntry>` | | | acts like a container for individual entries within the legend. | | |
| | | | | | |
| `<c:plotVisOnly>` | | plot *vis*ibile data points only | controls whether only visible data points are plotted on a chart. | | |
| `<c:dispBlanksAs>` | | *disp*lay blank as | specifies how blank cells should be handled when plotting data on a chart. | | | 
| `<c:showDLblsOverMax>` | | show *d*ata *l*a*b*e*l*s when is over *max*imum | determines whether data labels should be displayed even if their value exceeds the maximum value set for the chart's axis. | | | 

> [!IMPORTANT]
> How to calculate percentage that a data point takes of its total?
>
> See this article -- [How to calculate percentage that a data point takes of its total?](https://github.com/40843245/drawing-objects/blob/main/formula/graphics/chart/data%20point.md)

##### namespace declaration about `c` namespace
###### namespace declaration in `<c:chart>`
| namespace declaration | description | notes | notice |
| :---------- | :----------- | :----- | :--- |
| `xmlns:c` | | | as discussed above |
| `xmlns:r` | | | as discussed above |

##### attribute about `c` namespace
###### attribute in `<c:chart>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `style` | | | speficies the style of the chart. | | |

###### attribute in `<c:roundedCorners>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | determines whether all charts in this file should be rounded shape. | | |

###### attribute in `<c:autoTitleDeleted>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | determines whether a chart title is automatically generated by the charting application (e.g. Excel or PowerPoint) if it has been manually deleted by the user. | | |

###### attribute in `<c:barDir>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | determines the orientation of bars. | | |

###### attribute in `<c:grouping>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | determines the grouping method | | |

###### attribute in `<c:gapWidth>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | specifies the gap width (i.e. the distance between two bars) | | |

###### attribute in `<c:overlap>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | specifies, for different data series that belong to the same category, the degree that it will overlap each other.  | | |

###### attribute in `<c:showLegendKey>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | determines whether show legend for each series. | | |

###### attribute in `<c:showVal>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | determines whether show value for each series. | | |

###### attribute in `<c:showCatName>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | determines whether show category name for each series. | | |

###### attribute in `<c:showSerName>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | determines whether show name of data series for each series | | |

###### attribute in `<c:showPercent>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | determines whether show percentage that a data point takes of its total for each series | | |

###### attribute in `<c:showBubbleSize>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | determines whether show bubble size for each series. | | |

###### attribute in `<c:showLeaderLines>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | determines whether show leader lines for each series. | | |

###### attribute in `<c:ptCount>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | stores the number of cached copy of string value or numerical values | | |

###### attribute in `<c:idx>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | specifies the index of data point | | It is zero-based |

###### attribute in `<c:invertIfNegative>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | determines whether the color (of bar charts or column charts) will be inverted when its value it represents is negative. | | |

###### attribute in `<c:axId>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | specifies the axis id | | |

###### attribute in `<c:scaling>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `logBase` | | | specifies the base for a logarithmic scale. If present, the axis will use a logarithmic scale with the given base. | | |
| `orientation` | | orientation | | specifies the orientation of the value axis. | | |
| `type` | | type | specifies the scaling type for the category axis | | | 

###### attribute in `<c:orientation>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | specifies the orientation of the value axis. | | |

###### attribute in `<c:delete>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | stores the data labels is manually deleted by users. | | |

###### attribute in `<c:axPos>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | specifies the defined axis should be positioned at somewhere of the chart's plot area. | somewhere is according to value of `val` attribute, see [`<c:axPos>` -> `val` attribute section in Appendix 2](https://github.com/40843245/OOXML/blob/main/Word/structure/Appendix%202%20--%20available%20options%20of%20attribute%20of%20tag%20in%20xml%20for%20Word.md#caxpos---val-attribute) for available value of `val` attribute.  | |

###### attribute in `<c:majorTickMark>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | specifies the type and placement of the major tick marks. | | |

###### attribute in `<c:minorTickMark>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | specifies the type and placement of the minor tick marks. | | |

###### attribute in `<c:tickLblPos>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | controls the position of the tick labels relative to the tick marks on the axis. | | |

###### attribute in `<c:crossAx>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | holds the Guid of the of the axis (value of `val` attribute in `<c:axId>`) that the current axis should cross. | the relationship will cross from the current axis by its id (value of `val` attribute in `<c:crossAx>`) to the axis by its id (value of `val` attribute in `<c:axId>`)  | |

> [!IMPORTANT]
> About `How <c:crossAx> tag establish the relationship to cross the axis`, let's see the answers from [Google Gemini](https://github.com/40843245/OOXML/blob/main/Q%26A/about%20chart/about%20axis/How%20%60%3Cc%3AcrossAx%3E%60%20tag%20establish%20the%20relationship%20to%20cross%20the%20axis%3F.md)

###### attribute in `<c:auto>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | determines the axis settings are automatic or manual by given boolean value. | | |

###### attribute in `<c:lblAlgn>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | determines alignment of the text within the axis labels. | | |

###### attribute in `<c:lblAlgn>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | specifies the offset of the axis labels from the axis line. | | It takes the percentage of the default area. |

###### attribute in `<c:noMultiLvlLbl>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | determines whether multi-level labels are disabled on the category axis. | | |

###### attribute in `<c:axPos>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | specifies the position of the axis relative to the plot area of the chart. | | |

###### attribute in `<c:numFmt>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `sourceLinked` | | | specifies that source is linked. | | |
| `formatCode` | | number formattig code | specifies number formattig code. | | |

###### attribute in `<c:crosses>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | specifies how axes crosses each other | | |

###### attribute in `<c:crossBetween>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `val` | | | specifies how category axes are crossed by value axes in a chart. | | |

###### attribute in `<c:legendPos>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"top"` | | | specifies how category axes are crossed by value axes in a chart. | | |

###### attribute in `<c:plotVisOnly>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"val"` | | | determines whether only the currently visible data points in the source data range for the chart should be plotted.  | | |

###### attribute in `<c:dispBlanksAs>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"val"` | | | specifies how blank cells should be handled when plotting data on a chart. | | |

###### attribute in `<c:showDLblsOverMax>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"val"` | | | specifies whether data labels should be displayed even if their value exceeds the maximum value set for the chart's axis. | | |

> [!IMPORTANT]
> About implications of this setting,
>
> see my note -- [implication about charts#implication#graphics#charts](https://github.com/40843245/drawing-objects/blob/main/implication/graphics/charts/implication%20about%20charts.md#charts)

##### examples and explanations
###### example 1.1 -- chart space
root node of `~/word/charts/chart1.xml` file under `BarChartExample.docx` file.

```
<c:chartSpace xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart" xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main" xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships">
```

In above example, we can know that

+ In `<c:chartSpace>`, it defines a chart space that containing all charts and its configurations.
+ In `xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart"`, the namespace `xmlns:c` targets to `http://schemas.openxmlformats.org/drawingml/2006/chart`, which means that it uses DrawingML Chart Schema in Office 2006.
+ In `xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main"`, the namespace `xmlns:a` targets to `http://schemas.openxmlformats.org/drawingml/2006/main`, which means that it uses DrawingML in Office 2006.
+ In `xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships"`, the namespace `xmlns:r` targets to `http://schemas.openxmlformats.org/officeDocument/2006/relationships`, which means that it uses the Relationship Schema in Office 2006.

###### example 2.1 -- cached copy of string values
If a chart's category labels are "A", "B", and "C" pulled from a spreadsheet, 

the xml content may look like this:

```
<c:strCache>
  <c:ptCount val="3"/>
  <c:pt>
    <c:idx val="0"/>
    <c:v>A</c:v>
  </c:pt>
  <c:pt>
    <c:idx val="1"/>
    <c:v>B</c:v>
  </c:pt>
  <c:pt>
    <c:idx val="2"/>
    <c:v>C</c:v>
  </c:pt>
</c:strCache>
```

###### example 2.2 -- cached copy of numerical values
Let's say you have numerical data 10.5, 20.3, and 15.8 in cells B2 to B4 of Sheet1 in your spreadsheet, 

formatted as numbers with one decimal place.

It xml content may look like this:

```
<c:val>
  <c:numRef>
    <c:f>Sheet1!$B$2:$B$4</c:f>
    <c:numCache>
      <c:formatCode val="#,##0.0"/>
      <c:ptCount val="3"/>
      <c:pt>
        <c:idx val="0"/>
        <c:v>10.5</c:v>
      </c:pt>
      <c:pt>
        <c:idx val="1"/>
        <c:v>20.3</c:v>
      </c:pt>
      <c:pt>
        <c:idx val="2"/>
        <c:v>15.8</c:v>
      </c:pt>
    </c:numCache>
  </c:numRef>
</c:val>
```

###### example 3 -- a full chart
The original files are placed at [BarChartExample.docx](https://github.com/40843245/OOXML/tree/main/examples/documents/Word/charts/BarChartExample.docx)

The explanation is available at [example-and-explanation.md](https://github.com/40843245/OOXML/blob/main/examples/documents/Word/charts/BarChartExample.docx/example-and-explanation.md)

#### about `pic` namespace
##### namespace in `pic` namespace
| namespace | description | notes | notice |
| :---------- | :----------- | :----- | :--- |
| `pic:pic` | | | |

##### elements in `pic` namespace
| elements in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `<pic:nvPicPr>` | | *N*on-*v*isual *Pic*ture *Pr*operties | acts as a container that contains Non-Visual Picture Properties | | |
| `<pic:cNvPr>` | | *C*ommon *N*on-*v*isual Picture *Pr*operties | defines Common Non-visual Picture Properties | | |
| `<pic:blipFill>` | | | defines how the actual image data is used to fill the shape of the picture object. | it controls aspects like tiling, stretching, and the portion of the image that is visible. | |
| `<pic:spPr>` | | *s*ha*p*e *pr*operties | defines shape properties| | |

##### attribute about `pic` namespace
###### attribute in `<pic:cNvPr>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `id` | | | speficies the id. | | |
| `name` | | | speficies the name. | | |

#### about `o` namespace
`o` namespace contains metadata about the Word document itself.

##### elements in `o` namespace
| attribute in xml tag | stands for (represented as tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `<o:DocumentProperties>` | | document property | defines a property for the document itself. | | |
| `<o:Subject>` | | document subject | configures the subject of the document itself. | | |
| `<o:Author>` | | document author | configures the author of the document itself. | | |
| `<o:Keywords>` | | document keywords | configures keywords or tags associated with the document itself. | | |
| `<o:Description>` | | document description | configures the description of the document itself. | | |
| `<o:LastAuthor>` | | last saved author | configures the author who saved the document itself recently. | | |
| `<o:Revision>` | | document revision number | configures the revision number of the document itself recently. | | |
| `<o:TotalTime>` | | total time | stores the total time spent on the document itself. | | |
| `<o:LastPrinted>` | | last printed date and time | stores the date and time of last print to the document itself. | | |
| `<o:Created>` | | created date and time | stores the date and time the document was created. | | |
| `<o:LastSaved>` | | last saved date and time | stores the date and time the document was last saved. | | |
| `<o:Company>` | | company | stores the company or organization associated with the document. | | |
| `<o:Manager>` | | manager | stores the manager or responsible person for the document. | | |
| `<o:Category>` | | category | stores the category of the document. | | |
| `<o:PresentationFormat>` | | Presentation Format | The format used when saving as a presentation. | | |
| `<o:Bytes>` | | bytes | estimated of the document size in bytes. | | |
| `<o:Words>` | | words | estimated of the number of words in the document. | | |
| `<o:Characters>` | | characters | estimated of the number of characters in the document. | excluding spaces. | |
| `<o:CharactersWithSpaces>` | | characters | estimated of the number of characters in the document. | including spaces. | |
| `<o:Lines>` | | lines | estimated of the number of lines in the document. | | |
| `<o:Paragraphs>` | | paragraphs | estimated of the number of paragraphs in the document. | | |
| `<o:Version>` | | version | The version number of the application that created the document. | | |
| `<o:GUID>` | | Guid | Guid of the document. | | |
| `<o:HyperlinkBase>` | | base of hyperlink | The base path or URL for hyperlinks within the document. | | |
| `<o:Slides>` | | slides | estimated of the number of slides in the Slide. | (Potentially for PowerPoint documents etc embedded in Word) | |
| `<o:HiddenSlides>` | | notes | estimated of the number of hidden slides in the document. | (Potentially for PowerPoint documents etc embedded in Word) | |
| `<o:Notes>` | | notes | estimated of the number of notes in the document. | (Potentially for notes in the document). | |
| `<o:MMClips>` | | *M*utli*m*edia clips | estimated of the number of mutlimedia clips in the document. | (Potentially for embededded mutlimedia in the document). | |
| | | | | | |
| `<o:shapedefaults/>` | | | specifies the default properties for newly created shapes within a drawing canvas. | | |
| `<o:shapelayout>`| | | acts a container that holds information about how shapes are laid out and interact with the surrounding text. | | |
| `<o:idmap/>` | | | defines the map id. | | |

##### attribute about `o` namespace
###### attribute in `<o:shapedefaults>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `v:ext` | | | | explained in ``attribute in `v` namespace`` section | |
| `spidmax` | | max *s*ha*p*e *id* | sets the maximum Shape ID that can be assigned to new shapes created within the current drawing canvas. | 

###### attribute in `<o:shapelayout>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `v:ext` | | | | explained in ``attribute in `v` namespace`` section | |

###### attribute in `<o:idmap>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `v:ext` | | | | explained in ``attribute in `v` namespace`` section | |
| `data` | | | specifies the current shape ID. | The id of newly create shape will be value of `data` attribute plus one. | |

##### examples and explanation
###### example 1.1 -- xml content of metadata file
the xml content of metadata file in `Docx1.docx` file.

```
<o:DocumentProperties>
   <o:Title>Docx1</o:Title>
   <o:Author>40843245</o:Author>
   <o:LastAuthor>40843245</o:LastAuthor>
   <o:Revision>2</o:Revision>
   <o:TotalTime>0</o:TotalTime>
   <o:LastPrinted>2016-06-13T09:16:00Z</o:LastPrinted>
   <o:Created>2016-12-13T04:53:00Z</o:Created>
   <o:LastSaved>2016-12-13T04:53:00Z</o:LastSaved>
   <o:Pages>1</o:Pages>
   <o:Words>70</o:Words>
   <o:Characters>405</o:Characters>
   <o:Company>NFU</o:Company>
   <o:Lines>3</o:Lines>
   <o:Paragraphs>1</o:Paragraphs>
   <o:CharactersWithSpaces>474</o:CharactersWithSpaces>
   <o:Version>15</o:Version>
</o:DocumentProperties>
```

In above example, we can know that

+ To look at `<o:DocumentProperties>` tag, it contains metadata about `Docx1.docx` file.
+ In `<o:Title>Docx1</o:Title>`, its title is `Docx1`.
+ In `<o:Author>40843245</o:Author>`, the author of document when it is created is `40843245`.
+ In `<o:LastAuthor>40843245</o:LastAuthor>`, the author who last modifies it is `40843245`.
+ In `<o:Revision>2</o:Revision>`, its revision number is 2.
+ In `<o:TotalTime>0</o:TotalTime>`, the last modifies spent 0 minutes (or less than 1 minute) on this file
+ In `<o:LastPrinted>2016-06-13T09:16:00Z</o:LastPrinted>`, it will not be printed after `2016-06-13 09:16:00` UTC Time Zone.
+ In `<o:Created>2016-12-13T04:53:00Z</o:Created>`, someone creates this file at `2016-12-13 04:53:00` UTC Time Zone.
+ In `<o:LastSaved>2016-12-13T04:53:00Z</o:LastSaved>`, this file is saved at `2016-12-13 04:53:00` UTC Time Zone.
+ In `<o:Pages>1</o:Pages>`, this file has one page.
+ In `<o:Words>70</o:Words>`, this file contains exactly 70 words.
+ In `<o:Characters>405</o:Characters>`, this file contains exactly 405 characters (excluding space).
+ In `<o:Company>NFU</o:Company>`, this file is create by orginization NFU. Simply said, someone creates this file with Microsoft Office Word where its Microsoft Office product is registered by NFU.
+ In `<o:Lines>3</o:Lines>`, Office Word estimates this file has three lines.
+ In `<o:Paragraphs>1</o:Paragraphs>`, Office Word estimates this file has one paragraph.
+ In `<o:CharactersWithSpaces>474</o:CharactersWithSpaces>` Office Word estimates this file has 474 characters (including space).
+ In `<o:Version>15</o:Version>`, this file is created with Microsoft Office 2015. Here the version number 15 suggests version 2015.

#### about `wp` namespace
##### elements in `wp` namespace
| element in xml tag | stands for (represented as tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `<wp:inline>` | | inline | configure it (the tag that contains `<wp:inline>`) is inline.</br>For example, a `.xml` file that contains ``<w:drawing><wp:inline> <!-- element omitted --> </wp:inline></w:drawing>``, `<wp:inline>` element signifies that the drawing object is treated as if it were a character within the text flow. | see following example. | | 
| `<wp:extent>` | | | specifically deals with the size of a drawing object. | | |
| `<wp:effectExtent>` | | |  specifies the additional extent that should be added to each edge (top, bottom, left, right) of a drawing object to account for any visual effects applied to it. | | |
| `<wp:docPr/>` | | *d*rawing *o*bje*ct *pr*operties | | |  
| `<wp:cNvGraphicFramePr>` | | *C*ommon *N*on-*V*isual *Graphic* *Frame* *Pr*operties | holds non-visual properties for a graphic frame within a drawing object in WordprocessingML. | | |

##### attribute about `wp` namespace
###### attribute in `<wp:inline>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `wp:cx` | | | specifies the width of the drawing object | Its unit is EMU. | |
| `wp:cy` | | | specifies the height of the drawing object | Its unit is EMU. | |
| `wp:distT` | | | specifies the distance from top of the drawing object | Its unit is EMU. | |
| `wp:distB` | | | specifies the distance from bottom of the drawing object | Its unit is EMU. | |
| `wp:distL` | | | specifies the distance from left of the drawing object | Its unit is EMU. | |
| `wp:distR` | | | specifies the distance from right of the drawing object | Its unit is EMU. | |
| `wp:editId` | | | specifies the edit id | | |
| `wp:anchorId ` | | | specifies the anchor id | | |
| `wp:simplePos` | | | determines it uses simple position schema | | |
| `wp:relativeFrom ` | | | determines what the positioning of the object is relative to (e.g., page, margin). | | |

###### attribute in `<wp:extent>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `wp:cx` | | | sets extent length | its unit is EMU | |
| `wp:cy` | | | sets extent height | its unit is EMU | |

###### attribute in `<wp:effectExtent>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `wp:l` | | | specifies additional length in EMUs to be added to the left edge of the drawing object to accommodate effects | its unit is EMU | |
| `wp:t` | | | specifies additional length in EMUs to be added to the top edge of the drawing object to accommodate effects | its unit is EMU | |
| `wp:r` | | | specifies additional length in EMUs to be added to the right edge of the drawing object to accommodate effects | its unit is EMU | |
| `wp:b` | | | specifies additional length in EMUs to be added to the bottom edge of the drawing object to accommodate effects | its unit is EMU | |

###### attribute in `<wp:docPr>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `id` | | | the id of the drawing object | | |
| `name` | | | the name of the drawing object | | |
| `descr` | | *descr*iption | the description of the drawing object | | |

###### attribute in `<wp:cNvGraphicFramePr>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `wp:id` | | | speficies the unique identifier | | |

##### examples
###### example 1.1 -- an drawing object with description
```
<wp:docPr id="1" name="" descr="Midori"/>
```

In above example, we can know that

+ an drawing object with id `1`, no name, and description `Midori`.

###### example 2.1 -- extent
```
<wp:anchor relativeHeight="10" allowOverlap="true">
  </wp:anchor>
  <wp:extent cx="1828800" cy="1828800"/>
</wp:anchor>
```

In this example, we can know that

+ In `<wp:extent cx="1828800" cy="1828800"/>`, it indicates that the drawing object has a width and height of 1,828,800 EMUs.

#### about `w` namespace
##### elements in `w` namespace
| element in xml tag | stands for (represented as tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| | | | | | |
| `<w:settings>` | | settings | it serves as a container for a wide range of document-level settings and properties that control how the Word document behaves and is displayed. | it usually resides in `~/word/setting.xml` file under a Office Word file. | |
| `<w:webSettings>` | | web settings | is the root element for web-related settings in the Word document. | it usually resides in `~/word/setting.xml` file under a Office Word file. | |
| `<w:zoom>` | | zoom | specifies the display zoom level for the document when it is opened in Microsoft Word. | same as above| |
| `<w:characterSpacingControl>` | | character spacing controlls | specifies how to adjust the spacing between characters. | |
| `<w:compat/>` | | compatibility | it is a container element that holds various compatibility settings designed to ensure the document is displayed and behaves as expected across different versions of Microsoft Word. | | |
| | | | | | |
| `<w:rsids>` | | *r*evision *s*ave *id*entifier*s* | it is a container of revision save identifiers element (`<w:rsid>`, `<w:rsidRoot>`) | | |
| `<w:rsidRoot>` | | *r*evision *s*ave *id*entifiers baseline | establishes a revision save identifiers baseline for current editing session or the most recent save operation that affected the main content of the document. | | |
| `<w:rsid>` | | *r*evi*s*ion save | establishes a revision save identifier. | | |
| | | | | | |
| `<w:wordDocument>` | `<html>` | root node | the root node of a Microsoft Word file. | | |
| `<w:document>` | `<html>` | root node | the root node of **`~/word/document.xml`** file under a Microsoft Word file. | | |
| | | | | | |
| `<w:background>` |  | background | deals with background settings. | | |
| `<w:drawing>` |  | drawing | defines a drawing. | | |
| `<w:ignoreSubtree>` | | ignore a specific subtree | it instructs the Word processor to ignore a specific subtree of the XML document (according to the value of `w:val` attribute) during processing. | | | 
| `<w:body>` | `<body>` | body | the main part of file in native xml (and native html5) | | |
| `<w:lang>` | `<lang>` | language | the language for characters | lang stands for *lang*uage | |
| `<w:charset>` | `<charset>` in native html5 | charset | configure charset of this font | | |
| `<w:family>` | | family | configure family of this font | | |
| `<w:pitch>` | | character's pitch | configure pitch of characters that uses this font. | | | 
| `<w:defaultFont>` | | configure the default font | | |
| `<w:font>` | font in native css | define a font | | |
| `<w:sig>` | | digital signature | encapsulate the digital signature of this font. | | | 
| `<w:panose1>` | | panose | configure the panose (with highest priority) | The lower number is it, the higher priority it has. | |
| | | | | | |
| `<w:name/>` | | | provides a more user-friendly name (for the name defined in parent tag) | | |
| | | | | | |
| `<w:basedOn/>` | | | inherits a style | | |
| | | | | | |
| `<w:next/>` | | | specifies the style to be automatically applied to the next paragraph after a paragraph formatted with the current style. | | |
| | | | | | |
| `<w:altName>` | `alt` attribute in `<img>` tag in native html5 | *alt*ernative | use the alternative (according to the value specified in `w:val` attribute) **when** an element (such as an image) or things that used in an element (such as font) **can not be used or worked correctly**. | | |
| `<w:noProof/>` | | no proofing tool used | no spelling check and grammer check inside this tag. | | |
| | | | | | |
| `<w:framePr>` | | frame *pr(operty | configure property of frame | | |
| | | | | | | |
| `<w:p>` | `<p>` | *p*aragraph | defines a paragraph | notice that if an end-user only inputs an whitespace in .docx file, it will have `<w:p>` tag, the article `docx格式文档详解：xml解析并用html还原`[^4] says this situation. | 
| `<w:pStyle>` | | *p*aragraph style | applies style (according to value of `w:val` attribute) to paragraph (that is inside `<w:p>` tag) | the style to apply is defined in `~/word/style.xml` file | |
| `<w:pPr>` | | *p*aragraph *pr*operty | property of a paragraph (that is inside `<w:p>` tag) in Microsoft Word file | | |
| | | | | | | | 
| `<w:r>` | | *r*un | defines a run in Word | | |
| `<w:rPr>` | | *r*un *pr*operty | configure property of a run (that is inside `<w:r>` tag) | | |
| `<w:rFonts>`| | *r*un fonts | configure fonts of a run (that is inside `<w:rPr>` tag) | | |
| | | | | | | | 
| `<w:b/>` | `<b>` and `<b/>` in native html5 | bold | determines whether the non-complex script text is bold | | |
| `<w:bCs/>` | `<b>` and `<b/>` in native html5 | bold | determines whether the complex script text is bold | | |
| `<w:i/>` | | italic | determines whether the non-complex script text is italic. | | |
| `<w:iCs/>` | | italic | determines whether the complex script text is italic. | | |
| `<w:t/>` | | text | defines the text | | |
| `<w:bidi/>` | | text | defines the bidirectional text | | |
| | | | | | |
| `<w:rPrDefault>` | | | defines the default formatting properties for all text runs within the document. | | |
| `<w:pPrDefault/>` | | | defines the default formatting properties for all paragraphs in the document. | | |
| `<w:latentStyles>` | | | servers as a container for defining the latent styles (i.e. current unused styles). | | |
| | | | | | |
| `<w:ind>` | | paragraph *ind*entation | configure the indentation for this paragraph. | | |
| `<w:adjusLeftind>` | | adjust left *ind*entation | configure the left indentation will be adjusted due to different window size. | | |
| `<w:adjusRightind>` | | adjust right *ind*entation | configure the right indentation will be adjusted due to different window size. | | |
| | | | | | | | 
| `<w:jc>` | | *j*ustifi*c*ation | settings about justification (alignment) of the paragraph | | |
| `<w:spacing>` | spacing | settings about spacing between paragraphs | | |
| | | | | | | | 
| `<w:autoSpaceDE>` | | | controls whether Word should automatically adjust the spacing between Asian characters and Latin text (like English) within a paragraph. | | |
| `<w:autoSpaceDN>` | | | controls whether Word should automatically adjust the spacing between Asian characters and adjacent numbers (0-9) within a paragraph. | | |
| | | | | | | | 
| `<w:bar>` | | | insert a vertical line | | | | 
| | | | | | | | 
| `<w:footnotes>` | | footnotes | acts like a container containing footnotes | | | | 
| `<w:footnote>` | | footnote | defines a footnote | | | |
| `<w:footnotePr>` | | footnote *pr*operty | defines properties of the footnote | | | |
| `<w:footnoteRef>` | | footnote *ref*erence | references of the footnote | | | |
| | | | | | | |
| `<w:endnotes>` | | endnotes | acts like a container that containing endnotes | | | | 
| `<w:endnote>` | | endnote | defines a endnotes | | | |
| `<w:endnotePr>` | | endnote *pr*operty | defines properties of the endnote | | | |
| `<w:endnoteRef/>` | | endnote *ref*erence | references of the endnote | | | |
| | | | | | | | 
| `<w:hdr>` | | *h*ea*d*e*r* | configures the header | | | | 
| `<w:headerReference>` | | | indicates that the parent element refers the header with specific type. | | | | 
| | | | | | | | 
| `<w:ftr>` | | *f*oo*t*e*r* | configure the footer | | | | 
| `<w:footerReference>` | | | indicates that the parent element refers the footer with specific type. | | | | 
| | | | | | | |
| `<w:comments>` | | | acts like a container containing comments | | | | 
| `<w:comment>` | | | defines a comment | | | |
| `<w:commentPr>` | | | defines properties of the comment | | | |
| | | | | | | |
| `<w:titlePg>` | | title *p*a*g*e | defines a title page. | | | 
| | | | | | | | 
| `<w:sz>` | | *s*i*z*e for non-Complex script | defines a font size for standard characters (that is inside `<w:rPr>` tag) | | |
| `<w:szCs>` | | *s*i*z*e for *C*omplex *s*cript | defines a font size for complex script characters (that is inside `<w:rPr>` tag) | | |
| | | | | | | | 
| `<w:tbl>` | `<table>` | *t*a*bl*e | a table in Microsoft Word file | | |
| `<w:tblPr>` | | *t*a*bl*e *pr*operty | configure property (such as style and appearance) of a table (that is inside `<w:tbl>` tag) in Microsoft Word file | | |
| `<w:tblGrid>` | `<tr>` (first occurence) | *t*a*bl*e grid | defines a grid (header) of a table in Microsoft Word file | you can think of a grid like a header row ( consists of lots of columns ) in table | |
| `<w:gridCol>` | `<th>` | table grid column | defines a cell in a grid of a table in Microsoft Word file | | it must be inside `<w:tblGrid>` tag. Otherwise, the Word file is corrupted. |
| `<w:tr>`| `<tr>` | table row | a row of a table | t stands for *t*able, r stands *r*ow | |
| `<w:tc>` | `<td>` | table cell | an cell of a table | c stands for *c*ell | |
| `<w:tcW>` | | table cell width | determines the width of the cell of a table | W stands for *w*idth | |
| `<w:tcPr>` | | table cell property | configure property of a table cell (that is inside `<w:tc>` tag) | including width and grid span | |
| `<w:tblStyle>` | | table style | applies style (according to value of `w:val` attribute) to paragraph (that is inside `<w:tbl>` tag) | the style to apply is defined in `~/word/style.xml` file | |
| `<w:tblBorders>` | | table borders | specifies the table borders. | | |
| | | | | | | | 
| `<w:instrText>` | | *instr*uction text | it defines an instruction text for a field | | |
| `<w:fldChar>` | | *f*ie*ld* *char*acter | it defines a field character. | | | 
| | | | | | | | 
| `<w:fldSimple>` | | simple *f*ie*ld* | defines a simple field and acts like a container that contains its' setting (inside this tag). | | | 
| | | | | | | | 
| `<w:sectPr>` | | sect property | configure property of a sect | sect stands for section | |
| `<w:pgSz>` | | page size | configures a page size (that is inside `<w:sectPr>` tag) | pg stands for *p*a*g*e | |
| `<w:pgMar>` | | page margin | configures a page margin (that is inside `<w:sectPr>` tag) | Mar stands for *Mar*gin | |
| `<w:col>` | | columns in section | add columns in section (that is inside `<w:sectPr>` tag) | | |
| `<w:docGrid>` | | document grid | add document grid (that is inside `<w:sectPr>` tag) | | |
| | | | | | | | 
| `<w:tabs>` | | | acts like a container of tab stops (`<w:tab>`) | you may see one or more `<w:tab>` tag inside `<w:tabs>` tag. | | 
| `<w:defaultTabStop>` | | tab | define property of the default tab stop by assign the value to its attributes. | | | 
| `<w:tab>` | | tab | define property of a tab stop by assign the value to its attributes. | | | 
| | | | | | | | 
| `<w:bookmarkStart>` | | bookmark start | defines a bookmark with start point | | One `<w:bookmarkStart>` tag must match one `<w:bookmarkEnd>` tag. Otherwise, the file is corrupted. | 
| `<w:bookmarkEnd>` | | bookmark end | defines a bookmark with end point to enclose a bookmark | | Same as above | 
| | | | | | | | 
| `<w:lists>` | | | acts like a container of a list (`<w:list>`) | | |
| `<w:numbering>` | | numbering | It acts as a container for numbering definitions, which are then referenced by paragraphs to apply specific list styles. | | |
| `<w:listDef>` | | list *def*inition | defines a list with specific id for style | | |
| `<w:lsid>` | | *l*ist *s*tyle *id*entifier | assign the value of `w:val` attribute to id of list style to determine which style will be used | the id is defined in `~/word/style.xml` | |
| `<w:lvl>` | | list *l*e*v*e*l* | defines a level of list | lvl stands for *l*e*v*e*l* | |
| `<w:plt>` | | *p*icture *l*ist *t*ype (exactly to say, list pattern type in modern version of Word) | it describes the complexity or structure of the list definition | | |   
| `<w:tmpl>` | | *t*e*mpl*ate | it configure the what template will be used | <ol><li>tmpl stands for *t*e*mpl*ate</li><li>It accords to value of `W:val` attribute.</li><li>The template that will be used must be prefined (usually is predefined in `~/word/style.xml` or `~/word/template.xml`</li></ol> | | 
| `<w:start>` | | start | configure starting value for the numbering sequence at this list level | | It's only relevant when the <w:numFmt> (number format) for this level is set to a numbering style (like decimal, upperRoman, lowerLetter, etc.). |
| `<w:numFmt>` | | number *f*or*m*a*t*ting | determines whether this level uses numbers or bullets, and the specific style  | | |
| `<w:bullet>` | | bullet formatting | same above | | |
| `<w:numPr>` | | number *property | configure the property if it uses number formatting.  | | |
| `<w:numId>` | | numbering id | specifies the numbering id to link number formatting given the value of `w:val` attribute.  | | |
| `<w:suff>` | | suffix | specifies what character (if any) follows the number (e.g., a period, a hyphen, or a tab) | | |
| `<w:outlineLvl>` | | outline *l*e*v*e*l* | specifies the outline level which shall be associated with the current paragraph in the document. | | |
| `<w:lvlText>` | | *l*e*v*e*l* text | defines the numbering format using placeholders (e.g., "%1." for first-level numbers) | | |
| `<w:lvlJc>` | | *l*e*v*e*l* *j*ustifi*c*ation | configures the justification of this level | | | 
| `<w:nfc>` | | *N*umber *F*ormatting *C*ode | configures Number Formatting Code of this level | | | 
| | | | | | | |
| `<w:hyperlink>` | | hyperlink | defines a hyperlink | | |
| | | | | | | |
| `<w:bdr>` | `border` in css | *b*or*d*e*r* | configures properties of the border. | | |
| `<w:pBdr>` | | *p*aragraph *b*or*d*e*r* | configure paragraph border | | |
| `<w:between>` | | | border that appears between consecutive paragraphs | | |
| `<w:pgBorders>` | | *p*a*g*e borders | configures properties of the borders of page. | | |
| | | | | | | |
| `<w:top>` | | top | configures properties of top borders of some elements (according to this tag is inside what tag). | | |
| `<w:left>` | | left | configures properties of left borders of some elements (according to this tag is inside what tag). | | |
| `<w:bottom>` | | bottom | configures properties of bottom borders of some elements (according to this tag is inside what tag). | | |
| `<w:right>` | | right | configures properties of right borders of some elements (according to this tag is inside what tag). | | |
| `<w:insideH>` | | inside *H*orizontal | specifies internal horizontal border. i.e. specifies horizontal border between rows (within a paragraph or table etc). | | |
| `<w:insideV>` | | inside *V*ertical | specifies vertical border between columns within a table. | | |
| | | | | | | |
| `<w:displayBackgroundShape/>` | | | determines if the background shape is display or not | | | 
| `<w:themeFontLang/>`| | | specifies the language settings for the theme fonts used in a Microsoft Word document. | | | 
| `<w:clrSchemeMapping/>` | | | clear the settings of scheme mapping table, then configures the properties of scheme mapping table for document role. | | |
| | | | | | | | 
| `<w:shapeDefaults>` | | | acts like an container containing default properties for newly created drawing shapes within a Microsoft Word document. | It usually resides in `~/word/settings.xml` under a Word file. | |
| `<w:docDefaults>` | | | serves as a container for defining the default formatting properties for the entire document. | | |
| | | | | | | | 
| `<w:decimalSymbol/>` | | | explicitly specifies the decimal separator (by given value of `w:val` attribute) for numbers within the document. | | |
| `<w:listSeparator/>` | | | explicitly specifies the list separator (by given value of `w:val` attribute) for list within the document. | It is used when there are many items. | |
| | | | | | |
| `<w:style>` | | style | defines a style | it usually resides at `~/word/style.xml` file under a Word file. | |
| `<w:lsdException>` | | LSD exception | defines exceptions to the default behavior of LSD (Linked Style Definitions). | | |
| `<w:cnfStyle>` | | conflict styles | It's used to store information about how styles should be applied or resolved in situations where there might be conflicts or variations. | | |
| | | | | | |
| `<w:vertAlign/>` | | vertical alignment | specifies that which alignment the text within the current run should be formatted to | it usually resides at `~/word/style.xml` file under a Word file. | |
| `<w:hr>` | | | defines a horizontal rule | | |
| | | | | | |
| `<w:contextualSpacing>` | | | determine that Word can dynamically modify the line spacing in situations | `"true"` to modify, `"false"` to not modify. default value to `"true"` | |
| | | | | | |
| `<w:divId>`| | | speficies the div id | | | 
| `<w:separator/>`| | | defines a seperator (maybe section break) | | | 
| `<w:continuationSeparator/>`| | | defines that the continuation separator for footnotes.) | | | 
| | | | | | |
| `<w:keepLines>` | | | determines whether keep lines to make the paragraph must be on the same page. | | | 
| `<w:keepNext>` | | | specifies that the contents of this paragraph are at least partly rendered on the same page as the following paragraph whenever possible. | | | 
| | | | | | |
| <w:kinsoku> | | Kinsoku Shori (禁則處理) | specifies whether East Asian typography and line-breaking rules shall be applied to text in this paragraph to determine which characters can begin and end each line. | | This property only applies to Simplified Chinese, Traditional Chinese, and Japanese text in this paragraph. |
| `<w:minorIdents>` | | | detemines whether if this tag is present, Word will swap the left and right indent settings if the document or section is set to a right-to-left reading order. | | If this is omitted on a given paragraph, its value is determined by the setting previously set at any level of the style hierarchy (i.e. that previous setting remains unchanged). If this setting is never specified in the style hierarchy, then this property shall not be applied. |
| | | | | | |
| `<w:sdt>` | | *s*tructured *d*ocument *t*ag  | acts like a container for a specific piece content (e.g. TOC). | | |
| `<w:sdtContent>` | | *s*tructured *d*ocument *t*ag content |  acts like a container for the actual content that is displayed within a Structured Document Tag | | |
| `<w:sdtPr>` | | *s*tructured *d*ocument *t*ag *pr*operties | defines the properties of structured document tag (`<w:sdt>` tag). | About characterist of structured tag, see [here](https://github.com/40843245/Microsoft_Office/blob/main/Product/Word/terms/terms%20list.md#characteristics) | |
| `<w:sdtEndPr>` | | *s*tructured *d*ocument *t*ag end *pr*operties | specifies properties that are applied to the end delimiter of the content control in the document. | | |
| | | | | | |
| `<w:docPartObj>` | | *doc*ument part *obj*ect | defines an object for document part. The main advantage is to more easily embed it to a document and make it reusable (which is the core concept of OO design). | | |
| `<w:docPartGallery>` | | *doc*ument part gallery filter | specifies the document part gallery filter | | |
| `<w:docPartUnique/>` | | | ensures that only one instance of a selected building block from the gallery can exist within the scope of the content control. | | |
| | | | | | |

##### attribute about `w` namespace
###### attribute in `<w:style>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:type` | | | specifies what type of style that will apply to | | It is required. |
| `w:styleId` | | | specifies style name | | It is required. |
| `w:customStyle` | | | determines whether it is a custom style | | Its default value is `"false"` |
| `w:default` | | | determines whether that this style is the default style for its style type | | <ol><li>Its default value is `"false"` </li><li>There can be only one default style for each type.</li></ol> |
| `w:styleIdPrimary` | | | is used for linked styles (e.g., a character style linked to a paragraph style). It specifies the w:styleId of the primary style. | | |

> [!CAUTION]
> There can be only one default style for each type.

###### attribute in `<w:minorIdents>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | detemines whether if this tag is present, Word will swap the left and right indent settings if the document or section is set to a right-to-left reading order. | | |

###### attribute in `<w:kinsoku>`
> [!WARNING]
> This property only applies to Simplified Chinese, Traditional Chinese, and Japanese text in this paragraph.

| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | specifies whether East Asian typography and line-breaking rules shall be applied to text in this paragraph to determine which characters can begin and end each line. | | |

> [!IMPORTANT]
> What kind of characters are typically affected by kinsoku rules?
>
> + For starting characters: Small kana characters (like っ, ゃ), opening brackets/parentheses, punctuation marks.
> + For ending characters: Closing brackets/parentheses, certain punctuation marks.

###### attribute in `<w:keepLines>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | determines to keep lines or not | | It default value is `"true"` |

> [!IMPORTANT]
> **Why is `<w:keepLines>` useful?**
> + **Headings:** You usually want a heading to stay on the same page as the text that follows it.
> + **Short paragraphs or lists:** Keeping these together can improve readability and prevent awkward breaks.
> + **Tables and figures with accompanying text:** You might want to ensure that a caption or a short explanation remains on the same page as the object it describes.

###### attribute in `<w:keepNext>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | allows a page break to occur between the current paragraph and the following one if needed. | | It default value is `"true"` |

For more details, see [OOXML docs CH117.3.1.15](https://ooxml.info/docs/17/17.3/17.3.1/17.3.1.15/)

###### attribute in `<w:framePr>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:w` | | width | set width | | |
| `w:h` | | height | set height | | |
| `w:x` | | | horizontal position of the frame relative to its horizontal anchor (the page). | |
| `w:xAlign` | | | specifies the horizontal alignment of the frame relative to its horizontal anchor | |
| `w:yAlign` | | | specifies the vertical alignment of the frame relative to its vertical anchor | |
| `w:hRel` | | | specifies the horizontal positioning relative to the anchor | |
| `w:vRel` | | | specifies the vertical positioning relative to the anchor | |
| `w:hRule` | | height rule | specifies how the height of the frame should be determined. | | |
| `w:hSpace` | | horizontal spacing | sets the horizontal spacing around the frame, specifically to the left and right.  | | |
| `w:lSpace` | | left spacing | sets the left spacing around the frame.  | | |
| `w:wrap` | | wrap | determines how the surrounding text interacts with the frame | | |
| `w:vAnchor` | | vertical anchor | specifies the vertical anchor for the frame's positioning. | | |
| `w:hAnchor` | | horizontal anchor | specifies the horizontal anchor for the frame's positioning. | | |
| `w:wAnchor` | | wrapped anchor | specifies the horizontal reference point for the frame's sizing. | | |
| `w:anchorLock` | | | specifies that the frame shall always remain in the same logical position relative to the non-frame paragraphs which precede and follow it in this document. | See [anchorLock](https://ooxml.info/docs/17/17.3/17.3.1/17.3.1.11/#anchorlock-lock-frame-anchor-to-paragraph) for more information. | | |
| `w:dropCap` | | specifies that the current frame contains a drop cap to be located at the beginning of the next non-frame paragraph in the document. | | If this attribute is omitted, then this frame shall not be considered a drop cap frame. |
| `w:line` | | specifies the number of lines in the non-frame paragraph to which this text frame is anchored which should be used to calculate the drop cap’s height. | | If this attribute is omitted, then it should use the default value `"1"`. |

###### attribute in `<w:cnfStyle>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:evenHBand` | | Even Numbered *H*orizontal Band | specifies that the object has inherited the conditional properties applied to the even numbered horizontal bands of the parent object. | | |

###### attribute in `<w:background>`
[!WARNING]
> If the background specifies the use of a theme color via the themeColor attribute, this value is ignored.
>
> Thus, Applications are discouraged from specifying both the color and themeColor attributes on the same parent element.

[!WARNING]
> If neither the color nor themeColor attributes are present,
>
> the parent page shall be treated as though it has no background defined.

| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:themeColor` | | theme color | specifies the theme color. | | |
| `w:themeShade` | | theme shade | specifies the darkness of theme color. | | |
| `w:themeTint` | | theme tint | specifies the lightness of theme color. | | |
| `w:color` | | | specifies background color. | | |
| `w:fill` | | | specifies background color. | | |
| `w:fillThemeColor` | | | specifies background color of theme. | | |
| `w:fillShade` | | | specifies the darkness of background color of theme. | | |
| `w:fillTint` | | | specifies the lightness of background color of theme. | | |
| `w:backgroundType` | | | specifies the type of background. | | |

###### attribute in `<w:zoom>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:percentage` | | percentage | which zoom level should be when the document is displayed. | | must be a string contains positive number. |

###### attribute in `<w:characterSpacingControl>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | percentage | determines how to adjust characters between spaces. | | |

> [!IMPORTANT]
> The available value of `w:val` attribute in `<w:characterSpacingControl>` is defined in [Character-Level Whitespace Compression Settings](https://c-rex.net/samples/ooxml/e1/Part4/OOXML_P4_DOCX_ST_CharacterSpacing_topic_ID0E6AK2.html)

###### attribute in `<w:rsid>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | specifies a Guid as a revision save identifier. | | |

###### attribute in `<w:word>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:macrosPresent` | | macro to present or not | assign a value to determine it will use macro (written in VBA or VB).</br>If it is specified to "yes", it will use macro.</br>Otherwise, it will not use macro. | | |
| `w:embeddedObjPresent` | | embedded object to present or not | assign a value to determine whether the document contains embedded objects (like Excel spreadsheets or other OLE objects). | | |
| `w:ocxPresent` | | OCX controls to present or not | assign a value to determine whether the document will use OCX controls (i.e. ActiveX controls) | | |  

###### attribute in `<w:font>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:name` | | name | assign a value to give the name to this font. | | |

###### attribute in `<w:family>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | value | assign a value to determine which family will be used for those text that uses this font. | | |

###### attribute in `<w:charset>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | value | assign a value to determine which charset will be used for those text that uses this font. | | |

###### attribute in `<w:pitch>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | value | assign a value to determine which how many pitches will be used for those text that uses this font. | | |

###### attribute in `<w:bar>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | style of bar | | |

###### attribute in `<w:adjustLeftInd>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | adjust left indentation due to different window size. | | |

###### attribute in `<w:adjustRightInd>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | adjust right indentation due to different window size. | | |

###### attribute in `<w:ind>`
> [!CAUTION]
> I highly NOT recommend that specify BOTH `w:first-line` and `w:hanging` attribute.
>
> The Google Gemini says that
>
>> If both `w:first-line` and` w:hanging` are specified, `w:hanging` is usually ignored.

> [!CAUTION]
> Similarly, I highly NOT recommend that specify BOTH `w:first-line-chars` and `w:hanging-chars` attribute.
>
> The Google Gemini says that
>
>> If both `w:first-line-chars` and` w:hanging-chars` are specified, `w:hanging-chars` is usually ignored.

> [!NOTE]
> I list some common used attributes.
>
> For `<w:ind>` tag and its attributes, see the [DocumentFormat.OpenXml.Wordprocessing.Indentation class (MSDS API reference)](https://learn.microsoft.com/en-us/dotnet/api/documentformat.openxml.wordprocessing.indentation?view=openxml-3.0.1)

| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:left-chars` | | left indentation, characters unit | assign an positive value to specify left indentation of the paragraph, measured in character units. | it is measured with its unit -- default character | it is deprecated, but not obsolete. At Microsoft Office 2019, it can recongize this attribute |
| `w:left` | | left indentation | assign an positive value to specify left indentation of the paragraph, measured in twips.  | its unit is twips | same as above |
| `w:start-chars` | | start indentation, characters | assign an positive integer to specify left indentation of the paragraph, measured in character units. | it has meaning of `w:left-chars` attribute | However, it is implemented in later version of OOXML standard (ECMA-376, 2011), so Microsoft Word 2007 may not recognize this attribute. |
| `w:startChars` | | same as above | same as above | same as above | However, it is an old fashion. |
| `w:start` | | start indentation | assign an positive value to specify start indentation of the paragraph, measured in twips.  |  it has meaning of `w:left` attribute | same as above |
| `w:right-chars` | | right indentation, characters unit | assign an positive integer to specify right indentation of the paragraph, measured in character units. | it is measured with its unit -- default character | it is deprecated, but not obsolete. At Microsoft Office 2019, it can recongize this attribute |
| `w:right` | | right indentation | assign an positive value to specify right indentation of the paragraph, measured in twips.  | its unit is twips | same as above |
| `w:end-chars` | | end indentation, characters unit | assign an positive value to specify end indentation of the paragraph, measured in character units. | it has meaning of `w:right-chars` attribute | However, it is implemented in later version of OOXML standard (ECMA-376, 2011), so Microsoft Word 2007 may not recognize this attribute.</br>If it is not specified, it should use the default value `"0"`. |
| `w:endChars` | | | same above | same above | However, it is an old fashion of `w:end-chars`. |
| `w:end` | | end indentation | assign an positive value to specify end indentation of the paragraph, measured in twips.  |  it has meaning of `w:right` attribute | same as above |
| `w:hanging-chars` | | hanging indentation, characters unit | assign an positive integer to specify hanging indentation of the paragraph, measured in character units. | <ol><li>it is measured with its unit -- default character</li><li>For explanation about the term hang indentation, see `Appendix 4 -- terms`[^3]</li></ol>| It has higher preceedence than `w:hanging` attribute. |
| `w:hangingChars ` | | same above | same above | same above | However, it is an old fashion. |
| `w:hanging` | | hanging indentation | assign an positive value to specify hanging indentation of the paragraph, measured in twips.  | its unit is twips | |
| `w:first-line-chars` | | first-line indentation, characters unit | assign an value to specify first-line indentation of the paragraph, measured in twips.  | it is measured with its unit -- default character | <ol><li>It can be negative value, but when it is a negative value, there are some different effects.</br>See following cases.</br>Case 1:</br>When speficies a positive value, it indents the first line further to the right than the rest of the paragraph.</br>Case 2:</br>When specifics a negative value, it creates a `hanging indent` effect where the first line starts to the left of the subsequent lines.</li><li>It usually has higher preceedence of `w:first-line`. That is, if its value is speficied, it will ignore the value of `w:first-line` attribute.</li></ol>|
| `w:firstLineChars` | | same above | same above | | However, it is an old fashion. |
| `w:first-line` | | first-line indentation | assign an value to specify first-line indentation of the paragraph, measured in twips.  | its unit is twips |
same as above.</br>However, it has lower preceedence than `w:first-line-chars`. |
| `w:firstLine` | | same above | same above | | However, it is an old fashion. |
| `w:mirrorIndents` | | mirror indentation | the indentation should be mirrored.</br>Specifying to `"false"` indicates that the indentation will not be mirrored.</br>Otherwise, specifying to `"true"` indicates that it will be indented.</br>Default value is `"false"`. | | |

###### attribute in `<w:defaultFonts>`
Same as attribute in `<w:rFonts>`.

###### attribute in `<w:p>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:rsidR` | | *r*evision *s*ave *id*entifier for *r*un | specifies revision save id for run  | | |
| `w:rsidRDefault` | | *r*evision *s*ave *id*entifier for *default* *r*un | specifies revision save id for run  | | |
| `w:rsidSect` | | *r*evision *s*ave *id*entifier for *sect*ion | specifies revision save id for section | | |

##### attribute in `<w:r>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:rsidR` | | *r*evision *s*ave *id*entifier for *r*un | specifies revision save id for run  | | |
| `w:rsidRDefault` | | *r*evision *s*ave *id*entifier for *default* *r*un | specifies revision save id for run  | | |
| `w:rsidSect` | | *r*evision *s*ave *id*entifier for *sect*ion | specifies revision save id for section | | |

###### attribute in `<w:tab>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | determines alignment or behavior of the tab stop. | This attribute is required. | |
| `w:pos` | | | determines position of the tab stop. | This attribute is required. | |
| `w:leader` | | leader character | determines leader character that will fill the space before the tab stop.  | This attribute is optional. | |

###### attribute in `<w:defaultTabStop>`
Same as attribute in `<w:tab>`.

###### attribute in `<w:b/>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | determines whether the non-complex script text is bold. | | |

###### attribute in `<w:bCs/>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | determines whether the complex script text is bold. | | |

###### attribute in `<w:i/>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | determines whether the non-complex script text is italic. | | |

###### attribute in `<w:iCs/>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | determines whether the complex script text is italic. | | |

###### attribute in `<w:sz>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | `value` in native html5 | assign the value to determine default font size for **non-complex script characters** (that is inside `<w:pPr>` tag) | its unit is half-point. | |

###### attribute in `<w:szCs>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | `value` in native html5 | assign the value to determine default font size for **complex script characters** (that is inside `<w:pPr>` tag) | its unit is half-point. | |

###### attribute in `<w:pgSz>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:w` | `width` in css | assign the value to determine width of page size (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| `w:h` | `height` in css | assign the value to determine height of page size (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |

###### attribute in `<w:pgMar>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:top` | `margin-top` in css | margin-top |assign the value to determine top of page margin (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| `w:right` | `margin-right` in css | margin-right | assign the value to determine right of page margin (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| `w:bottom` | `margin-bottom` in css | margin-bottom | assign the value to determine bottom of page margin (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| `w:left` | `margin-left` in css | margin-left | assign the value to determine left of page margin (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| `w:header` | | header | assign the value to determine the distance from the top edge to the header (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| `w:footer` | | footer | assign the value to determine the distance from the bottom edge to the footer (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| `w:gutter` | | footer | assign the value to determine gutter margin (for binding) | its unit is twips (twentieths of a point). | |

###### attribute in `<w:cols>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:space` | | space | assign an value to determine the space between columns in section (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |

###### attribute in `<w:spacing/>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:after`| | | specifiies how many twips for spacing after the paragraph to  | its unit is twips (twentieths of a point). | |
| `w:line`| | |  specifiies how many twips for the line spacing to  | its unit is twips (twentieths of a point). | |
| `w:lineRule`| | | specifiies the line rule. | | |

###### attribute in `<w:instrText>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `xml:space` | | | specifies how whitespace should be handled within the text content of the `<w:instrText>` element. | | |

###### attribute in `<w:fldChar>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:fldCharType` | | | specifies how whitespace should be handled within the text content of the `<w:instrText>` element. | | |

###### attribute in `<w:fldSimple>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:instrText` | | | specifies field instruction. | Recall about field instruction (i.e. content in `<w:instrText>` tag), they have same concepts.</br> For more details, see my notes -- [syntax of field instruction in `<w:instrText>` tag section](https://github.com/40843245/OOXML/blob/main/Word/structure/CH1%20--%20syntax.md#syntax-of-field-instruction-in-winstrtext-tag)| |

###### attribute in `<w:footnote>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:id` | | | A positive integer that uniquely identifies this specific footnote within the footnotes part of the document. | These IDs are typically sequential. | |
| `w:type` | | | specifies the type of the footnote. | | |

###### attribute in `<w:footerReference>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `r:id` | | | specifies the id that links to the footer. | It usually resides in `~/word/_rels/document.xml.rels` file under a Word file. | |
| `w:type` | | | specifies the type of the footer that the parent element refers, determining that the footer will be applied to. | | |

###### attribute in `<w:hyperlink>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `r:id` | | | defines a relationship | | |
| `w:history` | | | indicates whether the hyperlink has been visited. | | |

###### attribute in `<w:docGrid>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:linePitch` | | vertical spacing | assign an value to determine the vertical spacing between grid lines in section (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| `w:charSpace` | | horizontal spacing | assign an value to determine horizontal spacing between grid lines in section (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| `w:type` | | type of document grid | assign an value to determine the type of document grid will be used in section (that is inside `<w:sectPr>` tag) | See `Appendix 2`[^2] for more information | |
| `w:lineGrid` | | number of line per grid | assign an value to determine number of line per grid in section (that is inside `<w:sectPr>` tag) | | its value must be positive number. |

###### attribute in `<w:tbW>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:w` | | width | assign an value to determine the width of the cell (that is inside `<w:tc>` tag) | NOTES that its unit is not necessary twips (its unit is according to value of `w:type` attribute. See next record | |
| `w:type` | | type | assign an value to determine its unit | | |

###### attribute in `<w:pStyle>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | `value` in native html5 | assign an Guid as value that determines what style of 7the paragraph (that is inside `<w:p>` tag) will apply to | | |

###### attribute in `<w:tblStyle>`
Way to parsing it is similar to parsing `<w:pStyle>`.

| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | `value` in native html5 | assign an Guid as value that determines what style of the table (that is inside `<w:tbl>` tag) will apply to | | |

###### attribute in `<w:lsid>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | `value` in native html5 | assign an Guid as value that determines what style of the list (that is inside `<w:listDef>` tag) will apply to | | |

###### attribute in `<w:bookmarkStart>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:id` | `id` in native html5 | id of start point of bookmark | assign the id of start point of bookmark that in the tag | | |
| `w:name` | `name` in native html5 | name of start point of bookmark | assign the name of start point of bookmark that in the tag | | |

###### attribute in `<w:bookmarkEnd>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:id` | `id` in native html5 | id of end point of bookmark | assign the id of end point of bookmark that in the tag | | | 

###### attribute in `<w:footnote>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:id` | `id` in native html5 | id of footnote | assign the id of the footnote | A value of `-1` is a convention used to identify the footnote separator. | | 
| `w:type` | | | specifies the type of footnote. | | |
| `w:numFmt` | | | specifies the number formatting of footnote. | | |
| `w:restart` | | | determines whether footnote numbering should restart at the beginning of a section. | | |

###### attribute in `<w:listDef>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:listDefId` | | list definition id | specify the unique id when defines a list to determine which style will be used. | | |

###### attribute in `<w:plt>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | assign the Guid as value to determine which style will be applied to for the list pattern type | | |

###### attribute in `<w:tmpl>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | assign the Guid as value to determine which template will be applied to for the list pattern type | | |

###### attribute in `<w:numId>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | the value determines which numbering formatting will be linked. | | |

###### attribute in `<w:lvl>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:ilvl` | | | specifies indentation of this level | | it must be a positive integer |

###### attribute in `<w:start>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | assign the positive integer as value to determine which the first item will be numbered to | the first item will use number or letter or bullet accords to value of `w:val` attribute in `<w:numFmt>` | it must be a positive integer |

###### attribute in `<w:lvlText>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | assign the string as value to specify the format for this level | | |

###### attribute in `<w:outlineLvl>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | specifies the outline level which shall be associated with the current paragraph in the document. | | |

###### attribute in `<w:lvlJc>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | assign the string as value to determine the alignment for this level | | |

###### attribute in `<w:bdr>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | `style` attribute in tag in native html5 | style | specifies the style of the border. | It is required. | | 
| `w:sz` | | size | specifies thickness or size of the border line | It is required. | | 
| `wx:bdrwidth` | `border-width` in css | *b*or*d*e*r* width | specifies border width. | Observe name of namespace -- `wx`, we can know its used in Word 2003-specific extension.</br>So this tag is available on Word that can the extension -- Word 2003-specific extension.</br> Use alternative `w:sz` instead. | | 
| `w:space` | | space | specifies spacing of border. | It is required. | | 
| `w:color` | color in css | color | specifies color of the border. | It is required. | |
| `w:themeColor` | | theme color | specifies theme color of the border. | It is optional.</br>There are default value. | |
| `w:themeTint` | | theme tint | specifies theme tint of the border. | It is optional.</br>There are default value. | |
| `w:themeShade` | | theme shade | specifies theme shade of the border. | It is optional.</br>There are default value. | |
| `w:frame` | | frame | determines the border should have frame effect. | It is optional.</br>Default value is `"false"`. | |
| `w:shadow` | | shadow | determines the border should have shadow effect. | It is optional.</br>Default value is `"false"`. | |

> [!NOTE]
> For introduction of frame effect, see [frame effect.md](https://github.com/40843245/CSS/blob/main/terms/frame%20effect.md)

> [!NOTE]
> For introduction of shadow effect, see [shadow effect.md](https://github.com/40843245/CSS/blob/main/terms/shadow%20effect.md)

###### attribute in `<w:pgBorders>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:display` | | display | specifies on which pages within the section the page border should be displayed. | It is optional | | 
| `w:offsetFrom` | | offeset from | determines how the page border's position is calculated relative to the page. | It is optional | |  
| `w:zOrder` | | z order | whether the page border should be rendered in front of or behind the document content. | | |

###### attribute in `<w:displayBackgroundShape>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | determines to display the background shape or not | | |

###### attribute in `<w:themeFontLang>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | specifies a language code to determines which language will be used, for complex script language, when the theme fonts are applied. | | |
| `w:bidi` | | | specifies a language code to determines which language will be used, for bi-directional language (such as Arabic or Hebrew) , when the theme fonts are applied. | | |

###### attribute in `<w:clrSchemeMapping>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:bg1` | | background color 1 | specifics background color 1 in scheme mapping table. | | | 
| `w:bg2` | | background color 2 | specifics background color 2  in scheme mapping table. | | | 
| `w:t1` | | text color 1 | specifics text color 1 in scheme mapping table. | | | 
| `w:t2` | | text color 2 | specifics text color 2 in scheme mapping table. | | | 
| `w:accent1` | | accent color 1 | specifics accent color 1 in scheme mapping table. | | | 
| `w:accent2` | | accent color 2 | specifics accent color 2 in scheme mapping table. | | | 
| `w:accent3` | | accent color 3 | specifics accent color 3 in scheme mapping table. | | | 
| `w:accent4` | | accent color 4 | specifics accent color 4 in scheme mapping table. | | | 
| `w:accent5` | | accent color 5 | specifics accent color 5 in scheme mapping table. | | | 
| `w:accent6` | | accent color 6 | specifics accent color 6 in scheme mapping table. | | | 
| `w:hyperlink` | | hyperlink | specifics hyperlink in scheme mapping table. | | | 
| `w:followedHyperlink` | | followedHyperlink  | specifics followed hyperlink in scheme mapping table. | | | 

For more informations and details, see [DocumentFormat.OpenXml.Wordprocessing.ColorSchemeMapping Class (MSDS API reference)](https://learn.microsoft.com/en-us/dotnet/api/documentformat.openxml.wordprocessing.colorschememapping?view=openxml-3.0.1)

###### attribute in `<w:latentStyles>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:default` | | | determined whether latent styles are enabled by default for the document. | | |
| `w:count` | | | an integer indicating the total number of latent styles defined within this element. | | |
| `w:defLockedState` | | | specifies the default locked state for new latent styles. | | |
| `w:defUIPriority` | | | specifies the default UI priority for new latent styles. | The higher value of ui priority is, the less preceedence it has so that styles might be displayed less prominently. | |
| `w:defSemiHidden` | | | specifies the default semi-hidden state for new latent styles. | | |
| `w:defUnhideWhenUsed` | | | specifies the default `unhide when used` state. | | |
| `w:defQFormat` | | | specifies the default quick format state for new latent styles. | | |

###### attribute in `<w:lsdException>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:name` | | | defines the exception to default LSD as `Normal` style | | |
| `w:semiHidden` | | | determines whether the style is hidden from the user interface under normal circumstances. | | |
| `w:uiPriority` | | | of the style in the user interface (e.g., in the Styles pane). | Concept similar to the concept mentioned at cell whose row is `w:defUIPriority` and column is `note`. | |
| `w:unhideWhenUsed` | | | specifies whether the style should become visible in the UI if it's used in the document, even if it was initially semi-hidden. | Concept similar to the concept mentioned at cell whose row is `w:defUnhideWhenUsed` and column is `note`. | | 
| `w:qFormat` | | | determines whether the style appears in the Quick Styles gallery. | Concept similar to the concept mentioned at cell whose row is `w:defQFormat` and column is `note`. | |

###### attribute in `<w:cnfStyle>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | might indicate that some form of conflict resolution or style application rule is active. | | |
| `w:firstColumn` | | | apply the style to first column | | |
| `w:lastColumn` | | | apply the style to last column | | |
| `w:firstRow` | | | apply the style to first row | | |
| `w:lastRow` | | | apply the style to last row | | |
| `w:firstRowFirstColumn` | | | apply the style to first row and first row | | |
| `w:firstRowLastColumn` | | | apply the style to first row and last column | | |
| `w:lastRowFirstColumn` | | | apply the style to last row and first column | | |
| `w:lastRowLastColumn` | | | apply the style to last row and last column | | |
| `w:italic` | | | the applied style is italic | | |
| `w:bold` | | | the applied style is bold | | |
| `w:underline` | | | the applied style is underlined | | |
| `w:color` | | | color of applied style | | |
| `w:oddHBand` | | | odd numbered horizontal bands of applied style | | |
| `w:oddVBand` | | | odd numbered vertical bands of applied style | | |
| `w:evenVBand` | | | even numbered vertical bands of applied style | | |

###### attribute in `<w:hr>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | specifies the line style of the horizontal rule | | |
| `w:sz` | | *s*i*z*e | height or thickness of the horizontal rule | | Its unit is half-point. |
| `w:space` | | | vertical spacing above and below the horizontal rule | | Its unit is half-point. |

##### examples and explanations
###### example 1.1 -- fonts
```
<w:fonts>
   <w:defaultFonts w:ascii="Times New Roman" w:fareast="新細明體" w:h-ansi="Times New Roman" w:cs="Times New Roman"/>
   <w:font w:name="Times New Roman">
      <w:panose-1 w:val="02020603050405020304"/>
      <w:charset w:val="00"/>
      <w:family w:val="Roman"/>
      <w:pitch w:val="variable"/>
      <w:sig w:usb-0="E0002EFF" w:usb-1="C000785B" w:usb-2="00000009" w:usb-3="00000000" w:csb-0="000001FF" w:csb-1="00000000"/>
   </w:font>
</w:fonts>
```

In above example, we can know that

+ In `<w:fonts>`, it configures properties of a collection of fonts.
+ In `<w:defaultFonts w:ascii="Times New Roman" w:fareast="新細明體" w:h-ansi="Times New Roman" w:cs="Times New Roman"/>`, it configure the default font.</br>It is `Times New Roman` when thoese text that uses default font is encoded with ascii encoding.</br>It is `新細明體` for thoese fareast-text that uses default font.</br>It is `Times New Roman` when thoese text that uses default font is encoded with high Ansi encoding.</br>It is `Times New Roman` for those complex script text that uses default font.
+ In `<w:font w:name="Times New Roman">`, it gives name of the font as `Times New Roman`, which indicates the text whose font is `Times New Roman` have these properties (inside `<w:font w:name="Times New Roman">` tag).
+ In `<w:panose-1 w:val="02020603050405020304"/>` (inside `<w:font w:name="Times New Roman">` tag), it classifies the text by PANOSE system with id `02020603050405020304` (that will be used with highest priority)
+ In `<w:charset w:val="00"/>`, it configures charset id as `00`.
+ In `<w:family w:val="Roman"/>`, it configures family of font as `Roman`.
+ In `<w:pitch w:val="variable"/>`, it configures pitch as variable-pitch.
+ In `<w:sig w:usb-0="E0002EFF" w:usb-1="C000785B" w:usb-2="00000009" w:usb-3="00000000" w:csb-0="000001FF" w:csb-1="00000000"/>`, it configure the digital signature.</br>Its 0th USB identifier (with highest priority) is `E0002EFF`.</br>Its 1th USB identifier is `C000785B`.</br>Its 2th USB identifier is `00000000`.</br>Its 3th USB identifier is `00000000`.</br>Its 0th CSB identifier is `000001FF`.</br>Its 1th CSB identifier is `00000000`.

> [!NOTE]
> USB id stands for unique signature block identifier.
> CSB id stands for custom signature block identifier.

> [!IMPORTANT]
> PANOSE system will be used when the specific font is NOT found in the device, it is corrupted, or it can not work.

> [!IMPORTANT]
> the value of the `w:val` attribute is "02020603050405020304". Each pair of digits represents a specific aspect of the font:
> 1.  **Family**: 02 = Text and display
> 2.  **Serif style**: 02 = Cove
> 3.  **Weight**: 06 = Book
> 4.  **Proportion**: 03 = Even width
> 5.  **Contrast**: 05 = Medium
> 6.  **Stroke variation**: 04 = Gradual/transitional
> 7.  **Arm style**: 05 = Slanted
> 8.  **Letterform**: 02 = Normal/upright
> 9.  **Midline**: 03 = Continuous
> 10. **X-height**: 04 = Medium

###### example 2.1 -- run
```
<w:r>
  <w:rPr>
    <!-- ... -->
    <w:rFonts w:ascii="標楷體" w:eastAsia="標楷體" w:hAnsi="標楷體"/>
    <w:sz w:val="52"/>
    <w:szCs w:val="52"/>
    <!-- ... -->
  </w:rPr>
</w:r>
```

In this example, we can know that

1. In `<w:r>`, it defines a run.
2. In `<w:rPr>`, it configures the property of the run.
3. In `<w:rFonts w:ascii="標楷體" w:eastAsia="標楷體" w:hAnsi="標楷體"/>`,

it configure the default fonts of the run,

the default fonts are `標楷體`, `標楷體`, `標楷體` when it is decoded as ascii characters, East Asian characters, high Ansi characters respectively.

4. In `<w:sz w:val="52"/>`,

it also configure the default size is 52 half-points for **standard characters** (i.e. non-complex script characters) (like English, French, German etc).

> [!TIP]
> You can think it as setting the `style` attr as `"font-size:52"` in native html5.

5. In `<w:szCs w:val="52"/>`,

it also configure the default size is 52 for **complex script characters** (like Arabic, Hebrew, Devanagari etc).

> [APPRECIATION]
> Thanks to Google Gemini, it refers from Google Gemini's answer.

###### example 3.1 -- a table
```
<!-- other elements omitted -->

<w:tbl>
  <w:tblPr>
    <w:tblStyle w:val="TableGrid"/>
    <w:tblW w:w="5000" w:type="auto"/>
    <w:tblLook w:val="04A0"/>
  </w:tblPr>
  <w:tblGrid>
    <w:gridCol w:w="1892.5"/>
  </w:tblGrid>
  <w:tr>
    <w:tc>
      <w:tcPr>
        <w:tcW w:w="15140" w:type="dxa"/>
        <w:gridSpan w:val="9"/>
      </w:tcPr>
    </w:tc>
    <w:p>
      <w:pPr>
        <w:jc w:val="left"/>
      </w:pPr>
      <w:r>
        <w:rPr>
          <w:rFonts w:ascii="標楷體" w:hAnsi="標楷體" w:cs="標楷體" w:eastAsia="標楷體"/>
          <w:sz w:val="32"/>
          <w:szCs w:val="32"/>
          <w:b/>
        </w:rPr>
        <w:t>text 1</w:t>
      </w:r>
    </w:p>
  </w:tr>
</w:tbl>
```

In the above example, we can know that

+ In `<w:tbl>`, it adds a table.
+ In `<w:tblPr>`, it add some properties of the table.
+ In `<w:tblStyle w:val="TableGrid"/>`, the table uses predefined style named `TableGrid` which is defined in `~/word/style.xml`.
+ In `<w:tblW w:w="5000" w:type="auto"/>`, the table width is 5000 and the Word will automatically justify the width to fit the content in cells.
+ In `<w:tblLook w:val="04A0"/>`, the `<w:tblLook>` tag determines which table styles and formatting options should be applied to a table.</br>The value of `w:val` attribute acts like a bitmask then determines which table styles and formatting options.</br>Its value is `04A0` which is a hexadecimal number.</br>Converting `04A0` from hexadecimal number to binary number gets `0000 0100 1010 0000`.</br>Only 5th bit (counting from LST, zero-based), 7th bit and 10th bit are set to 1 (other bits is set to 0).</br>When 5th bit is set to 1, applies table formatting for first row.</br>When 7th bit is set to 1, applies table formatting for first column.</br>When 10th bit is set to 1, do not apply column banding.</br>Therefore, applies table formatting for first row and first column. Dont't apply column banding. For more details, see [table formatting option and styling](https://github.com/40843245/Microsoft_Office/blob/main/Product/General%20Product/elements/table/table%20formatting%20option%20and%20styling/element%20value%20in%20OOXML.md)
+ In `<w:tblGrid>`, it defines a header of the table.
+ In `<w:gridCol w:w="1892.5"/>`, it defines a column of the table and set its width as 1892.5 twips.
+ In `<w:tr>`, it defines a row of the table.
+ In `<w:tc>`, it defines a cell in the row.
+ In `<w:tcPr>`, it defines the cell property.
+ In `<w:tcW w:w="15140" w:type="dxa"/>`, it configures width of the cell is 15140 twips.
+ In `<w:gridSpan w:val="9"/>`, it configure the grid span of the cell is nine, which means that the cell is cross from nine columns. The nine columns of this row is merged into this one cell.
+ In `<w:p>`, it defines a paragraph.
+ In `<w:pPr>`, it defines properties of the paragraph.
+ In `<w:jc w:val="left"/>`, it configures the alignment of the paragraph as left. The paragraph is left-aligned.
+ In `<w:r>` (inside `<w:p>`), it defines a run in this paragraph..
+ In `<w:rPr>`, it defines properties of the run.
+ In `<w:rFonts w:ascii="標楷體" w:hAnsi="標楷體" w:cs="標楷體" w:eastAsia="標楷體"/>`, it configures the fonts of run.</br>It is `標楷體` when the text that uses the run is encoded with ascii encoding.</br>It is `標楷體` when the text that uses the run is encoded with high Ansi encoding. It is `標楷體` for those complex-script text that uses the run.</br>It is `標楷體` when the text that uses the run is eastern-asia text (東南亞文字).
+ In `<w:sz w:val="32"/>`, it configures the size for those non-complex script text that uses the run is 32 twips.
+ In `<w:szCs w:val="32"/>`, it configures the size for those complex script text that uses the run is 32 twips.
+ In `<w:b/>`, it configures the text that uses the run is bold.
+ In `<w:t>text 1</w:t>` (inside `<w:r>`), it adds a text with content`text 1` in the run which is used by the paragraph. 

###### example 3.2 -- table borderss
```
<w:tbl>
    <w:tblPr>
      <w:tblBorders>
        </w:top>
        </w:left>
        </w:bottom>
        </w:right>
        <w:insideH w:val="single" w:sz="4" w:color="000000"/>
        <w:insideV/>
      </w:tblBorders>
    </w:tblPr>
</w:tbl>
```

In above example, we can know that

+ In `<w:tblBorders>`, it specifies the table borders.
+ In `</w:top>`, it specifies the top border of table borders (defined in `<w:tblBorders>`). However, it is empty, meaning that it uses default settings.
+ In `</w:left>`, it specifies the left border of table borders (defined in `<w:tblBorders>`). However, it is empty, meaning that it uses default settings.
+ In `</w:bottom>`, it specifies the bottom border of table borders (defined in `<w:tblBorders>`). However, it is empty, meaning that it uses default settings.
+ In `</w:right>`, it specifies the right border of table borders (defined in `<w:tblBorders>`). However, it is empty, meaning that it uses default settings.
+ In `<w:insideH w:val="single" w:sz="4" w:color="000000"/>`, it specifies the horizontal border within the table. It sets the horizontal border to be single solid line.  And it sets the thickness of border to 4 in quarter points (which is equivalent to 1 point), meaning that horizontal border is a 1-point line). Additionally, the color of horizontal border is set to `000000` (in rgb hex value).
+ In <w:insideV/>, it specifies the vertical border within the table. However, it is empty, meaning that it uses default settings.

###### example 4.1 -- outline level
```
<w:pPr>
  <w:outlineLvl w:val="0" />
</w:pPr>
```
###### example 4.2 -- list
```
<w:lists>
   <w:listDef w:listDefId="0">
      <w:lsid w:val="FFFFFF7C"/>
      <w:plt w:val="SingleLevel"/>
      <w:tmpl w:val="CC904CB8"/>
      <w:lvl w:ilvl="0">
         <w:start w:val="1"/>
         <w:lvlText w:val="%1."/>
         <w:lvlJc w:val="left"/>
         <w:pPr>
            <w:tabs>
               <w:tab w:val="list" w:pos="2281"/>
            </w:tabs>
            <w:ind w:left-chars="1000" w:left="2281" w:hanging-chars="200" w:hanging="360"/>
         </w:pPr>
      </w:lvl>
   </w:listDef>
</w:lists>
```

In above example, we can know that

+ In `<w:lists>`, it acts as a container for the list definitions.
+ In `<w:listDef w:listDefId="0">`, it defines the definition of list</br>which id is 0.
+ In `<w:lsid w:val="FFFFFF7C"/>`, it specifies the list style identifier whose value is `FFFFFF7C`.
+ In `<w:plt w:val="SingleLevel"/>`, it specifies the list pattern type is `single`, which means this list has only one level.
+ In `<w:tmpl w:val="CC904CB8"/>`, it specifies the template identifier whose value is `CC904CB8`.
+ In `<w:lvl w:ilvl="0">`, it defines the properties for a specific level, whose indentation level is 0.
+ In `<w:start w:val="1"/>`, it speficies the start point is 1.</br>i.e. The placeholder of first item in this level will be marked as `1` (or its corresponding symbol according to number formatting).
+ In `<w:lvlText w:val="%1."/>`, it specifies the placeholder.</br>The placeholder of first item in this level will be marked as `%1` (or its corresponding symbol according to number formatting) instead of `1`.
+ In `<w:lvlJc w:val="left"/>`, the placeholder of items in this level item in this level are left-aligned.
+ In `<w:pPr>`, it defines properties of a paragraph.
+ In `<w:tabs>`, it acts a container of a tab stop.
+ In `<w:tab w:val="list" w:pos="2281"/>`, it defines a tab stop specifically for list indentation at the position "2281" twips (i.e. twentieths of a point).
+ In `<w:ind w:left-chars="1000" w:left="2281" w:hanging-chars="200" w:hanging="360"/>`, controls the indentation of the list item.</br>By this attribute `w:left="2281"`, left indentation of the paragraph takes 2281 twips in total.</br>By this attribute `w:left-chars="1000"`, left indentation of the paragraph takes 1000 characters unit in total.</br>By this attribute `w:hanging="360"`, hanging indentation of the paragraph takes 360 twips in total.</br>By this attribute `w:hanging-chars="200"`, hanging indentation of the paragraph takes 200 characters unit in total.</br>Watch out for preceedence of this attribute. See following note.

> [!NOTE]
> The `w:hanging` attributes usually takes precedence over than `w:hanging-chars`.
>
> Similarly, the `w:left` attributes usually takes precedence over than `w:left-chars`.

###### example 5.1 -- line border
```
<w:rPr>
   <!-- other tags omitted -->
   <w:rFonts w:fareast="標楷體" w:hint="fareast" />
   <w:bdr w:val="single" w:sz="4" wx:bdrwidth="10" w:space="0" w:color="auto" />
</w:rPr>
```

In above example, we can know that

+ In `<w:rFonts>`, it defines the font of the run.
+ In `w:fareast="標楷體"`, for those far east asian characters that uses the run, the font of run is `標楷體`.
+ In `w:hint="fareast"`, it provides a hint to the rendering engine about the character set of the text in this run, and it reinforces that the primary character set for this text is East Asian.
+ In `<w:bdr>`, it defines a border of the run.
+ In `w:val="single"`, set the border as single solid line.
+ In `w:sz="4"`, set border width to 4 twips.
+ In `wx:bdrwidth="10"`, for Word that uses Word XML schema extension (it coulde be happen on Word in older version that it can not parse the attribute `w:sz`), sets its border width to 10 twips. 
+ In `w:space="0"`, it sets the spacing (from the border to its inner element) to zero.
+ In `w:color="auto"`, the border color is determined by the XML preprocessor.

###### example 5.2 -- page border
```
<w:sectPr>
  <w:pgBorders w:display="notFirstPage" w:offsetFrom="text" w:zOrder="back">
    <w:top w:val="single" w:sz="8" w:space="24" w:color="0000FF"/>
    <w:left w:val="dashed" w:sz="12" w:space="18" w:color="FF0000"/>
    <w:bottom w:val="double" w:sz="6" w:space="24" w:color="008000"/>
    <w:right w:val="dotted" w:sz="10" w:space="18" w:color="800080"/>
  </w:pgBorders>
</w:sectPr>
```

In above example, we can know that

+ In `<w:sectPr>`, it defines properties of the section.
+ In `<w:pgBorders w:display="notFirstPage" w:offsetFrom="text" w:zOrder="back">`, <ol><li>`w:display="notFirstPage"` indicates all pages (except for first page) should be display the page border within the section.</li><li>`w:offsetFrom="text"` indicates the values of `w:space` attribute (inside this tag) will be measured from the text margins of the page.</li><li>`w:zOrder="back"` specifies that the page borders should be rendered behind the document content.</li></ol>

###### example 6.1 -- display background shape
```
<w:displayBackgroundShape w:val="true"/>
```

In above example, we can know that

+ In `<w:displayBackgroundShape w:val="true"/>`, it will display background shape when a user open a Word file with Microsoft Office Word.

###### example 6.2 -- default shape
```
<w:shapeDefaults>
    <o:shapedefaults v:ext="edit" spidmax="2050"/>
    <o:shapelayout v:ext="edit">
        <o:idmap v:ext="edit" data="1"/>
    </o:shapelayout>
</w:shapeDefaults>
```

In above example, we can know that

+ In `<w:shapeDefaults>`, it defines a container containing default shapes.
+ In `<o:shapedefaults v:ext="edit" spidmax="2050"/>`, it specifies that id of newly created shape must be less than or equal to 2050 (according from `spidmax="2050"`).</br>Additionally,it specifies that newly created shape is fully editable in Office app (according from `v:ext="edit"`).
+ In `<o:idmap v:ext="edit" data="1"/>`, it sets the current id of newly created shape to one. Thus, the next id of newly created shape will be set to two. And it is current newly created shape is fully editable.

###### example 7.1 -- theme font language
```
<w:themeFontLang w:val="zh-TW" w:bidi="ar-SA"/>
```

In above example, we can know that

+ In `w:val="zh-TW"`, when applying theme fonts to text that is marked as **Traditional Chinese (Taiwan)**, use language-specific rendering rules appropriate for `zh-TW`.
+ In `w:bidi="ar-SA"`, When applying theme fonts to text that is marked as **Arabic (Saudi Arabia)** (a right-to-left language), use language-specific rendering rules appropriate for `ar-SA`.

###### example 7.2 -- color scheme
```
<w:clrSchemeMapping w:bg1="light1" w:t1="dark1" w:bg2="light2" w:t2="dark2" w:accent1="accent1" w:accent2="accent2" w:accent3="accent3" w:accent4="accent4" w:accent5="accent5" w:accent6="accent6" w:hyperlink="hyperlink" w:followedHyperlink="followedHyperlink"/>
```

In above example, we can know that

+ By tag name `w:clrSchemeMapping`, we can know it configure the scheme mapping table for document role.
+ In `w:bg1`, in the scheme mapping table, the property -- background color 1 is set to `light1`.
+ In `w:t1`, in the scheme mapping table, the property -- text color 1 is set to `dark1`.
+ In `w:bg2`, in the scheme mapping table, the property -- background color 2 is set to `light2`.
+ In `w:t2`, in the scheme mapping table, the property -- text color 2 is set to `dark2`.
+ In `w:accent1`, in the scheme mapping table, the property -- accent color 1 is set to `accent1`.
+ In `w:accent2`, in the scheme mapping table, the property -- accent color 2 is set to `accent2`.
+ In `w:accent3`, in the scheme mapping table, the property -- accent color 3 is set to `accent3`.
+ In `w:accent4`, in the scheme mapping table, the property -- accent color 4 is set to `accent4`.
+ In `w:accent5`, in the scheme mapping table, the property -- accent color 5 is set to `accent5`.
+ In `w:accent6`, in the scheme mapping table, the property -- accent color 6 is set to `accent6`.
+ In `w:hyperlink`, in the scheme mapping table, the property -- hyperlink is set to `hyperlink`.
+ In `w:followedHyperlink`, in the scheme mapping table, the property -- followed hyperlink 1 is set to `followedHyperlink`.
  
###### example 8.1 -- separator for number symbol
```
<w:decimalSymbol w:val="."/>
```

In above example, we can know that

+ In `<w:decimalSymbol w:val="."/>`, it specifies the separator of decimal symbol is `.`.

###### example 8.2 -- separator for list
```
<w:listSeparator w:val=","/>
```

In above example, we can know that

+ In `<w:listSeparator w:val=","/>`, it specifies the separator of list is `,`.

###### example 9 -- default setting for entire document
```
<w:docDefaults>
    <w:rPrDefault>
        <w:rPr>
            <w:rFonts w:asciiTheme="minorHAnsi" w:eastAsiaTheme="minorHAnsi" w:hAnsiTheme="minorHAnsi" w:cstheme="minorBidi"/>
            <w:sz w:val="22"/>
            <w:szCs w:val="22"/>
            <w:lang w:val="zh-TW" w:eastAsia="en-US" w:bidi="ar-SA"/>
        </w:rPr>
    </w:rPrDefault>
    <w:pPrDefault/>
</w:docDefaults>
```

In above example, we can know that

+ In `<w:docDefaults>`, it configures default settings for entire documents.
+ In `<w:rPrDefault>`, it configures default property of text run.
+ In `<w:rPr>`, it defines properties of text run.

###### example 10.1 -- default latent style
```
<w:latentStyles w:defLockedState="0" w:defUIPriority="99" w:defSemiHidden="1" w:defUnhideWhenUsed="1" w:defQFormat="0" w:count="267">
```

In above example, we can know that

+ In `w:latentStyles`, it specifies the default setting for latent styles.
+ In `w:defLockedState="0"`, it sets the locked state to `false` by default , meaning the latent styles will NOT be locked by default.
+ In `w:defUIPriority="99"`, it sets the ui priority of latent style to 99 by default.
+ In `w:defSemiHidden="1"`, it sets the semi-hidden state to `true` by default, meaning the latent styles are semi-hidden by default,</br>so that they will not be readily visible in the Styles pane unless they are in use in the document, by default.\
+ In `w:defUnhideWhenUsed`, it sets the unhide-when-used state to `true` by default, meaning that if a latent style is applied to content, then it will automatically become unhidden and visible in the Styles pane, by default.
+ In `w:defQFormat`, it sets the quick format style to `false`, meaning that latent styles are not included in the Quick Styles gallery, by default.
+ In `w:count="267"`, we can know there are 267 latent styles defined in the Word file.

###### example 10.2 -- LSD and latent style
```
<w:lsdException w:name="Normal" w:semiHidden="0" w:uiPriority="0" w:unhideWhenUsed="0" w:qFormat="1"/>
```

In above example, we can know that

+ In `w:lsdException`, it defines a latent style.
+ In `w:name="Normal"`, it uses `Normal` style.
+ In `w:semiHidden="0"`, it sets semi-hidden state to `false`, meaning that the latent style is NOT semi-hidden and will be visible in the Styles pane.
+ In `w:uiPriority="0"`, it sets the ui priority to zero.
+ In `w:unhideWhenUsed="0"`, the latent style is NOT unhide (i.e. become visible) when it is actually used.
+ In `w:qFormat="1"`, the latent style will be placed in Quick Style pane.

###### example 11.1 -- paragraph with frame configuration
```
<w:p>
  <w:pPr>
    <w:framePr w:w="2191" w:h="811" w:hRule="exact" w:hSpace="180"
w:wrap="around" w:vAnchor="text" w:hAnchor="page" w:x="1921"/>
  </w:pPr>
  <w:r>
    <w:t>Paragraph One</w:t>
  </w:r>
</w:p>
```

In above example, we can know that

+ In `<w:p>`, it defines a paragraph.
+ In `<w:pPr>`, it configures the properties of the paragraph.
+ In `<w:framePr>`, it defines a frame and configures properties of the frame.
+ In `w:w="2191"`, it sets the width of the frame is 2191 twips.
+ In `w:h="811"`, it sets the height of the frame is 811 twips.
+ In `w:hRule="exact"`, it specifies that the height should be exactly the value.
+ In `w:hSpace="180"`, it sets the horizontal spacing to 180 twips.
+ In `w:wrap="around"`, it will makes the surrounding text flow around all sides of the frame.
+ In `w:vAnchor="text"`, anchors the frame vertically to the flow of the surrounding text.
+ In `w:hAnchor="text"`, anchors the frame horizontally to the page margins.
+ In `w:x="1921"`, it positions the left side of the frame approximately 1921 twips from the left edge of the page.

###### example 12.1 -- always keep the paragraph in same page (if possible)
`~/word/document.xml` file under `Docx1.docx` file

```
<?xml version="1.0" encoding="utf-8" standalone="yes"?>
<!-- this tag `<w:document>` omitted -->
  <w:body>
    <w:p>
      <w:pPr>
        <w:t>This is the first paragraph -- (1)</w:t>
        <w:t>This is the first paragraph -- (2)</w:t>
        <w:t>This is the first paragraph -- (3)</w:t>
        <w:t>This is the first paragraph -- (4)</w:t>
        <w:t>This is the first paragraph -- (5)</w:t>
        <w:t>This is the first paragraph -- (6)</w:t>
        <w:t>This is the first paragraph -- (7)</w:t>
        <w:t>This is the first paragraph -- (8)</w:t>
        <w:t>This is the first paragraph -- (9)</w:t>
        <w:t>This is the first paragraph -- (10)</w:t>
        <w:t>This is the first paragraph -- (11)</w:t>
        <w:t>This is the first paragraph -- (12)</w:t>
        <w:t>This is the first paragraph -- (13)</w:t>
        <w:t>This is the first paragraph -- (14)</w:t>
        <w:t>This is the first paragraph -- (15)</w:t>
        <w:t>This is the first paragraph -- (16)</w:t>
      </w:pPr>
      <w:pPr>
        <w:keepLine/>
        <w:t>This is the second paragraph -- (1)</w:t>
        <w:t>This is the second paragraph -- (2)</w:t>
        <w:t>This is the second paragraph -- (3)</w:t>
        <w:t>This is the second paragraph -- (4)</w:t>
        <w:t>This is the second paragraph -- (5)</w:t>
        <w:t>This is the second paragraph -- (6)</w:t>
        <w:t>This is the second paragraph -- (7)</w:t>
        <w:t>This is the second paragraph -- (8)</w:t>
        <w:t>This is the second paragraph -- (9)</w:t>
        <w:t>This is the second paragraph -- (10)</w:t>
        <w:t>This is the second paragraph -- (11)</w:t>
        <w:t>This is the second paragraph -- (12)</w:t>
        <w:t>This is the second paragraph -- (13)</w:t>
        <w:t>This is the second paragraph -- (14)</w:t>
        <w:t>This is the second paragraph -- (15)</w:t>
        <w:t>This is the second paragraph -- (16)</w:t>
      </w:pPr>
    </w:p>
  </w:body>
</w:document>
```

In above example, 

There are two paragraphs, but here the second paragraph can not fit in the first page 

and `<w:keepLine/>` is present inside second `<w:pPr>`. 

Therefore, the second paragraph was moved to the beginning of the second page.

###### example 12.2 -- combine two paragraphs in same page (if possible)
```
<?xml version="1.0" encoding="utf-8" standalone="yes"?>
<!-- this tag `<w:document>` omitted -->
  <w:body>
    <w:p>
      <w:pPr>
        <w:t>This is the first paragraph -- (1)</w:t>
        <w:t>This is the first paragraph -- (2)</w:t>
        <w:t>This is the first paragraph -- (3)</w:t>
        <w:t>This is the first paragraph -- (4)</w:t>
        <w:t>This is the first paragraph -- (5)</w:t>
        <w:t>This is the first paragraph -- (6)</w:t>
        <w:t>This is the first paragraph -- (7)</w:t>
        <w:t>This is the first paragraph -- (8)</w:t>
        <w:t>This is the first paragraph -- (9)</w:t>
        <w:t>This is the first paragraph -- (10)</w:t>
        <w:t>This is the first paragraph -- (11)</w:t>
        <w:t>This is the first paragraph -- (12)</w:t>
        <w:t>This is the first paragraph -- (13)</w:t>
        <w:t>This is the first paragraph -- (14)</w:t>
        <w:t>This is the first paragraph -- (15)</w:t>
        <w:t>This is the first paragraph -- (16)</w:t>
      </w:pPr>
      <w:pPr>
        <w:t>This is the second paragraph -- (1)</w:t>
        <w:t>This is the second paragraph -- (2)</w:t>
        <w:t>This is the second paragraph -- (3)</w:t>
        <w:t>This is the second paragraph -- (4)</w:t>
        <w:t>This is the second paragraph -- (5)</w:t>
        <w:t>This is the second paragraph -- (6)</w:t>
        <w:t>This is the second paragraph -- (7)</w:t>
        <w:t>This is the second paragraph -- (8)</w:t>
      </w:pPr>
      <w:pPr>
        <w:t>This is the third paragraph -- (1)</w:t>
        <w:t>This is the third paragraph -- (2)</w:t>
        <w:t>This is the third paragraph -- (3)</w:t>
        <w:t>This is the third paragraph -- (4)</w:t>
        <w:t>This is the third paragraph -- (5)</w:t>
        <w:t>This is the third paragraph -- (6)</w:t>
        <w:t>This is the third paragraph -- (7)</w:t>
        <w:t>This is the third paragraph -- (8)</w:t>
      </w:pPr>
    </w:p>
  </w:body>
</w:document>
```

In above example,

There are three paragraphs.

`<w:keepLNext/>` is present inside second `<w:pPr>`. It combines the second paragraph and third paragraph as a group.

However, the group can not fit in the first page.

Therefore, the second paragraph and third paragraph were moved to the beginning of the second page.

> [!TIP]
> You can think `<w:keepNext/>` combines this paragraph and next paragraph into a group.
>
> So that, it is not allowed to have page section break between this paragraph and next paragraph
>
> (if possible, e.g. the second paragraph and third paragraph does not hold over than one page in total).

In above example, we can know that

+ In `<w:outlineLvl w:val="0" />`, this paragraph is of outline level 1, and if a table of contents field is inserted that utilizes outlines levels, the text in this paragraph is at level one in the TOC.

###### example 13.1 -- style definition
part code of `~/word/style.xml` in a Word file.

```
<w:style w:type="paragraph" w:styleId="Heading2">
    <w:name w:val="heading 2"/>
    <w:basedOn w:val="Normal"/>
    <w:next w:val="Normal"/>
    <w:link w:val="Heading2Char"/>
    <w:uiPriority w:val="9"/>
    <w:unhideWhenUsed/>
    <w:qFormat/>
    <w:rsid w:val="00263428"/>
    <w:pPr>
        <!-- tags omitted -->
    </w:pPr>
    <w:rPr>
        <!-- tags omitted -->
    </w:rPr>
</w:style>
```

In above example, we can know that

+ In `<w:style w:type="paragraph" w:styleId="Heading2">`, it defines a style named `Heading2` that applies to paragraph.
+ In `<w:name w:val="heading 2"/>`, it gives an alias as `heading 2`.
+ In `<w:basedOn w:val="Normal"/>`, it inherits the style named `Normal`.
+ In `<w:link w:val="Heading2Char"/>`, it defines a hyperlink that, when clicked, will jump the reader to a specific location within the same Word document where text has been formatted using a character style called "Heading2Char".

###### example 13 -- formatted as superscript
```
<w:r>
  <w:rPr>
    <w:vertAlign w:val="superscript"/>
  </w:rPr>
  <w:t>2</w:t>
</w:r>
```

In above example, we can know that

+ In `<w:vertAlign w:val="superscript"/>`, indicates that the text within the current run should be formatted as superscript.

It would represent the number "2" formatted as a superscript.

###### example 14.1 -- defines a footer
```
<w:ftr w:type="default">
  <w:p w:rsidR="602E0000" w:rsidRDefault="602E0000">
    <w:r>
      <w:fldChar w:fldCharType="begin"/>
    </w:r>
    <w:r>
      <w:instrText xml:space="preserve"> PAGE   \* MERGEFORMAT </w:instrText>
    </w:r>
    <w:r>
      <w:fldChar w:fldCharType="separate"/>
    </w:r>
    <w:r>
      <w:rPr>
        <w:noProof/>
      </w:rPr>
      <w:t>1</w:t>
    </w:r>
    <w:r>
      <w:fldChar w:fldCharType="end"/>
    </w:r>
  </w:p>
</w:ftr>
```

In above example, we can know that

+ In `<w:ftr w:type="default">`, it defines a footer with default type.</br>That is, the content in this footer should be displayed as the regular footer for all pages in that section, unless there are specific first-page or even/odd page footers defined for the same section.

+ In `<w:p w:rsidR="602E0000" w:rsidRDefault="602E0000">`, it defines a paragraph. It specifies the revision save identifier for the run as `602E0000`, and the revision save identifier for the default run as `602E0000`.
+ In

```
    <w:r>
      <w:fldChar w:fldCharType="begin"/>
    </w:r>
```

it defines a run. It acts as the marker that divides the "how to calculate/display" part of the field from the "currently displayed value" part.

+ In

```
    <w:r>
      <w:instrText xml:space="preserve"> PAGE   \* MERGEFORMAT </w:instrText>
    </w:r>
```

it defines a run. In the run, it defines an instruction text

which will display the current page number, and the formatting of the displayed page number should be maintained, even if the field is refreshed.

Let's dive into this tag -- `<w:instrText xml:space="preserve"> PAGE   \* MERGEFORMAT </w:instrText>`.

    - `<w:instrText>`: it specifically holds the instruction text for a field. It tells Word what kind of dynamic content to display.
    - `xml:space="preserve"`: This attribute indicates that any whitespace within the enclosed text should be preserved exactly as it is.
    - `PAGE \* MERGEFORMAT`: This is the actual field code.
        1. `PAGE`: it tells Word to display the current page number.
        2. `\*`: it is a field switch, introducing a formatting instruction.
        3. `MERGEFORMAT`: It specific switch instructs Word to preserve the formatting of the field result if the field is updated.
        
+ In
   
```
    <w:r>
      <w:fldChar w:fldCharType="separate"/>
    </w:r>
```

it defines a run. In the run, it defines a field character that represents the point where the field instructions end and the field result (the displayed value) begins.

+ In

```
    <w:r>
      <w:rPr>
        <w:noProof/>
      </w:rPr>
      <w:t>1</w:t>
    </w:r>
```

it defines a run with these properties:

    - the text in this run should be ignored by Word's spell and grammar checkers.

And there are only a text `1` in the run (according by `<w:t>1</w:t>`).

+ In

```
    <w:r>
      <w:fldChar w:fldCharType="end"/>
    </w:r>
```

it marks the end of a field in the Word document.

###### example 14.2 -- refers footers
part of content in `~/word/document.xml` in `InsertSectionExample.docx`.

```
<w:p>
    <w:pPr>
        <w:sectPr w:rsidR="003E25F4" w:rsidSect="00FC3028">
            <w:pgSz w:w="11906" w:h="16838"/>
            <w:pgMar w:top="1440" w:right="1440" w:bottom="1440" w:left="1440" w:header="708" w:footer="708" w:gutter="0"/>
            <w:cols w:space="708"/>
            <w:docGrid w:linePitch="360"/>
            <w:footerReference w:type="even" r:id="R3d26812d683949a8"/>
            <w:footerReference w:type="first" r:id="R1a4d6aee14a84bf5"/>
            <w:footerReference w:type="default" r:id="R812e7120657b4c46"/>
            <w:titlePg/>
        </w:sectPr>
    </w:pPr>
</w:p>
```

In above example, we can know that

+ It defines a paragraph.
+ In the paragraph, it defines a section whose revision save identifier for run is `003E25F4` and that for section is `00FC3028`.
+ In the section, it sets the page width to `11906` twips and its height to `16838` twips.
+ In the section, it sets top-margin right-margin, bottom-margin, left-margin of the page to `1440` twips, </br>distance from the top to the header is `708` twips,</br>distance from the bottom to the footer is `708` twips, and</br> gutter margin to zero twips.
+ In the section, if there are has multiple columns, there will be a spacing of 708 twips between them.
+ In the section, it sets the vertical spacing between lines of text within the grid to 360 twips.
+ In `<w:footerReference w:type="even" r:id="R3d26812d683949a8"/>`, in the section, it refers a footer for even-numbered pages. Its id that links the footer is `R3d26812d683949a8`.
+ Similarly, in `<w:footerReference w:type="first" r:id="R1a4d6aee14a84bf5"/>`, in the section, it refers a footer for first page. Its id that links the footer is `R1a4d6aee14a84bf5`.
+ While, in `<w:footerReference w:type="default" r:id="R812e7120657b4c46"/>`, in the section, it refers a footer for all pages. Its id that links the footer is `R812e7120657b4c46`.
  
###### example 16.1 -- defines a footnote
part of content in `~/word/footernotes.xml` in `FootNoteExample1.docx`

```
<w:footnotes xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">
    <w:footnote w:id="0" w:type="continuationSeparator">
        <w:p>
            <w:pPr>
                <w:spacing w:lineRule="auto" w:line="240" w:after="0"/>
            </w:pPr>
            <w:r>
                <w:continuationSeparator/>
            </w:r>
        </w:p>
    </w:footnote>
</w:footnotes>
```

In above example, we can know that

+ In `<w:footnotes xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">`, it acts like a container that defines the footnotes, and it refers to Word Office 2006 (according to `xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main"`).
+ In `<w:footnote w:id="0" w:type="continuationSeparator">`, it defines a footnote and encapsulate the properties inside this tag.
+ In `<w:p>`, it defines a paragraph in the footnote.
+ In

```
            <w:pPr>
                <w:spacing w:lineRule="auto" w:line="240" w:after="0"/>
            </w:pPr>
```

it defines the property of paragraph, and setting the amount of vertical space before, within, and after a paragraph or run as follows.

    - w:lineRule="auto": Word automatically adjusts the vertical line spacing to accommodate the size of the font and any other inline elements on the line.
    - w:line="240": it instructs Word to apply single line spacing as 240 twips, which is 240/20 = 12 points. Thus, the base of vertical line spacing is set to the equivalent of 12 points.
    - w:after="0": spacing 0 twips after the paragraph, meaning that it has no extra space after paragraph.

+ In

```
            <w:r>
                <w:continuationSeparator/>
            </w:r>
```
    
it is the instance of that separator being placed within the flow of the document, specifically within a paragraph.

###### example 15.1 -- defines a footnote
other part of content in `~/word/footernotes.xml` in `FootNoteExample1.docx`

```
<w:footnotes xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">
    <w:footnote xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main" w:id="1">
        <w:p xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">
            <w:pPr>
                <w:pStyle w:val="FootnoteText"/>
            </w:pPr>
            <w:r>
                <w:rPr>
                    <w:rStyle w:val="FootnoteReference"/>
                </w:rPr>
            <w:footnoteRef/>
            </w:r>
            <w:r>
                <w:t xml:space="preserve"> </w:t>
            </w:r>
            <w:r>
                <w:t>This is a footnote.</w:t>
            </w:r>
        </w:p>
    </w:footnote>
</w:footnotes>
```

In above example, we can know that

+ In `<w:footnotes xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">`, it acts like a container that defines the footnotes, and it refers to Word Office 2006 (according to `xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main"`).
+ In

```
            <w:pPr>
                <w:pStyle w:val="FootnoteText"/>
            </w:pPr>
```

it defines the style paragraph whose name is `FootnoteText`.

+ In

```
            <w:r>
                <w:rPr>
                    <w:rStyle w:val="FootnoteReference"/>
                </w:rPr>
            <w:footnoteRef/>
            </w:r>
```

it defines a run in the paragraph. In the run, it defines a style of the run whose name is `FootnoteReference`.

And it represents the actual in-text marker that signals the presence of a footnote.

+ In

```
            <w:r>
                <w:t xml:space="preserve"> </w:t>
            </w:r>
```

it defines a run that contains text -- a single space ` `.

+ In

```
            <w:r>
                <w:t>This is a footnote.</w:t>
            </w:r>
```

it defines a run that contains text -- `This is a footnote.`, but Word will handle whitespace according to its default rules (collapsing multiple spaces into one, etc.) since `xmlns:space` attribute is NOT explicitly specified.

###### example 16.1 -- refers an endnote
part of content in `~/word/endnotes.xml` in `ModifyParagraphsExample1.docx`

```
<w:endnote xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main" w:id="2">
    <w:p xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">
        <w:pPr>
            <w:pStyle w:val="EndnoteText"/>
        </w:pPr>
        <w:r>
            <w:rPr>
                <w:rStyle w:val="EndnoteReference"/>
            </w:rPr>
            <w:endnoteRef/>
        </w:r>
        <w:r>
            <w:t xml:space="preserve"> </w:t>
        </w:r>
        <w:r>
            <w:t>This is an endNote.</w:t>
        </w:r>
    </w:p>
</w:endnote>
```

In above example, we can know that

+ In `<w:endnote xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main" w:id="2">`, it defines a footnote with id `2`. And it uses Office Word 2006.
+ In

```
        <w:pPr>
            <w:pStyle w:val="EndnoteText"/>
        </w:pPr>
```

it sets the style name of the paragraph to `EndnoteText`.

+ In

```
        <w:r>
            <w:rPr>
                <w:rStyle w:val="EndnoteReference"/>
            </w:rPr>
            <w:endnoteRef/>
        </w:r>
```

In the paragraph, it defines a run whose style name is `EndnoteReference` 

and defines an endnote reference character.

+ In

```
        <w:r>
            <w:t xml:space="preserve"> </w:t>
        </w:r>
```

In the paragraph, it defines a run. 

In the run, it defines a text -- one space (` `). And the text is preserved any whitespace characters exactly as they appear within the `<w:t>` tag.

+ In

```
        <w:r>
            <w:t>This is an endNote.</w:t>
        </w:r>
```

In the run, it defines a text -- `This is an endNote.`.

###### example 17.1 -- simple field
part of content in `~/word/document.xml` in `InsertPageCountExample1.docx`.

```
<w:fldSimple w:instr=" NUMPAGES \* MERGEFORMAT ">
    <w:r xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main" w:rsidR="001D0226">
        <w:rPr xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">
            <w:lang w:val="zh-TW"/>
        </w:rPr>
        <w:t>1</w:t>
    </w:r>
</w:fldSimple>
```

In above example, we can know that

+ In `<w:fldSimple w:instr=" NUMPAGES \* MERGEFORMAT ">`, it defines a simple field where its field instruction is `NUMPAGES \* MERGEFORMAT`.

As my notes -- [syntax of field instruction in `<w:instrText>` tag section](https://github.com/40843245/OOXML/blob/main/Word/structure/CH1%20--%20syntax.md#syntax-of-field-instruction-in-winstrtext-tag) said, 

```
{fieldInstruction}:= {whitespaces}{fieldIdentifier}{whitespaces}{switches}?{whitespaces}{arguments}?{whitespaces}
```

```
{whitespaces}:= {whitespace}+

{whitespace}:= ({space}|{tab})

{space}:= ` `

{tab}:= \t
```

We can know 

    - its field identifier is `NUMPAGES`, meaning that Word will display the total number of pages in the document.
    - its switch control is `\* MERGEFORMAT`, meaning that Word will preserve the formatting that is applied to the field result.  After the field is updated, Word will recompose (updates it using the preserved formatting).

In summary, it represents a field in the Word document that will display the total number of pages in the document and will try to maintain its formatting upon updates.

+ In

```
    <w:r xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main" w:rsidR="001D0226">
        <w:rPr xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">
            <w:lang w:val="zh-TW"/>
        </w:rPr>
        <w:t>1</w:t>
    </w:r>
```

it defines a run which is specific to Office Word 2006.

In the run, it specifies the language as Tradition Chinese and there is a text `1`.

###### example 17.2 -- simple field
other part of content in `~/word/document.xml` in `InsertPageCountExample1.docx`.

```
<w:fldSimple w:instr=" SECTIONPAGES \* MERGEFORMAT ">
    <w:r xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main" w:rsidR="001D0226">
        <w:rPr xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">
            <w:lang w:val="zh-TW"/>
        </w:rPr>
        <w:t>1</w:t>
    </w:r>
</w:fldSimple>
```

In above example, we can know that

+ In `<w:fldSimple w:instr=" NUMPAGES \* MERGEFORMAT ">`, it defines a simple field where its field instruction is `NUMPAGES \* MERGEFORMAT`.

As my notes -- [syntax of field instruction in `<w:instrText>` tag section](https://github.com/40843245/OOXML/blob/main/Word/structure/CH1%20--%20syntax.md#syntax-of-field-instruction-in-winstrtext-tag) said, 

```
{fieldInstruction}:= {whitespaces}{fieldIdentifier}{whitespaces}{switches}?{whitespaces}{arguments}?{whitespaces}
```

```
{whitespaces}:= {whitespace}+

{whitespace}:= ({space}|{tab})

{space}:= ` `

{tab}:= \t
```

We can know 

    - its field identifier is `SECTIONPAGES`, meaning that Word will display the total number of pages in the current section of the document.
    - its switch control is `\* MERGEFORMAT`, meaning that Word will preserve the formatting that is applied to the field result.  After the field is updated, Word will recompose (updates it using the preserved formatting).

In summary, it represents a field in the Word document that will display the total number of pages in current section of the document and will try to maintain its formatting upon updates.

+ In

```
    <w:r xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main" w:rsidR="001D0226">
        <w:rPr xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">
            <w:lang w:val="zh-TW"/>
        </w:rPr>
        <w:t>1</w:t>
    </w:r>
```

it defines a run which is specific to Office Word 2006.

In the run, it specifies the language as Tradition Chinese and there is a text `1`.

###### example 17.3 -- field simple
part of content of `~/word/document.xml` file under `InsertPageCountExample2.docx` file.

```
<w:p>
    <w:fldSimple w:instr=" PAGE \* MERGEFORMAT ">
        <w:r xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main" w:rsidR="001D0226">
            <w:rPr xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">
                <w:lang w:val="zh-TW"/>
            </w:rPr>
            <w:t>1</w:t>
        </w:r>
    </w:fldSimple>
    <w:pPr/>
    <w:r>
        <w:rPr>
            <w:lang w:val="zh-TW"/>
        </w:rPr>
        <w:t>This is the 1th paragraph.</w:t>
    </w:r>
</w:p>
```

Thus, the 
In above example, we can know that

+ In `<w:p>`, it defines a paragraph.
+ In `<w:fldSimple w:instr=" PAGE \* MERGEFORMAT ">`, it defines a simple field</br>which is for current page (according to `field identifier` is set to `PAGE`) and maintain formatting upon updating the field (according to `switch controller` is set to `\* MERGEFORMAT`.
+ In `<w:r xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main" w:rsidR="001D0226">`, it defines a run in the paragraph, which targets on Office Word 2006, and its revision save identifier for the run is `001D0226`.
+ In

```
            <w:rPr xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">
                <w:lang w:val="zh-TW"/>
            </w:rPr>
```

it defines properties of the run where it is opened with Office Word 2006. 

It set the language of the run (in Word Office 2006) is Traditional Chinese.

+ In `<w:t>1</w:t>`, it defines a text -- `1`.
+ In `<w:pPr/>`, it defines properties of the paragraph, with no configurations, meaning that the paragraph will use the default settings.

```
    <w:r>
        <w:rPr>
            <w:lang w:val="zh-TW"/>
        </w:rPr>
        <w:t>This is the 1th paragraph.</w:t>
    </w:r>
```

it defines a run whose language is in Traditional Chineses and contains text -- `This is the 1th paragraph.`

It will output like this:

<img width="776" alt="image" src="https://github.com/user-attachments/assets/9eebe2ec-73e0-42a2-adbb-22ccf618721b" />

![image](https://github.com/user-attachments/assets/60bca40e-ed57-42d5-932f-656b8dba428c)

###### example 18.1 -- content controls
```
<w:sdt>
  <w:sdtPr>
    <w:id w:val="-1234567890"/>
    <w:docPartObj>
      <w:docPartGallery w:val="Cover Pages"/>
    </w:docPartObj>
  </w:sdtPr>
  <w:sdtContent>
  </w:sdtContent>
</w:sdt>
```

In above example, we can know that

+ In `<w:sdt>`, it acts like a container for the structured document tag.
+ In `<w:sdtPr>`, it defines properties of the structured document tag.
+ In `<w:id w:val="-1234567890"/>`, it sets the identifier of the structured document tag to `-1234567890`.
+ In `<w:docPartObj>`, it signifies that this SDT is designed to host a document part, which in this context refers to a building block.
+ In `<w:docPartGallery w:val="Cover Pages"/>`, it defines the type of building blocks that will be displayed in this content control.
+ In `<w:sdtContent>`, it is empty, which indicates that there are no actual content that is currently present within the content control.

###### example 18.2 -- TOC (table of contents)
part of content in `~/word/document.xml` under `InsertTableOfContentExample.docx` file.

```
<w:sdt xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">
    <w:sdtPr>
        <w:docPartObj>
            <w:docPartGallery w:val="Table of Contents"/>
            <w:docPartUnique/>
        </w:docPartObj>
        \
    </w:sdtPr>
    <w:sdtEndPr>
        <w:rPr>
            <!-- tags omitted -->    
        </w:rPr>
    </w:sdtEndPr>
    <w:sdtContent>
        <w:p>
            <w:pPr>
                <w:pStyle w:val="TOCHeading"/>
            </w:pPr>
            <w:r>
                <w:t>Teams</w:t>
            </w:r>
        </w:p>
        <w:p>
            <w:pPr>
                <w:pStyle w:val="TOC1"/>
                <w:tabs>
                    <w:tab w:val="right" w:leader="dot" w:pos="9010"/>
                </w:tabs>
                <w:rPr>
                    <w:noProof/>
                </w:rPr>
            </w:pPr>
            <w:r>
                <w:fldChar w:fldCharType="begin" w:dirty="true"/>
            </w:r>
            <w:r>
                <w:instrText xml:space="preserve"> TOC \o "1-3" \u \z \h </w:instrText>
            </w:r>
            <w:r>
                <w:fldChar w:fldCharType="separate"/>
            </w:r>
        </w:p>
        <w:p>
            <w:r>
                <w:rPr>
                    <w:b/>
                    <w:bCs/>
                    <w:noProof/>
                </w:rPr>
                <w:fldChar w:fldCharType="end"/>
            </w:r>
        </w:p>
    </w:sdtContent>
</w:sdt>
```

In above example, we can know that

+ In `<w:sdt xmlns:w="http://schemas.openxmlformats.org/wordprocessingml/2006/main">`, it acts a container for SDT, but it uses Office 2006.
+ In `<w:sdtPr>`, it defines the properties of the SDT.
+ In `<w:docPartObj>`, it indicates that the SDT is related to a document part (building block).
+ In `<w:docPartGallery w:val="Table of Contents"/>`, it specifies that the building block gallery associated with this content control</br>should display items related to TOC.</br>This allows users to choose from different styles for TOC.
+ In `<w:docPartUnique/>`, it ensures that there is exactly one document part in the SDT. The reason why we do so is that we always want to exactly one TOC in a document.
+ In `<w:sdtEndPr>`, it defines properties for the end of the SDT.
+ In `<w:sdtContent>`, it contain the markup for a dynamically generated TOC.
+ In

```
        <w:p>
            <w:pPr>
                <w:pStyle w:val="TOCHeading"/>
            </w:pPr>
            <w:r>
                <w:t>Teams</w:t>
            </w:r>
        </w:p>
```

it defines a paragraph with run of text `Teams`. It also sets the style name of the paragraph to `TOCHeading`.

+ In

```
        <w:p>
            <w:pPr>
                <w:pStyle w:val="TOC1"/>
                <w:tabs>
                    <w:tab w:val="right" w:leader="dot" w:pos="9010"/>
                </w:tabs>
                <w:rPr>
                    <w:noProof/>
                </w:rPr>
            </w:pPr>
            <!-- tags omitted -->
        </w:p>
```

it defines a paragraph whose style name is `TOC1`.

And it defines a tab stop at the end of the paragraph with `9010` twips and filled with `dot` for spacing.

For the run of the paragraph, it will NOT use proofing tool, meaning that it will NOT check the spelling.

+ In

```
        <w:p>
            <!-- tags omitted -->
            <w:r>
                <w:fldChar w:fldCharType="begin" w:dirty="true"/>
            </w:r>
            <w:r>
                <w:instrText xml:space="preserve"> TOC \o "1-3" \u \z \h </w:instrText>
            </w:r>
            <w:r>
                <w:fldChar w:fldCharType="separate"/>
            </w:r>
        </w:p>
```

In the paragraph, `w:fldCharType="begin"` attribute clearly marks this as the starting point of a field.

While, `w:dirty="true"` attribute suggests that the field's result might be outdated and needs to be recalculated or updated.

And add separator in the simple field.

And the format should be 

```
[BEGIN FIELD] [INSTRUCTIONS] [SEPARATOR] [FIELD RESULT AREA] [END FIELD]
```

+ In 

```
        <w:p>
            <w:r>
                <w:rPr>
                    <w:b/>
                    <w:bCs/>
                    <w:noProof/>
                </w:rPr>
                <w:fldChar w:fldCharType="end"/>
            </w:r>
        </w:p>
```

It defines a paragraph.

It defines a run in the paragraph.

In the run, it sets font of the run is bold for all text and NOT use the proofing tool.

It defines field character which marks the end of a field.

#### about `m` namespace
##### elements in `m` namespace
| element in xml tag | stands for (represented as tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `<m:mathPr>` | | math properties | configures properties about math. | | |
| `<m:mathFont>` | | math font | configures properties of font that used in mathematical content. | | |
| `<m:brkBin>` | | *br*ea*k* on *bin*ary operators | configures properties of break on binary operator (such as `+` in `3+4`.) that used in mathematical content. | See `Appendix 5`[^4] for more information. | |
| `<m:brkBinSub>` | | substitution string for *br*ea*k* on *bin*ary operators | configures properties of substitution string for break on binary operators (such as `+` in `3+4`.) that used in mathematical content.</br>Simply said, it configures the text to be displayed as a visual indicator of a broken binary operation. | See `Appendix 5`[^4] for more information.| |
| `<m:smallFrac>` | | small *frac*tion style | configure the setting for the display of inline fractions. | | DON'T confuse small *frac*tion style and style of small fraction (i.e. the style of fraction which is small (with small numerator and denominator)). |
| `<m:dispDef/>` | | display mode for default setting | indicates that the default display mode for equations (inline or block) should be determined by the application's default settings |
| `<m:lMargin/>` | | left margin | left margin for displayed (block-level) equations. | | |
| `<m:rMargin/>` | | right margin | right margin for displayed (block-level) equations. | | |
| `<m:defJc/>` | | *def*ault *j*ustifi*c*ation | configures default justification for groups to an equation. | | |
| `<m:wrapIndent>` | | wrap indent | configure indentation for wrapped lines within multiline equations. | | |
| `<m:intLim>` | | *int*egration *lim*itation | configures limits of integration should be displayed as.  | | | | 
| `<m:naryLim>` | | *n*-*ary* operation *lim*itation | configures limits of n-ary operator should be displayed as.  | | | 

##### atttribute about `m` namespace
###### attribute in `<m:brkBin>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | determines which position the binary operator should be placed when it has neccessary line break of the expression with a binary operator. | | |

###### attribute in `<m:brkBinSub>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | the string that will replaced to for the line break on an expression with a binary operator. | | |

###### attribute in `<m:smallFrac>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | determines small fraction style is enabled or disabled. | | |

###### attribute in `<m:lMargin>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | determines left margin of the equation | its unit is in twips. | |

###### attribute in `<m:rMargin>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | determines right margin of the equation | its unit is in twips. | |

###### attribute in `<m:defJc>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | determines justification of the equation in the default settings | | |

###### attribute in `<m:wrapIndent>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | determines indentation for wrapping text in a multiline equation. | | |

###### attribute in `<m:intLim>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | determines the behaviour for limitations of integration operators. | | |

> [!NOTE]
> Integration operators includes:
>
> + integral: <img width="71" alt="image" src="https://github.com/user-attachments/assets/22d6eb26-9b8f-4b7d-91b2-5b6e75ed3582" />
> + summation: <img width="50" alt="image" src="https://github.com/user-attachments/assets/d6e87f62-8e05-4a91-8081-e1bb62088943" />
> + product: <img width="82" alt="image" src="https://github.com/user-attachments/assets/4f1127b4-8c9b-484c-a338-895f20e96961" />

> [!NOTE]
> This is an example of equation that apply the configuration set by `<m:intLim m:val="subSup">`.
>
> <img width="570" alt="image" src="https://github.com/user-attachments/assets/5e850987-7ee7-425e-abee-daec42024f51" />

> [!NOTE]
> This is an example of equation that apply the configuration set by `<m:intLim m:val="undOvr">`.
>
> <img width="445" alt="image" src="https://github.com/user-attachments/assets/61b8c6bf-bd28-4eb9-8489-96778d353194" />

###### attribute in `<m:naryLim>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `m:val` | | | determines the behaviour for limitations of n-ary operators | | |

> [!NOTE]
> n-ary operators includes:
>
> + summation: <img width="50" alt="image" src="https://github.com/user-attachments/assets/d6e87f62-8e05-4a91-8081-e1bb62088943" />
> + product: <img width="82" alt="image" src="https://github.com/user-attachments/assets/4f1127b4-8c9b-484c-a338-895f20e96961" />
> + union: <img width="22" alt="image" src="https://github.com/user-attachments/assets/fc6ffa1f-d2c5-44fd-a9f0-7881fefe2f06" />
> + intersection: <img width="22" alt="image" src="https://github.com/user-attachments/assets/88a3d1a0-a3d4-4d2c-87a4-b84757f254d9" />

> [!NOTE]
> An example of equations that use the configuration set by `<m:naryLim m:val="subSup"/>`.
>
> <img width="509" alt="image" src="https://github.com/user-attachments/assets/3c11af0e-f8c5-4f0c-919a-82861352179e" />

> [!NOTE]
> An example of equations that use the configuration set by `<m:naryLim m:val="undOvr"/>`.
>
> <img width="547" alt="image" src="https://github.com/user-attachments/assets/1149ce2c-8790-4579-b1ff-f0a43c03c835" />

##### examples and explanations
###### example 1.1 -- configuration about math equation
```
<m:mathPr>
    <m:mathFont m:val="Cambria Math"/>
    <m:brkBin m:val="before"/>
    <m:brkBinSub m:val="--"/>
    <m:smallFrac m:val="off"/>
    <m:dispDef/>
    <m:lMargin m:val="0"/>
    <m:rMargin m:val="0"/>
    <m:defJc m:val="centerGroup"/>
    <m:wrapIndent m:val="1440"/>
    <m:intLim m:val="subSup"/>
    <m:naryLim m:val="undOvr"/>
</m:mathPr>
```

In above example, we can know that

+ In `<m:mathPr>`, it defines the properties about math equation.
+ In `<m:mathFont m:val="Cambria Math"/>`, it configures the default font for math equation is `Cambria Math`.
+ In `<m:brkBin m:val="before"/>`, it indicates that the binary operator should be at the beginning of the new line if the expression with a binary operator.
+ In `<m:brkBinSub m:val="--"/>`, it indicates when line break is necessary, it will place the `--` around the binary operator.
+ In `<m:smallFrac m:val="off"/>`, it disables small fraction style, meaning that the fraction will not be displayed in smaller size, ensuring that the fraction can be displayed in standard size.
+ In `<m:dispDef/>`, the math equation will be rendered with this displayed style by default.
+ In `<m:lMargin m:val="0"/>`, left-margin is 0.
+ In `<m:rMargin m:val="0"/>`, right-margin is 0.
+ In `<m:defJc m:val="centerGroup"/>`, the default justification of math equation is center-aligned. It is applied to a group of element.
+ In `<m:wrapIndent m:val="1440"/>`, when wrapping the text on a math equation, it indents 1440 twips.
+ In `<m:intLim m:val="subSup"/>`, for integration operators, the lower limit will be placed as sub-script and upper limit will be placed in super-script. 
+ In `<m:naryLim m:val="undOvr"/>`, for n-ary operator, the n-th symbol should be displayed underneath and over the equation.

[^1]:[Prequisite Review 1 -- terms](https://github.com/40843245/XmlOfOffice/blob/main/Word/structure/Prequisite%20Review%201%20--%20terms.md)

[^2]:[Appendix 2 -- available options of attribute of tag in xml for Word](https://github.com/40843245/XmlOfOffice/blob/main/Word/structure/Appendix%202%20--%20available%20options%20of%20attribute%20of%20tag%20in%20xml%20for%20Word.md#appendix-2----available-options-of-attribute-of-tag-in-xml-for-word)

[^3]:[`Appendix 1 -- tags in xml`](https://github.com/40843245/Xml/blob/main/structure/Appendix%201%20--%20tags%20in%20xml.md)

[^4]: [Appendix 5 -- break on binary operations](https://github.com/40843245/XmlOfOffice/blob/main/Word/structure/Appendix%205%20--%20break%20on%20binary%20operations.md)

[^5]:[9.2 Relationships in Office Open XML](https://ooxml.info/docs/9/9.2/)

[^6]:[ DocumentFormat.OpenXml.Linq.WNE class (MSDS API reference)](https://learn.microsoft.com/en-us/dotnet/api/documentformat.openxml.linq.wne?view=openxml-3.0.1) 

[^7]:[`docx格式文档详解：xml解析并用html还原`](https://juejin.cn/post/7166821284087595038)
