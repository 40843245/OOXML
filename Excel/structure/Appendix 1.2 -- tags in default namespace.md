.# Appendix 1.2 -- tags in default namespace
## default namespace
### elements that are children in default namespace
Required elements in `~/DocProps/app.xml` under a `.xlsx` file.

| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<Properties>` | | acts like a container containing all properties in Metadata. | | |
| `<Application>` | | the application used when the document is created. | | |
| `<DocSecurity>` | | determines whether the document has security policies. | | |
| `<ScaleCrop>` | | determines whether the drawing object in the document can be scaled or cropped. | | |
| `<Company/>` | | compnay or organization when the document is created. | | |
| `<LinksUpToDate>` | | determines whether the link in the document is up to date. | | |
| `<SharedDoc>` | | determines whether the document can be shared. | | |
| `<HyperlinksChanged>` | | determines whether hyperlink in the document has been changed. | | |
| `<HeadingPairs>` | | defines pairs of headings and the count of parts under those headings. | | |
| `<TitlesOfParts>` | | ists the titles of the individual parts of the document, in this case, worksheets. | | |

Required elements in `~/xl/workbook.xml` under a `.xlsx` file.
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<workbook>` | | The root element in `workbook`.xml | | |

Required elements in `~/xl/worksheets/sheet1.xml` under a `.xlsx` file.
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<worksheet>` | | The root element in `sheet1.xml` | | |
| `<sheetData>` | | a cell table that holds the actual data displayed in the spreadsheet. | | |

Optional elements in `~/xl/worksheets/sheet1.xml` under a `.xlsx` file.
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<sheetViews>` | | acts like a container that stores the information about these different viewing configurations for a single sheet. | a collection of `<sheetView>` | |
| `<sheetView>` | | defines a view for a single sheet | | |

### elements under `<HeadingPairs>` element
#### children in `<HeadingPairs>` element
| children in `<HeadingPairs>` element | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:vector>` | | defines a vector for the heading of the Worksheet and acts like a container containing all properties about the vector. | | |

#### elements under `<vt:vector>` element
##### children in `<vt:vector>` element
| children in `<vt:vector>` element | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:variant>` | | acts like a container containing a single value within the vector. | | |

##### elements under `<vt:variant>` element
###### children in `<vt:variant>` element
| children in `<vt:variant>` element | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:lpwstr>` | | usually contains the string value representing the heading text. | | |
| `<vt:i4>` | | typically holds the integer value representing the count associated with the heading. | | |

### elements under `<TitlesOfParts>` element
#### children in `<TitlesOfParts>` element
| children in `<TitlesOfParts>` element | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:vector>` | | defines a vector for the title of the Worksheet and acts like a container containing all properties about the vector. | | |

#### elements under `<vt:vector>` element
##### children in `<vt:vector>` element
| children in `<vt:vector>` element | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:variant>` | | acts like a container containing a single value within the vector. | | |

##### elements under `<vt:variant>` element
###### children in `<vt:variant>` element
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:lpwstr>` | | usually contains the string value representing the title text. | | |

### elements under `<workbook>` element
#### children in `<workbook>` element
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<fileVersion/>` | | indicates the file version in the workbook. | | It is required |
| `<workbookPr/>` | workbook *pr*operties | specifies various document-level settings and properties that apply to the entire workbook. | | It is optional |

##### attributes of `<fileVersion/>` element
| attributes | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `appName` | | the app name in the last edit. | | |
| `lastEdited` | | last edited id | | |
| `lowestEdited` | | earliest edited id | | |
| `rupBuild` | *r*oll*up* build | *r*oll*up* build id | | |

##### attributes of `<workbookPr/>` element
| attributes | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `date1904` | | determines that uses 1904 date system | | The default value is `"false"` |
| `showObjects` | | determines how graphic objects are displayed. | | The default value is `"all"` |
| `saveExternalLinkValues` | | determines to save external link values | | The default value is `"true"` |
| `updateLinks` | | controls how external links are updated when the workbook is opened.  | | The default value is `"userSet"` |
| `codeName` | | specifies the programmatic identifier (codename) for the workbook, often used in VBA (Visual Basic for Applications) code. | | |
| `backupFile` | | indicates whether a backup copy of the workbook is created upon saving.  | | The default value is `"false"` |
| `hidePivotFieldList` | | determines if the field list for PivotTables is hidden.  | | The default value is `"false"` |
| `autoCompressPictures` | | determines if the field list for PivotTables is hidden.  | | The default value is `"false"` |
| `refreshAllConnections ` | | indicates whether all data connections in the workbook should be refreshed when the workbook is opened. | | |
| `defaultThemeVersion` | | specifies the version of the default theme applied to the workbook.  | | The default value is `"false"` |
| `checkCompatibility ` | | determines whether a compatibility check is performed when saving the workbook to older file formats.  | | The default value is `"false"` |
| `filterPrivacy` | |Indicates whether personally identifiable information (PII) should be removed when the workbook is saved. | | The default value is `"false"` |

###### `<workbookPr/>` -> `date1904`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"true"` | | use 1904 date system | the first date is January 2, 1904 | |
| `"false"` | | use 1900 date system instead of 1904 date system | the first date is January 1, 1900 | |

###### `<workbookPr/>` -> `showObjects`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"all"` | | show all objects | | |
| `"placeholders"` | | show placeholders for objects | | |
| `"none"` | | show none for objects | | |

###### `<workbookPr/>` -> `saveExternalLinkValues`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"true"` | | save external link values  | | |
| `"false"` | | NOT save external link values | | |

###### `<workbookPr/>` -> `updateLinks`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"userSet"` | | The user is prompted to update links. | | |
| `"never"` | | Links are never updated. | | |
| `"always"` | | Links are updated without prompting. | | |

###### `<workbookPr/>` -> `updateLinks`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"userSet"` | | The user is prompted to update links. | | |
| `"never"` | | Links are never updated. | | |
| `"always"` | | Links are updated without prompting. | | |

###### `<workbookPr/>` -> `backupFile`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"true"` | | Creates a backup file. | | |
| `"false"` | | NOT create a backup. | | |

###### `<workbookPr/>` -> `hidePivotFieldList`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"true"` | | Hides the PivotTable field list. | | |
| `"false"` | | Shows the PivotTable field list. | | |

###### `<workbookPr/>` -> `autoCompressPictures`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"true"` | | Refreshes all connections | | |
| `"false"` | | NOT automatically refreshes all connections | | |

###### `<workbookPr/>` -> `refreshAllConnections`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"true"` | | Automatically compresses pictures. | | |
| `"false"` | | NOT automatically compresses pictures. | | |

###### `<workbookPr/>` -> `checkCompatibility`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"true"` | |  Performs a compatibility check. | | |
| `"false"` | | NOT compatibility check. | | |

### examples and explanation
#### exaple 1
```
<workbookPr date1904="1" showObjects="all" saveExternalLinkValues="1" codeName="ThisWorkbook"/>
```

+ The workbook uses the 1904 date system.
+ All objects are displayed
+ External link values are saved.
+ The VBA codename for the workbook is "ThisWorkbook".
  
### elements under `<worksheet>` element
### elements under `<workbook>` element
### elements under `<workbook>` element
