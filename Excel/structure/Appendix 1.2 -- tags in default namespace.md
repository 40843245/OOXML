# Appendix 1.2 -- tags in default namespace
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

Optional elements in `~/xl/worksheets/sheet1.xml` under a `.xlsx` file.
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<sheetViews>` | | acts like a container that stores the information about these different viewing configurations for a single sheet. | a collection of `<sheetView>` | |

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
| `<xr:revisionPtr>` | revision *p*oin*t*e*r* | a pointer that relates to document revisions.  | | It is optional |
| `<sheets>` | | acts like a container containing all info about worksheet in the workbook.  | | It is required |
| `<calcPr/>` | *calc*ulation *pr*operties | defines and configures calculation properties  | | It is required |
| `<extLst>` | *ext*ensibility *l*i*st* | acts like a container containing all extensions | | It is required |

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
| `filterPrivacy` | | indicates whether personally identifiable information (PII) should be removed when the workbook is saved. | | The default value is `"false"` |

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

##### attributes of `<revisionPtr/>` element
| attributes | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `revIDLastSave` | *rev*ision *id*entifier one saved at last time.| indicates the revision identifier at the time the document was last saved.  | | |
| `documentId` | | unique identifier for the document. | For more details, see [Appendix 2.1 -- What's the design of documentId attribute of `<xr:revisionPtr>` tag?](https://github.com/40843245/OOXML/blob/main/Excel/structure/Appendix%202.1%20--%20What's%20the%20design%20of%20documentId%20attribute%20of%20%60%3Cxr%3ArevisionPtr%3E%60%20tag%3F.md) | |
| `xr6:coauthVersionLast` | version of document that is edited by last *co*-*auth*or.  | indicates the version of document that is edit by last co-author.  | | |
| `xr6:coauthVersionMax` | the *max*imum number of version of document among all *co*-*auth*ors' edit.  | indicates the maximum number of version of document among all co-authors' edit.  | | |
| `xr10:uidLastSave` | user identifier of last saved operation.  | indicates the user identifier of last saved operation.  | | |

### elements under `<sheets>` element
#### children in `<sheets>` element
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<sheet/>` | | info of a sheet | | |

##### attributes of `<sheet/>` element
| attributes | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `name` | | name of the sheet | | |
| `id` | | id of the sheet | | |
| `r:id` | *r*elationship of id | specifies relationship of id | It usually refers to a xml file under `~/xl/worksheets` directory | |

### elements under `<calcPr/>` element
#### attributes of `<calcPr/>` element
| attributes | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `calcId` | *calc*ulation id | specifies calculation id for revision tracking. | | |

### elements under `<extLst>` element
#### children in `<extLst>` element
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `ext` | *ext*ensibility | specifies a single extension. | | |

### elements under `<ext>` element
#### children in `<ext>` element
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `x15:workbookPr` | workbook *pr*operties | defines and configures workbook properties | | |

##### attributes of `<ext>` element
| attributes | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `uri` | URI | 128-bit guid of the single extension | | |

### elements under `<x15:workbookPr/>` element
#### children in `<x15:workbookPr/>` element
none

#### attributes of `<x15:workbookPr/>` element
| attributes | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `chartTrackingRefBase` | chart tracking *ref*erence base | determines whether enables a specific mode or feature for tracking the base of chart. | | |

### elements under `<vt:sheetViews>` element
#### children in `<vt:sheetViews>` element
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<sheetView>` | | usually contains the string value representing the title text. | | |

#### elements under `<sheetView>` element
#### children in `<sheetView>` element
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<pane>` | | defines the visual splitting of the worksheet. | | |
| `<selection>` | | specifies the selected cell or range of cells. There can be up to four <selection> elements, each corresponding to a pane in a split view | | |
| `<pivotSelection>` | | defines the selection within a PivotTable. | | |
| `<extLst>` | | acts like a container a container for future extensions to the <sheetView> element. | | |

##### attributes of `<pane/>` element
| attributes | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `xSplit` | | secifies the horizontal position of the split (in twips of point). A value of 0 indicates no horizontal split. If the pane is frozen, this attribute indicates the number of columns visible in the top pane.  |  | It is optional | 
| `ySplit`| | specifies the vertical position of the split (in a twips of a point). A value of 0 indicates no vertical split. If the pane is frozen, this attribute indicates the number of rows visible in the left pane. | | It is optional |
| `topLeftCell` | | specifies the location of the top-left visible cell in the bottom-right pane (when in left-to-right mode). | | <ol><li>It is optional</li><li>Its value MUST be in `A1` Annotation</li></ol> |
| `activePane` | | specifies which pane is active. | | It is optional |
| `state` | | specifies the state of the pane | | It is optional |

###### `<pane/>` -> `activePane`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"bottomLeft"` | | indicates the bottom-left pane is active (when both horizontal and vertical splits are applied). This value is also used when only a horizontal split is applied, dividing the pane into upper and lower regions, in that case, it specifies the bottom pane. | | |
| `"bottomRight"` | | indicates the bottom-right pane is active (when both horizontal and vertical splits are applied). | | |
| `"topLeft"` | | indicates the top-left pane is active (when both horizontal and vertical splits are applied). This value is also used when only a horizontal split is applied, dividing the pane into upper and lower regions; in that case, it specifies the top pane. Additionally, it's used when only a vertical split is applied, dividing the pane into right and left regions; in that case, it specifies the left pane. | | |
| `"topRight"` | | indicates the bottom-right pane is active (when both horizontal and vertical splits are applied). | | |
| `"bottomRight"` | | indicates the top-right pane is active (when both horizontal and vertical splits are applied). This value is also used when only a vertical split is applied, dividing the pane into right and left regions; in that case, it specifies the right pane. | | |

###### `<pane/>` -> `state`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<frozen>` | | specifies that the panes are frozen, but they were not split before being frozen. This means the split lines are at the edges of the visible area. | | |
| `<frozenSplit>` | | specifies that the panes are both split and frozen. | | |
| `<split>` | | specifies that the panes are split, but not frozen. The user can still adjust the split lines. | | |

### examples and explanation
#### example 1.1 -- workbook tag as root node in `~/xl/workbook.xml`
the root node of `~/xl/worbook.xml` under an Excel file.

```
<workbook
xmlns="http://schemas.openxmlformats.org/spreadsheetml/2006/main"
xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships"
xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
xmlns:x15="http://schemas.microsoft.com/office/spreadsheetml/2010/11/main"
xmlns:xr="http://schemas.microsoft.com/office/spreadsheetml/2014/revision"
xmlns:xr6="http://schemas.microsoft.com/office/spreadsheetml/2016/revision6"
xmlns:xr10="http://schemas.microsoft.com/office/spreadsheetml/2016/revision10"
xmlns:xr2="http://schemas.microsoft.com/office/spreadsheetml/2015/revision2"
mc:Ignorable="x15 xr xr6 xr10 xr2">
```

In above example, we can know that

+ the `xmlns` namespace targets to `http://schemas.openxmlformats.org/spreadsheetml/2006/main`, meaning that the default namespace uses Office Excel 2006 (according to `xmlns="http://schemas.openxmlformats.org/spreadsheetml/2006/main"`).
+ the `xmlns:r` namespace targets to `http://schemas.openxmlformats.org/officeDocument/2006/relationships`, meaning that the relationship uses Office Excel 2006 (according to `xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships"`).
+ the markup will be compatible to Office Excel 2006 (according to `xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"`).
+ specifies extensions version. The extensions that introduced in relates to Office Excel 2013 (according to `xmlns:x15="http://schemas.microsoft.com/office/spreadsheetml/2010/11/main"`).
+ specifies extensions version. The extension that relates to revision tracking features introduced in or around Excel 2016 (according to `xmlns:xr="http://schemas.microsoft.com/office/spreadsheetml/2014/revision"`).
+ for further revision tracking enhancements introduced in a later update of Excel 2016 or a subsequent version. (according to `xmlns:xr6="http://schemas.microsoft.com/office/spreadsheetml/2016/revision6")`.
+ for yet another set of revision tracking features, likely introduced in a later update of Excel 2016 or a subsequent version (according to `xmlns:xr10="http://schemas.microsoft.com/office/spreadsheetml/2016/revision10"`)
+ for revision tracking features introduced around Excel 2016. (according to `xmlns:xr2="http://schemas.microsoft.com/office/spreadsheetml/2015/revision2"
`).
+ it indicates that the xml preprocessor will ignores them.
    - x15
    - xr
    - xr6
    - x10
    - xr2

(according to `mc:Ignorable="x15 xr xr6 xr10 xr2"`).



#### exaple 1.1 -- sheets
a part of xml content of `~/xl/worbook.xml` under an Excel file.

```
<sheets>
  <sheet name="工作表1" sheetId="1" r:id="rId1"/>
  <sheet name="動漫或動畫等角色介紹" sheetId="2" r:id="rId2"/>
  <sheet name="動漫或動畫等介紹" sheetId="3" r:id="rId3"/>
</sheets>
```

In above example, we can know that

+ there are three worksheets in the workbook at current.

Respectively named `工作表1`, `動漫或動畫等角色介紹`, `動漫或動畫等介紹`.

The first worksheet named `工作表1` refers to `~/xl/worksheets/sheet1.xml` by default.

While the second worksheet named `動漫或動畫等角色介紹` refers to `~/xl/worksheets/sheet2.xml` by default.

Similarly the third worksheet named `動漫或動畫等介紹` refers to `~/xl/worksheets/sheet3.xml` by default.

#### exaple 3.1 -- workbook properties
```
<workbookPr date1904="1" showObjects="all" saveExternalLinkValues="1" codeName="ThisWorkbook"/>
```

In above example, we can know that

+ The workbook uses the 1904 date system.
+ All objects are displayed
+ External link values are saved.
+ The VBA codename for the workbook is "ThisWorkbook".
