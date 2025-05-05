# Appendix 1.1 -- xml tag in Excel
## Prequisite
See [`Prequisite.md`](https://github.com/40843245/OOXML/blob/main/Prequisite/Prequisite.md)

## Suggestion
See [`Suggestion.md`](https://github.com/40843245/OOXML/blob/main/Suggestion/Suggestion.md)

## NOTICE
See [`NOTICE.md`](https://github.com/40843245/OOXML/blob/main/NOTICE/NOTICE.md)

## Important concept
See [`important concept.md`](https://github.com/40843245/OOXML/blob/main/concept/important%20concept.md)

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
See [`OOXML/Word/structure/Appendix 1.1#namespace under xmlns namespace`](https://github.com/40843245/OOXML/blob/main/Word/structure/Appendix%201.1%20--%20xml%20tag%20in%20Document.md#namespace-under-xmlns-namespace)

### element and its attribute in xml tag in OOXML
#### about `mc` namespace
#### elements in `mc` namespace
| elements | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `<mc:AlternateContent>` | | acts like a container containing all informations about different versions or representations of certain content within the file | | It is required |

##### direct children in `<mc:AlternateContent>`
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

