# Appendix 1.1 -- xml tag in Excel
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

> [!IMPORTANT]
> In OOXML,
>
> For those value of attribute that needs to be specified with a string containing a boolean value (i.e. `"true"` or `"false"`),
>
> + `"0"` is equivalent to `"false"`
> 
> + `"1"` is equivalent to `"true"`

### processing instruction
See `Appendix 1 -- tags in xml`[^3]

But in OOXML, there are many ways added to process a file that will be parse with OOXML preprocessor.

I just list some of them that commonly seen in Excel file.

### namespace declaration
| namespace declaration | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `<workbook>` | | The root element in `workbook`.xml | | |
| `<worksheet>` | | The root element in `sheet1.xml` | | |

### namespace about `xmlns` namespace
| namespace about `xmlns` namespace | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `xmlns` | | | is used to declare a default namespace for an element and its descendants. Elements without a prefix within this scope belong to this namespace | | |

### namespace under `xmlns` namespace
| namespace under `xmlns` namespace | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `r` | *R*elationship | it specifies which relationship will be used. | | | 
| `m` | *M*ath | it specifies which tools about math (its functionalities contain `Equation`) will be used. | | | 
| `ignorable` | ignorable | it specifies which namespace declaration in this tag will be ignored. | it must be string, seperated by exactly one space. (To represent that many of them will be ignored.) | | 
| `w` | *W*ordProcessingML | assign a value to it determine which WordprocessingML elements is used. | | |
| `w14` | *W*ordProcessingML | assign a value to it determine which WordprocessingML (with version id 14) elements is used. | | |
| `w15` | *W*ordProcessingML | assign a value to it determine which WordprocessingML (with version id 15) elements is used. | | |
| `w16cid` | *W*ordProcessingML *C*ontent *Id*entifiers | assign a value to it determine which Content Identifiers of WordprocessingML (with version id 16) elements is used. | | |
| `w16se` | *W*ordProcessingML *S*ymbol *E*xtensibility | assign a value to it determine which Symbol Extensibility of WordprocessingML (with version id 16) elements is used. | | |
| `wpg` | *W*ordProcessingML *G*rouping  | assign a value to it determine which Symbol Extensibility of WordprocessingML Grouping is used. | | |
| `wpi` | *W*ordProcessingML *I*nk  | assign a value to it determine which Symbol Extensibility of WordprocessingML Ink is used. | At intial release of WordprocessingML Ink (in Microsoft Office 2010), its namespace is named as `wpi` but it is named as `aink` at later release. | |

### element and its attribute in xml tag in OOXML
#### about `mc` namespace
#### elements in `mc` namespace
| elements | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `<mc:AlternateContent>` | | acts like a container containing all informations about different versions or representations of certain content within the file | | It is required |

##### children in `<mc:AlternateContent>`
| elements | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `<mc:Choice>` | | acts like a container to present one of the alternative content options. | | It is required |
| `<mc:Fallback>` | | content that should be used by applications that do not understand any of the `<mc:Choice>` elements | | It is optional |

#### about `xr` namespace
#### elements in `xr` namespace
| elements | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `<xr:uid>` | | a unique identifier for a particular extended reference. | | |
| `<xr:sheetXluid>` | | refers to a unique identifier for a sheet. | | |
| `<xr:tabId>` | |  identifies a specific tab within a sheet. | | |
| `<xr:ref>` | |  defines the cell or range that the extended reference applies to.| | |
| `<xr:formula>` | | might contain a formula associated with the extended reference. | | |
| `<xr:fmlaType>` | *f*or*m*u*la* | specifies the type of formula. | | |
| `<xr:name>` | |  might provide a name for the extended reference. | | |
| `<xr:valt>` | *val*ue *t*ype | indicates the data type of the referenced value. | | |
| `<xr:extLst>` | *ext*ension *l*i*st* | acts like a container for future extensions to the extended reference. | |
| `<xr:ext>` | *ext*ension | defines a specific extension within the `extLst` | | |
| `<xr:ajt>` | *a*d*j*us*t*ment  | are related to adjustment values and are available in Office 2016 and later. | | |
| `<xr:ajtx>` | *a*d*j*us*t*ment *ext*ension *l*i*st* | same as above | | but is used in extension pack. |

