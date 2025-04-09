# Appendix 1 -- xml tag in Document.md
## Prequisite
To have a better understanding of a list of tags in OOXML, it's better to be familiar with these basic knowledgement or concepts before looking at these articles.

+ concept of layout, style, headings etc that will be used in a Document.
+ commonly used terms. (Some advanced terms can be reviewed at this article -- `Prequisite Review 1 -- terms`[^1] )
+ commonly used tags (and theire attributes) in native html5 and native xml.
+ concepts of namespace, class in OO (Object-Oriented) design pattern.
+ concepts of `Part and Relationship in OOXML`[^4].

## Suggestion
Here is my suggestion to reader.

**NEVER cram these tags in OOXML into your brain (死記，沒理解就硬塞東西)**. Otherwise, you may got stuck on this.

Just understand these commonly used tags in OOXML then remember (理解在記住) it.

For those uncommonly used tags and attribute, **search it when you need it**. 

After all, it only lists some tags and its attribute in OOXML. 

It's like a dictionary, search it when you want to know a vocabulary.

## tables
> [!WARNING]
> Most content of these table are refered from Google Gemini's answer or from non-official website, which BOTH may be incorrect.
>
> Read with caution.

### namespace declaration in xml tag 
| namespace in xml tag | stands for (represented as tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `xmlns` | | xml namespace | declare a namespace in xml. Or configure the property in xml (such as `xmlns:aml`) | | |

### namespace under `xmlns` namespace
| namespace under `xmlns` namespace | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `aml` | *A*nnotation *M*arkup *L*anguage | used for comments and revisions. | | |
| `dt` | *D*ata *T*ypes | often used for properties or values within the document. | | |
| `mc` | *Markup* *C*ompatibility | determine which version of documents are allowed to be able to be compatible with different versions of Office Open XML. | | |
| `o` | *O*ffice | it is for Office-specific elements, often related to general Office document properties. | | | 
| `v` | *V*ector Markup Language | it is for Vector Markup Language, which is a legacy format for vector graphics in Office documents. | | |
| `w10` | *W*ord *10*-specific elements | it is for Word 10-specific elements, indicating features or settings from that version. | | |
| `w` | *W*ord 2003 elements | it is the primary namespace for Word 2003 XML. | reason about why it is for Word 203 XML see following history. | |
| `wx` | *W*ord 2003 Au*x*iliary Hints | it is for Word 2003 Auxiliary Hints, which might contain additional information for specific Word features. | The word `Auxiliary` has a meaning of the word `Extension`, but its usage of the word `Auxiliary` is narrower and more concise than that of the word `Extension`, and we usually abbreviates the word `Extension` to `X`. And I guess this is the reason why the namespace is declared as `wx`. | |
| `wne`| WNE | it points to elements from which version (according to the value of `xmlns:wne`). Its presence suggests potential compatibility features or elements used across versions. | See `WNE class`[^5] for more details. | | 
| `wsp` | *W*ord *S*ervice *P*ack | This namespace might relate to Word xxx (version according to value of `xmlns:wsp` ) Service Pack 2 specific elements or extensions. | | | 
| `sl` | *S*chema *L*ibrary | This namespace could be for a Schema Library, possibly related to document templates or components. | | | 

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

### namespace in xml tag for OOXML
| namespace in xml tag | stands for (represented as tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w` | | Microsoft Word | indicates that it describes xml content of a Microsoft Word file.| w stands for Microsoft *W*ord | |

### namespace declared in `<w:wordDocument>`
You can know which namespaces in `xmlns` namespace are declared through finding `xmlns` in `<w:wordDocument>`.

| namespace in xml tag | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `o` | *O*ffice-specific namespace | it contains metadata about the Word document itself. | | |

### element in xml tag for OOXML
#### `<o>` namespace
`o` namespace contains metadata about the Word document itself.

| element in xml tag | stands for (represented as tag in native xml or native html5)  | meaning | description | notes | notice |
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

###### xml attribute
###### attribute in `<o>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |

#### `<w>` namespace
| element in xml tag | stands for (represented as tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `<w:wordDocument>` | `<html>` | root node | the root node of a Microsoft Word file. | | |
| `<w:ignoreSubtree>` | | ignore a specific subtree | it instructs the Word processor to ignore a specific subtree of the XML document (according to the value of `w:val` attribute) during processing. | | | 
| `<w:body>` | `<body>` | body | the main part of file in native xml (and native html5) | | |
| `<w:lang>` | `<lang>` | language | the language for characters | lang stands for *lang*uage | |
| `<w:charset>` | `<charset>` in native html5 | charset | configure charset of this font | | |
| `<w:family>` | | family | configure family of this font | | |
| `<w:pitch>` | | character's pitch | configure pitch of characters that uses this font. | | | 
| `<w:font>` | font in native css | define a font | | |
| `<w:sig>` | | digital signature | encapsulate the digital signature of this font. | | | 
| `<w:panose1>` | | panose | configure the panose (with highest priority) | The lower number is it, the higher priority it has. | |
| `<w:altName>` | `alt` attribute in `<img>` tag in native html5 | alternative | use the alternative (according to the value specified in `w:val` attribute) **when** an element (such as an image) or things that used in an element (such as font) **can not be used or worked correctly**. | | |
| | | | | | | | 
| `<w:p>` | `<p>` | paragraph | A paragraph | notice that if an end-user only inputs an whitespace in .docx file, it will have `<w:p>` tag, the article `docx格式文档详解：xml解析并用html还原`[^2] says this situation. | 
| `<w:pStyle>` | | paragraph style | applies style (according to value of `w:val` attribute) to paragraph (that is inside `<w:p>` tag) | the style to apply is defined in `~/word/style.xml` file | |
| `<w:pPr>` | | paragraph property | property of a paragraph (that is inside `<w:p>` tag) in Microsoft Word file | Pr stands for *Pr*operty | |
| `<w:ind>` | | paragraph indentation | configure the indentation for this paragraph. | ind stands for *ind*entation | |
| | | | | | | | 
| `<w:b/>` | `<b>` and `<b/>` in native html5 | bold | determine the text is bold | | |
| `<w:spacing>` | spacing | settings about spacing between paragraphs | | |
| `<w:jc>` | | justification | settings about justification (alignment) of the paragraph | jc stands for *j*ustifi*c*ation | |
| | | | | | | | 
| `<w:r>` | | run | defines a run in Word | r stands for run | |
| | | | | | | | 
| `<w:rPr>` | | run property | configure property of a run (that is inside `<w:r>` tag) | | |
| `<w:rFonts>`| | run fonts | configure fonts of a run (that is inside `<w:rPr>` tag) | |
| | | | | | | | 
| `<w:sz>` | | size | defines a font size for standard characters (that is inside `<w:rPr>` tag) |  |
| `<w:szCs>` | | size | defines a font size for complex script characters (that is inside `<w:rPr>` tag) | Cs stands for *C*omplex *s*cript | |
| | | | | | | | 
| `<w:tbl>` | `<table>` | table | a table in Microsoft Word file | tbl stands for table | |
| `<w:tblPr>` | | table property | configure property (such as style and appearance) of a table (that is inside `<w:tbl>` tag) in Microsoft Word file | | |
| `<w:tblGrid>` | `<tr>` (first occurence) | table grid | defines a grid (header) of a table in Microsoft Word file | you can think of a grid like a header row ( consists of lots of columns ) in table | |
| `<w:gridCol>` | `<th>` | table grid column | defines a cell in a grid of a table in Microsoft Word file | | it must be inside `<w:tblGrid>` tag. Otherwise, the Word file is corrupted. |
| `<w:tr>`| `<tr>` | table row | a row of a table | t stands for *t*able, r stands *r*ow | |
| `<w:tc>` | `<td>` | table cell | an cell of a table | c stands for *c*ell | |
| `<w:tcW>` | | table cell width | determines the width of the cell of a table | W stands for *w*idth | |
| `<w:tcPr>` | | table cell property | configure property of a table cell (that is inside `<w:tc>` tag) | including width and grid span | |
| `<w:tblStyle>` | | table style | applies style (according to value of `w:val` attribute) to paragraph (that is inside `<w:tbl>` tag) | the style to apply is defined in `~/word/style.xml` file | |
| | | | | | | | 
| `<w:sectPr>` | | sect property | configure property of a sect | sect stands for section | |
| `<w:pgSz>` | | page size | configures a page size (that is inside `<w:sectPr>` tag) | pg stands for *p*a*g*e | |
| `<w:pgMar>` | | page margin | configures a page margin (that is inside `<w:sectPr>` tag) | Mar stands for *Mar*gin | |
| `<w:col>` | | columns in section | add columns in section (that is inside `<w:sectPr>` tag) | | |
| `<w:docGrid>` | | document grid | add document grid (that is inside `<w:sectPr>` tag) | | |
| | | | | | | | 
| `<w:tabs>` | | many tabs | define lots of a tab stop you may see lots of | you may see one or more `<w:tab>` tag inside `<w:tabs>` tag. | | 
| `<w:tab>` | | tab | define property of a tab stop by assign the value to its attributes. | | | 
| | | | | | | | 
| `<w:bookmarkStart>` | | bookmark start | defines a bookmark with start point | | One `<w:bookmarkStart>` tag must match one `<w:bookmarkEnd>` tag. Otherwise, the file is corrupted. | 
| `<w:bookmarkEnd>` | | bookmark end | defines a bookmark with end point to enclose a bookmark | | Same as above | 
| | | | | | | | 
| `<w:listDef>` | | list definition | defines a list with specific id for style | | |
| `<w:lsid>` | | list style id | assign the value of `w:val` attribute to id of list style to determine which style will be used | the id is defined in `~/word/style.xml` | |
| `<w:lvl>` | | list level | defines a level of list | lvl stands for *l*e*v*e*l* | |
| `<w:plt>` | | picture list type (exactly to say, list pattern type in modern version of Word) | it describes the complexity or structure of the list definition | | |   
| `<w:tmpl>` | | template | it configure the what template will be used | <ol><li>tmpl stands for *t*e*mpl*ate</li><li>It accords to value of `W:val` attribute.</li><li>The template that will be used must be prefined (usually is predefined in `~/word/style.xml` or `~/word/template.xml`</li></ol> | | 
| `<w:start>` | | start | configure starting value for the numbering sequence at this list level | | It's only relevant when the <w:numFmt> (number format) for this level is set to a numbering style (like decimal, upperRoman, lowerLetter, etc.). |
| `<w:numFmt>` | | number formatting | determines whether this level uses numbers or bullets, and the specific style  | | |
| `<w:bullet>` | | bullet formatting | same above | | |
| `<w:numPr>` | | number property | configure the property if it7 uses number formatting.  | | |
| `<w:suff>` | | suffix | specifies what character (if any) follows the number (e.g., a period, a hyphen, or a tab) | | |
| `<w:lvlText>` | | level text | defines the numbering format using placeholders (e.g., "%1." for first-level numbers) | | |
| `<w:lvlJc>` | | level justification | configures the justification of this level | | | 
| `<w:nfc>` | | Number Formatting Code | configures Number Formatting Code of this level | nfc stands for *N*umber *F*ormatting *C*ode | | 

###### xml attribute
###### attribute in `xmlns` namespace
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `xmlns:space` | | space | assign a value to determine how to deal with whitespace (i.e. ` `, `\t`,`\n`).

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

###### attribute in `<w:p>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:rsidR` | | revision id for run | assign the value of revision id for run  | rs stands for *r*evi*s*ion, R stands for *R*un | |
| `w:rsidRDefault` | | revision id for run default | assign the default value of revision id for run  | rs stands for *r*evi*s*ion, R stands for *R*un | |
| `w:rsidSect` | | revision id for section | assign the default value of revision id for section | rs stands for *r*evi*s*ion | |

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
| `w:start` | | start indentation | assign an positive value to specify start indentation of the paragraph, measured in twips.  |  it has meaning of `w:left` attribute | same as above |
| `w:right-chars` | | right indentation, characters unit | assign an positive integer to specify right indentation of the paragraph, measured in character units. | it is measured with its unit -- default character | it is deprecated, but not obsolete. At Microsoft Office 2019, it can recongize this attribute |
| `w:right` | | right indentation | assign an positive value to specify right indentation of the paragraph, measured in twips.  | its unit is twips | same as above |
| `w:end-chars` | | end indentation, characters unit | assign an positive value to specify end indentation of the paragraph, measured in character units. | it has meaning of `w:right-chars` attribute | However, it is implemented in later version of OOXML standard (ECMA-376, 2011), so Microsoft Word 2007 may not recognize this attribute. |
| `w:end` | | end indentation | assign an positive value to specify end indentation of the paragraph, measured in twips.  |  it has meaning of `w:right` attribute | same as above |
| `w:hang-chars` | | hang indentation, characters unit | assign an positive integer to specify hang indentation of the paragraph, measured in character units. | <ol><li>it is measured with its unit -- default character</li><li>For explanation about the term hang indentation, see `Appendix 4 -- terms`[^3]</li></ol>| |
| `w:hanging` | | hanging indentation | assign an positive value to specify hanging indentation of the paragraph, measured in twips.  | its unit is twips | |
| `w:first-line-chars` | | first-line indentation, characters unit | assign an value to specify first-line indentation of the paragraph, measured in twips.  | it is measured with its unit -- default character | It can be negative value, but when it is a negative value, there are some different effects.</br>See following cases.</br>Case 1:</br>When speficies a positive value, it indents the first line further to the right than the rest of the paragraph.</br>Case 2:</br>When specifics a negative value, it creates a `hanging indent` effect where the first line starts to the left of the subsequent lines. |
| `w:first-line` | | first-line indentation | assign an value to specify first-line indentation of the paragraph, measured in twips.  | its unit is twips |
same as above |
| `w:mirrorIndents` | | mirror indentation | the indentation should be mirrored.</br>Specifying to `"false"` indicates that the indentation will not be mirrored.</br>Otherwise, specifying to `"true"` indicates that it will be indented.</br>Default value is `"false"`. | | |
| etc | | | | | |


###### attribute in `<w:r>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:rsidR` | | revision id for run | assign the value of revision id for run  | rs stands for *r*evi*s*ion, R stands for *R*un | |
| `w:rsidRDefault` | | revision id for run default | assign the default value of revision id for run  | rs stands for *r*evi*s*ion, R stands for *R*un | |
| `w:rsidSect` | | revision id for section | assign the default value of revision id for section | rs stands for *r*evi*s*ion | |

###### attribute in `<w:tab>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | determines alignment or behavior of the tab stop. | This attribute is required. | |
| `w:pos` | | | determines position of the tab stop. | This attribute is required. | |
| `w:leader` | | leader character | determines leader character that will fill the space before the tab stop.  | This attribute is optional. | |

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
| w:space | | space | assign an value to determine the space between columns in section (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |

###### attribute in `<w:docGrid>`
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:linePitch | | vertical spacing | assign an value to determine the vertical spacing between grid lines in section (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| w:charSpace | | horizontal spacing | assign an value to determine horizontal spacing between grid lines in section (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| w:type | | type of document grid | assign an value to determine the type of document grid will be used in section (that is inside `<w:sectPr>` tag) | See `Appendix 2`[^2] for more information | |
| w:lineGrid | | number of line per grid | assign an value to determine number of line per grid in section (that is inside `<w:sectPr>` tag) | | its value must be positive number. |

###### attribute in `<w:tbW>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:w | | width | assign an value to determine the width of the cell (that is inside `<w:tc>` tag) | NOTES that its unit is not necessary twips (its unit is according to value of `w:type` attribute. See next record | |
| w:type | | type | assign an value to determine its unit | | |

###### attribute in `<w:pStyle>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:val | `value` in native html5 | assign an Guid as value that determines what style of 7the paragraph (that is inside `<w:p>` tag) will apply to | | |

###### attribute in `<w:tblStyle>`
Way to parsing it is similar to parsing `<w:pStyle>`.

| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:val | `value` in native html5 | assign an Guid as value that determines what style of the table (that is inside `<w:tbl>` tag) will apply to | | |

###### attribute in `<w:lsid>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:val | `value` in native html5 | assign an Guid as value that determines what style of the list (that is inside `<w:listDef>` tag) will apply to | | |

###### attribute in `<w:bookmarkStart>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:id` | `id` in native html5 | id of start point of bookmark | assign the id of start point of bookmark that in the tag | | |
| `w:name` | `name` in native html5 | name of start point of bookmark | assign the name of start point of bookmark that in the tag | | |

###### attribute in `<w:bookmarkEnd>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:id` | `id` in native html5 | id of end point of bookmark | assign the id of end point of bookmark that in the tag | | | 

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

###### attribute in `<w:lvlJc>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | | | assign the string as value to determine the alignment for this level | | |

##### examples and explanations
###### example 1 -- run
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

###### example 2 -- table

```
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

In this example, we can know that

1. In `<w:tr>`, it defines 

[^1]:[Prequisite Review 1 -- terms](https://github.com/40843245/XmlOfOffice/blob/main/Word/structure/Prequisite%20Review%201%20--%20terms.md)

[^2]:[Appendix 2 -- available options of attribute of tag in xml for Word](https://github.com/40843245/XmlOfOffice/blob/main/Word/structure/Appendix%202%20--%20available%20options%20of%20attribute%20of%20tag%20in%20xml%20for%20Word.md#appendix-2----available-options-of-attribute-of-tag-in-xml-for-word)

[^3]:[`docx格式文档详解：xml解析并用html还原`](https://juejin.cn/post/7166821284087595038)

[^4]:[9.2 Relationships in Office Open XML](https://ooxml.info/docs/9/9.2/)

[^5]:[ DocumentFormat.OpenXml.Linq.WNE class (MSDS API reference)](https://learn.microsoft.com/en-us/dotnet/api/documentformat.openxml.linq.wne?view=openxml-3.0.1) 
