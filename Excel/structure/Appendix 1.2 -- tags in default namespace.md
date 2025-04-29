# Appendix 1.2 -- tags in default namespace
## default namespace
### elements that are children in default namespace
+ Required elements in `~/DocProps/app.xml` under a `.xlsx` file.

| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<Properties>` | | acts like a container containing all properties in Metadata. | | |

+ Required elements in `~/xl/workbook.xml` under a `.xlsx` file.

| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<workbook>` | | The root element in `workbook`.xml | | |

+ Required elements in `~/xl/worksheets/sheet1.xml` under a `.xlsx` file.

| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<worksheet>` | | The root element in `~/xl/worksheets/sheet1.xml | | |

+ Required elements in `~/xl/sharedStrings.xml` under a `.xlsx` file.

| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<sst>` | *s*hared *s*tring *t*ext | The root element in `~/xl/sharedStrings.xml` | | |

+ Required elements in `~/xl/styles.xml` under a `.xlsx` file.

| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<styleSheet>` | *s*hared *s*tring *t*ext | The root element in `~/xl/styles.xml` | | |

## Required elements in `~/DocProps/app.xml` under a `.xlsx` file.
### elements under `<Properties>` element
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<Properties>` | | acts like a container containing all properties in Metadata. | | |

#### children in `<Properties>` element
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<Application>` | | the application used when the document is created. | | |
| `<DocSecurity>` | | determines whether the document has security policies. | | |
| `<ScaleCrop>` | | determines whether the drawing object in the document can be scaled or cropped. | | |
| `<Company/>` | | compnay or organization when the document is created. | | |
| `<LinksUpToDate>` | | determines whether the link in the document is up to date. | | |
| `<SharedDoc>` | | determines whether the document can be shared. | | |
| `<HyperlinksChanged>` | | determines whether hyperlink in the document has been changed. | | |
| `<HeadingPairs>` | | defines pairs of headings and the count of parts under those headings. | | |
| `<TitlesOfParts>` | | ists the titles of the individual parts of the document, in this case, worksheets. | | |

### elements under `<HeadingPairs>` element
#### children in `<HeadingPairs>` element
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:vector>` | | defines a vector for the heading of the Worksheet and acts like a container containing all properties about the vector. | | |

#### elements under `<vt:vector>` element
##### children in `<vt:vector>` element
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:variant>` | | acts like a container containing a single value within the vector. | | |

##### elements under `<vt:variant>` element
###### children in `<vt:variant>` element
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:lpwstr>` | | usually contains the string value representing the heading text. | | |
| `<vt:i4>` | | typically holds the integer value representing the count associated with the heading. | | |

### elements under `<TitlesOfParts>` element
#### children in `<TitlesOfParts>` element
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:vector>` | | defines a vector for the title of the Worksheet and acts like a container containing all properties about the vector. | | |

#### elements under `<vt:vector>` element
##### children in `<vt:vector>` element
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:variant>` | | acts like a container containing a single value within the vector. | | |

##### elements under `<vt:variant>` element
###### children in `<vt:variant>` element
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:lpwstr>` | | usually contains the string value representing the title text. | | |

## Required elements in `~/xl/workbook.xml` under a `.xlsx` file.
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

### elements under `<vt:sheetViews>`->`<sheetView>` element
#### children in `<vt:sheetViews>`->`<sheetView>` element
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<pane>` | | defines the visual splitting of the worksheet. | | |
| `<selection>` | | specifies the selected cell or range of cells. There can be up to four `<selection>` elements, each corresponding to a pane in a split view | | |
| `<pivotSelection>` | | defines the selection within a `PivotTable`. | | |
| `<extLst>` | | acts like a container a container for future extensions to the `<sheetView>` element. | | |

### elements under `<pane/>` element
#### attributes of `<pane/>` element
| attributes | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `xSplit` | | secifies the horizontal position of the split (in twips of point). A value of 0 indicates no horizontal split. If the pane is frozen, this attribute indicates the number of columns visible in the top pane.  |  | It is optional | 
| `ySplit`| | specifies the vertical position of the split (in a twips of a point). A value of 0 indicates no vertical split. If the pane is frozen, this attribute indicates the number of rows visible in the left pane. | | It is optional |
| `topLeftCell` | | specifies the location of the top-left visible cell in the bottom-right pane (when in left-to-right mode). | | <ol><li>It is optional</li><li>Its value MUST be in `A1` Annotation</li></ol> |
| `activePane` | | specifies which pane is active. | | It is optional |
| `state` | | specifies the state of the pane | | It is optional |

##### `<pane/>` -> `activePane`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"bottomLeft"` | | indicates the bottom-left pane is active (when both horizontal and vertical splits are applied). This value is also used when only a horizontal split is applied, dividing the pane into upper and lower regions, in that case, it specifies the bottom pane. | | |
| `"bottomRight"` | | indicates the bottom-right pane is active (when both horizontal and vertical splits are applied). | | |
| `"topLeft"` | | indicates the top-left pane is active (when both horizontal and vertical splits are applied). This value is also used when only a horizontal split is applied, dividing the pane into upper and lower regions; in that case, it specifies the top pane. Additionally, it's used when only a vertical split is applied, dividing the pane into right and left regions; in that case, it specifies the left pane. | | |
| `"topRight"` | | indicates the bottom-right pane is active (when both horizontal and vertical splits are applied). | | |
| `"bottomRight"` | | indicates the top-right pane is active (when both horizontal and vertical splits are applied). This value is also used when only a vertical split is applied, dividing the pane into right and left regions; in that case, it specifies the right pane. | | |

##### `<pane/>` -> `state`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<frozen>` | | specifies that the panes are frozen, but they were not split before being frozen. This means the split lines are at the edges of the visible area. | | |
| `<frozenSplit>` | | specifies that the panes are both split and frozen. | | |
| `<split>` | | specifies that the panes are split, but not frozen. The user can still adjust the split lines. | | |

## Required elements in `~/xl/worksheets/sheet1.xml` under a `.xlsx` file.
### elements under `<worksheet>` element
#### children in `<worksheet>` element
| elements | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<dimension>` | | dimension. | |
| `<sheetViews>` | | serves as a container containg views for sheets. | |
| `<sheetFormatPr>` | sheet *format*ting *pr*operties | configures sheet formatting properties | |
| `<cols>` | | acts as a container containing all columns | |
| `<sheetData>` | | serves like a container containing all the row and cell data within a worksheet. | | |

### elements under `<dimension/>` element
#### attributes of `<dimension/>` element
| attributes | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `ref` | | the reference of the used range (in A1 annotation) | | |

### elements under `<worksheet>`->`<sheetViews>` element
#### children in `<worksheet>`->`<sheetViews>` element
| elements | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `<sheetView>` | | acts as a container containing a view for a sheet and configures the view. | | |

### elements under `<sheetView>` element
#### children in `<sheetView>` element
| elements | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `<selection>` | | stores information about selection | | |

#### attributes of `<sheetView>` element
| attributes | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `topLeftCell` | | specifies the cell that should appear in the top-left corner of the visible portion of the worksheet when it's opened. | | |
| `workbookViewId` | | links this specific sheet view to a workbook view setting. | zero-based index | A workbook can have multiple view settings (e.g. for different window sizes, zoom levels, etc.) |

### elements under `<selection>` element
#### attributes of `<selection>` element
| attributes | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `activeCell` | | stores active cell within the current selection. | | |
| `sqref` | *s*e*q*uence of *ref*erence | specifies a sequence of cell or range references. | This allows for non-contiguous selections or multiple distinct areas to be targeted by a single element within the OOXML structure. | |

> [!CAUTION]
> `sqref` does NOT stand for `single-range reference`.
>
> It stands for `sequence of references`.

> [!IMPORTANT]
> However, `sequence of references` can contain `single-range reference`.

See [Google Gemini's answer -- What does `sqref` attribute stand for in OOXML?](https://github.com/40843245/OOXML/blob/main/Excel/tags/abbreviation/sqref/What%20does%20%60sqref%60%20attribute%20stand%20for%20in%20OOXML%3F.md) for more explanation.

### elements under `<workbookViewId>` element
#### children in `<workbookViewId>` element
| elements | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `<pane>` | | defines the visual splitting of the worksheet. | | |
| `<selection>` | | specifies the selected cell or range of cells. | | <ul><li>A `<sheetView>` can have multiple `<selection>` elements, especially in collaborative scenarios or if multiple ranges were selected.</li><li>Attributes include the active cell, the selected range, and the pane it applies to.</li></ul>|
| `<pivotSelection>` | | is specific to `PivotTable` views | | It stores information about the selected areas within a `PivotTable`. |
| `<viewPr>` | view *pr*operties | contains view properties for the sheet, such as whether gridlines are visible, whether row and column headers are displayed, and the state of outline symbols. | | |
| `<extLst>` | | acts like a container containing one or more `<ext>` | It allows applications to add custom elements to the `<sheetView>` element without breaking compatibility with applications that don't understand these extensions. | |

### elements under `<dimension/>` element
#### attributes of `<dimension/>` element
| attributes | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `ref` | | the reference of the used range (in A1 annotation) | | |

### elements under `<col>` element
#### attributes in `<col>` element
| attributes | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `min` | | starting column number | | |
| `max` | | ending column number | | |
| `customWidth` | | determines that the width is custom (i.e. should NOT be automatically adjusted ) | | |
| `bestFit` | | determines that to do best fit for width (i.e. should automatically adjust the width of the column to fit the widest content within them.) | | |
| `width` | | explicity specifies the width of the column | | |

##### `<col>`->`customWidth`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"true"` | | the column should NOT be automatically adjusted | | |
| `"false"` | | the column should be automatically adjusted | | |

##### `<col>`->`bestFit`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"true"` | | should automatically adjust the width of the column to fit the widest content within them. | | |
| `"false"` | | should NOT automatically adjust the width of the column to fit the widest content within them | | |

### elements under `<sheetFormatPr/>` element
#### attributes of `<sheetFormatPr/>` element
| attributes | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `defaultRowHeight` | default row height | specifies default row height for all rows. | | |
| `x14ac:dyDescent` | *dy*namic descent | specifies a dynamic descent of how many pixels for bottom-aligned text in the rows of the sheet. | Its unit is in pixels.| |

### elements under `<sheetData>` element
#### children in `<sheetData>` element
| elements | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `<row>` | | defines a row and configures its properties. | | |

### elements under `<row>` element
#### children in `<row>` element
| elements | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `<c>` | *c*ell | specifies a cell in the row. | | |

#### attributes in `<row>` element
| attributes | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `r` | | specifies row index | first-index based | |
| `spans` | | specifies spans (i.e. the range of non-empty columns for the block of rows to which the current row belongs) | seperated by `:`. | |
| `s` | | specifies style index to refes to a style defined in the `<styleSheet>` part | zero-based index | The default value is `"0"`|
| `customFormat` | | determines whether some formatting has been applied directly to the row, overriding the default style. | | The default value is `"false"` |
| `ht` | row *h*eigh*t* | specifies the height of the row in points. | | There's no margin padding on row height. |
| `hidden` | | determines whether the row is hidden | This could be due to a collapsed outline or manual hiding | The default value is `"false"` |
| `customHeight` | | determines whether the row height has been explicitly set and should NOT be automatically adjusted. | | The default value is `"false"` |
| `outlineLevel` | | specifies the outline level of the row when outlining is enabled. | | The default value is `"0"` |
| `collapsed` | | determines whether rows with an outline level one greater than the current row should be in a collapsed state and thus hidden by the outline. | | The default value is `"false"` |
| `thickTop` | | <ul><li>When specified to `"true"` and the attribute `customHeight` is also specified to `"false"`,</br>it implies that the row height might have been adjusted higher by 0.75 points</br>due to a thick top border on any cell in the row or a thick bottom border on any cell in the row above.</li><li>Otherwise, the row height MUST NOT been adjusted.</li></ul> | | The default value is `"false"` |
| `thickBot` | thick *bot*tom | <ul><li>When specified to `"true"`,</br>it indicates that at least one cell in the row has a medium or thick bottom border, or any cell in the row directly below has a thick top border.</br>This can also influence the automatic row height adjustment when the attribute `customHeight` is specified to `"false"`.</li><li></li></ul>| | The default value is `"false"` |
| `ph` | show *ph*onetic | determines whether phonetic information associated with the cells in this row should be displayed (if available). | | The default value is `"false"` |

##### `<row>`->`customFormat`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"true"` | | rows with an outline level one greater than the current row should be in a collapsed state | | |
| `"false"` | | rows with an outline level one greater than the current row should NOT be in a collapsed state | | |

##### `<row>`->`hidden`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"true"` | | the row is hidden. | | |
| `"false"` | | the row is NOT hidden. | | |

##### `<row>`->`customHeight`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"true"` | | the row height should NOT be automatically adjusted | | |
| `"false"` | | the row height should be automatically adjusted | | |

##### `<row>`->`collapsed`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"true"` | | the row height should NOT be automatically adjusted | | |
| `"false"` | | the row height should be automatically adjusted | | |

##### `<row>`->`thickTop`
See description above.

##### `<row>`->`thickBot`
See description above.

##### `<row>`->`ph`
| values | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `"true"` | | phonetic information associated with the cells in this row should be displayed (if available) | | |
| `"false"` | | phonetic information associated with the cells in this row should NOT be displayed. | | |

### elements under `<c>` element
#### children in `<c>` element
| elements | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `v` | *v*alue | given index, the value found (by index) in shared string table.  |  |  |

#### attributes in `<c>` element
| attributes | meaning | description | notes | notice
| :-- | :-- | :-- | :-- | :-- |
| `r` | *r*eference | indicates the cell references which cell in worksheet. | in A1 annotation | |
| `t` | *t*ype | stores type of actual data | NOT type of displayed text. | |

## Required elements in `~/xl/sharedStrings.xml` under a `.xlsx` file.
### elements under `<sst>` element
#### children in `<sst>` element
| elements | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `<si>` | *s*tring *i*ndex | contains an `innerHTML` value that is mapped by the given index (the number between `<v>` and `</v>` tag). | | |

### elements under `<si>` element
#### children in `<si>` element
| elements | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `<t>` | *t*ext | the plain text | | |

## Required elements in `~/xl/styles.xml` under a `.xlsx` file
### elements under `<styleSheet>` element
#### children in `<styleSheet>` element
| elements | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `<fonts>` | | acts like a container containing all fonts. | | |
| `<fills>` | | acts like a container containing all fillings. | | |
| `<borders>` | | acts like a container containing all borders. | | |
| `<cellStyleXfs>` | | acts like a container containing all cell style formats. | defines named styles. | |
| `<cellXfs>` | | acts like a container containing all all cell style formats. | deals with the specific formatting of each cell. | |
| `<extLst>` | | acts like a container containing all extensions. | | |

> [!IMPORTANT]
> DON'T be confused with `<cellStyleXfs>` and `<cellXfs>`.

### elements under `<fonts>` element
#### children in `<fonts>` element
| elements | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `<font>` | | defines a font and servers as a container that specifies the properties inside this tag. | | |

#### attributes in `<fonts>` element
| attributes | meaning | description | notes | notice
| :-- | :-- | :-- | :-- | :-- |
| `count` | | indicates the number of direct children do we have in this tag. | | |
| `x14ac:knownFonts` | known fonts | suggests that how many are there the defined fonts that is `known` or standard font that the application might handle more efficiently | | |

### elements under `<font>` element
#### children in `<font>` element
| elements | meaning | description | notes | notice 
| :-- | :-- | :-- | :-- | :-- |
| `<name>` | | gives the font the name | | |
| `<sz>` | *s*i*z*e | specifies font size for non-complex script characters | | |
| `<color>` | | specifies the color of font | | |
| `<family>` | | specifies the family of the font | | |
| `<scheme>` | | specifies the font scheme | | |
| `<b/>` | | specifies the font is bold | | |
| `<i/>` | | specifies the font is italic | | |
| `<u/>` | | specifies the font is underlined | | |
| `<strike/>` | | specifies the font is strikethrough | | |
| `<outline/>` | | specifies the font is displayed as an outline | | |
| `<shadow/>` | | specifies the font should have a shadow effect | | |
| `<condense/>` | | specifies the font should be condensed ( narrower). | | |
| `<extend/>` | | specifies the font should be extended (wider).  | | |

### elements under `<name>` element
#### attributes in `<name>` element
| attributes | meaning | description | notes | notice
| :-- | :-- | :-- | :-- | :-- |
| `val` | | gives the font the name | | |

### elements under `<sz>` element
#### attributes in `<sz>` element
| attributes | meaning | description | notes | notice
| :-- | :-- | :-- | :-- | :-- |
| `val` | | specifies font size for non-complex script characters | | |

### elements under `<color>` element
#### attributes in `<color>` element
| attributes | meaning | description | notes | notice
| :-- | :-- | :-- | :-- | :-- |
| `val` | | specifies color of font | | |

### elements under `<family>` element
#### attributes in `<family>` element
| attributes | meaning | description | notes | notice
| :-- | :-- | :-- | :-- | :-- |
| `val` | | specifies font family | | |

##### `<family>`->`val`
| values | meaning | description | notes | notice
| :-- | :-- | :-- | :-- | :-- |
| `"0"` | | Unknown or default | | |
| `"1"` | | serif | | |
| `"2"` | | sans-serif | | |
| `"3"` | | fixed-pitch | | |
| `"4"` | | Script | | |
| `"5"` | | Decorative | | |

### elements under `<scheme>` element
#### attributes in `<scheme>` element
| attributes | meaning | description | notes | notice
| :-- | :-- | :-- | :-- | :-- |
| `val` | | specifies font scheme | | |

##### `<scheme>`->`val`
| values | meaning | description | notes | notice
| :-- | :-- | :-- | :-- | :-- |
| `"major"` | | Major font (typically used for headings) | | |
| `"minor"` | | Minor font (typically used for body text) | | |

### elements under `<b/>` element
presence of `</b>` signifies bold formatting.

### elements under `<i/>` element
presence of `<i/>` signifies italic formatting.

### elements under `<u/>` element
presence of `<u/>` signifies underline formatting.

### `<u/>`->`val`
| values | meaning | description | notes | notice
| :-- | :-- | :-- | :-- | :-- |
| `"single` | | Major font (typically used for headings) | | |
| `"double"` | | Minor font (typically used for body text) | | |
| `"singleAccounting"` | | Minor font (typically used for body text) | | |
| `"doubleAccounting."` | | Minor font (typically used for body text) | | |

### elements under `<i>` element
presence of `<u/>`  signifies underline formatting

### elements under `<strike/>` element
that indicates the font should be displayed as an outline. Its presence signifies outline formatting

### elements under `<shadow/>` element
Its presence signifies shadow formatting.

### elements under `<extend/>` element
Its presence signifies extend formatting.

### elements under `<fills>` element
#### children in `<fills>` element
| elements | meaning | description | notes | notice
| :-- | :-- | :-- | :-- | :-- |
| `<fill>` | | defines a filling and servers as a container that specifies the properties in this tag. | | |

#### attributes in `<fills>` element
| attributes | meaning | description | notes | notice
| :-- | :-- | :-- | :-- | :-- |
| `count` | | specifies the number of fillings | | |

### elements under `<fill>` element
#### children in `<fill>` element
| elements | meaning | description | notes | notice
| :-- | :-- | :-- | :-- | :-- |
| `<patternFill>` | | defines the pattern to fill | | |

#### attributes in `<fill>` element
none

### elements under `<patternFill>` element
#### children in `<patternFill>` element
none

#### attributes in `<patternFill>` element
| attributes | meaning | description | notes | notice
| :-- | :-- | :-- | :-- | :-- |
| `patternType` | | specifies the type of pattern for filling | | |

##### `<patternFill>`->`patternType`
All values `patternType` attribute in `<patternFill>` tag in **Standard OOXML**.

There may be more values in `Spreadsheet`.

| values | meaning | description | notes | notice
| :-- | :-- | :-- | :-- | :-- |
| `"none"` | |  No pattern fill. | The shape will be transparent (unless another fill is applied). | |
| `"solid"` | |  A solid color fill. | The color is determined by the `<fgColor>` element. | |
| `"pct5"` | |  5% pattern fill. | | |
| `"pct10"` | |  10% pattern fill. | | |
| `"pct20"` | |  20% pattern fill. | | |
| `"pct25"` | |  25% pattern fill. | | |
| `"pct30"` | |  30% pattern fill. | | |
| `"pct40"` | |  40% pattern fill. | | |
| `"pct50"` | |  50% pattern fill. | | |
| `"pct60"` | |  60% pattern fill. | | |
| `"pct70"` | |  70% pattern fill. | | |
| `"pct75"` | |  75% pattern fill. | | |
| `"pct80"` | |  80% pattern fill. | | |
| `"pct90"` | |  90% pattern fill. | | |
| `"horz"` | |  horzitonal line pattern. | | |
| `"vert"` | |  vertical line pattern. | | |
| `"diagCross"` | | diagonal crosshatch fill. | | |
| `"diagStripe"` | | diagonal stripe fill. | | |
| `"thinHorz"` | |  thin horizontal line pattern | | |
| `"thinVert"` | |  thin vertical line pattern | | |
| `"thinDiagCross"` | | thin diagonal crosshatch pattern | | |
| `"thinDiagStripe"` | | thin diagonal stripe  pattern | | |
| `"dot5x5"` | |   5x5 dot pattern | | |
| `"dot10x10"` | | 10x10 dot pattern | | |
| `"smCheck"` | | Small checkerboard pattern | | |
| `"lgCheck"` | | Large checkerboard pattern | | |
| `"smGrid"` | | Small grid  pattern | | |
| `"lgGrid"` | |  Large grid  pattern | | |
| `"divot"` | | divot pattern | | |
| `"brick"` | | brick pattern | | |
| `"weave"` | | weave pattern | | |
| `"plaid"` | | plaid pattern | | |
| `"dither"` | | dither pattern | | |

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

+ the `xmlns` namespace targets to `http://schemas.openxmlformats.org/spreadsheetml/2006/main`, meaning that the default SpreadSheetML schema in Office Excel 2006 (according to `xmlns="http://schemas.openxmlformats.org/spreadsheetml/2006/main"`).
+ the `xmlns:r` namespace targets to `http://schemas.openxmlformats.org/officeDocument/2006/relationships`, meaning that the relationship uses Office Excel 2006 (according to `xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships"`).
+ the markup will be compatible to Office Excel 2006 version (or above) (according to `xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"`).
+ specifies extensions version. The extensions that introduced in relates to Office Excel 2013 (according to `xmlns:x15="http://schemas.microsoft.com/office/spreadsheetml/2010/11/main"`).
+ specifies extensions version. The extension that relates to revision tracking features introduced in or around Excel 2016 (according to `xmlns:xr="http://schemas.microsoft.com/office/spreadsheetml/2014/revision"`).
+ for further revision tracking enhancements introduced in a later update of Excel 2016 or a subsequent version. (according to `xmlns:xr6="http://schemas.microsoft.com/office/spreadsheetml/2016/revision6")`.
+ for yet another set of revision tracking features, likely introduced in a later update of Excel 2016 or a subsequent version (according to `xmlns:xr10="http://schemas.microsoft.com/office/spreadsheetml/2016/revision10"`)
+ for revision tracking features introduced around Excel 2016. (according to `xmlns:xr2="http://schemas.microsoft.com/office/spreadsheetml/2015/revision2"`).
+ it indicates that the xml preprocessor will ignores these namespace
    - x15
    - xr
    - xr6
    - x10
    - xr2

(according to `mc:Ignorable="x15 xr xr6 xr10 xr2"`).

#### example 1.2 -- styleSheet tag as root node in `~/xl/styles.xml`
```
<styleSheet
xmlns="http://schemas.openxmlformats.org/spreadsheetml/2006/main"
xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
xmlns:x14ac="http://schemas.microsoft.com/office/spreadsheetml/2009/9/ac"
xmlns:x16r2="http://schemas.microsoft.com/office/spreadsheetml/2015/02/main"
xmlns:xr="http://schemas.microsoft.com/office/spreadsheetml/2014/revision"
mc:Ignorable="x14ac x16r2 xr">
```

In above example, we can know that

+ In `xmlns` namespace, it uses the SpreadsheetML Schema in version 2006.
+ In `xmlns:mc` namespace, the markup is compatible with SpreadsheetML Schema in version 2006 (or above).
+ In `xmlns:x14ac` namespace, the application is compatible with Office Excel 2009.9 (released at Sep, 2009) version (or above).

> [!NOTE]
> However, the closest version of Office Excel, but at least of version 2009.9 is version 2010.

+ In `xmlns:x16r2` namespace, for Office Excel in version 2016 (or above), the SpreadsheetML Schema in version 2015.02 (released at Feb, 2015) applies for revision.

+ In `xmlns:xr` namespace, the SpreadsheetML Schema in version 2014 applies for revision tracking (tracking for revision changes).

+ In `mc:Ignorable`, it ignore these namespace `x14ac`,`x16r2`,`xr`.

#### exaple 2.1 -- sheets
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

#### exaple 3.1 -- view of workbook
```
<bookViews>
    <workbookView xWindow="0" yWindow="0" windowWidth="22260" windowHeight="C" activeTab="2" xr2:uid="{00000000-000D-0000-FFFF-FFFF00000000}"/>
</bookViews>
```

In above example, we can know that

+ there is exactly one workbook.
+ the first workbook's window is at the top-most point (relative to its parent window or screen (if it has no parent).
+ the width of the first workbook's window is `22260` twips of the point.
+ the height of the first workbook's window is `width` twips of the point.
+ The third tab (or said, worksheet) is in active. due to zero-based.
+ its guid is `00000000-000D-0000-FFFF-FFFF00000000`.
  
#### exaple 4.1 -- workbook properties
```
<workbookPr date1904="1" showObjects="all" saveExternalLinkValues="1" codeName="ThisWorkbook"/>
```

In above example, we can know that

+ The workbook uses the 1904 date system.
+ All objects are displayed
+ External link values are saved.
+ The VBA codename for the workbook is "ThisWorkbook".

#### exaple 5.1 -- views of sheets 
a part of xml content of `~/xl/sheets/sheet1.xml` under an Excel file.

```
<sheetViews>
  <sheetView topLeftCell="A10" workbookViewId="0">
    <selection activeCell="E1" sqref="E1"/>
  </sheetView>
</sheetViews>
```

In above example, we can know that

+ There are one sheet view that references to the id of workbook view equals to `0`.</br>Additionally, when it is opened, it will navigate to the cell `A10` (here, the cell `A10` is on the top-left corner).
+ In the sheet view, it references the selection `E1` and the active cell is `E1` in current section.

#### exaple 6.1 -- columns of views of sheets 
a part of xml content of `~/xl/sheets/sheet1.xml` under an Excel file.

```
<sheetViews>
  <sheetView topLeftCell="A10" workbookViewId="0">
    <selection activeCell="E1" sqref="E1"/>
  </sheetView>
</sheetViews>
<sheetFormatPr defaultRowHeight="14.5" x14ac:dyDescent="0.35"/>
<cols>
  <col min="1" max="1" width="9.1796875" bestFit="1" customWidth="1"/>
  <col min="2" max="2" width="18.36328125" bestFit="1" customWidth="1"/>
  <col min="3" max="3" width="12.90625" bestFit="1" customWidth="1"/>
</cols>
```

In above example, we can know that

+ In the sheet view that references to id of workbook view equals to `0`, there are three columns that are used or their formatting are specified.

  - In `A` column, the width is `9.1796875` points.</br>And the width can be customized, meaning that the width is NOT automatically adjusted to the the value specified in `width` attribute.</br>Additionally, it should be best fit, meaning that the app should always adjust the column width so that it exactly fits to the content of the column. (i.e. The column width is automatically adjusted to the maximum of width the content holds for each cell in the column).   
  - In `B` column, the width is `18.36328125` points.</br>And the width can be customized, meaning that the width is NOT automatically adjusted to the the value specified in `width` attribute.</br>Additionally, it should be best fit, meaning that the app should always adjust the column width so that it exactly fits to the content of the column.
  - In `C` column, the width is `12.90625` points.</br>And the width can be customized, meaning that the width is NOT automatically adjusted to the the value specified in `width` attribute.</br>Additionally, it should be best fit, meaning that the app should always adjust the column width so that it exactly fits to the content of the column.

#### exaple 7.1 -- default sheet format
a part of xml content of `~/xl/sheets/sheet1.xml` under an Excel file.

```
<sheetFormatPr defaultRowHeight="14.5" x14ac:dyDescent="0.35"/>
```

In above example, we can know that

+ The default row height of the sheet is `14.5` point and specifies a dynamic descent of 0.35 pixels for bottom-aligned text in the rows of this sheet.

#### exaple 8.1 -- data within a worksheet
xml content of `~/xl/sheets/sheet1.xml` under an Excel file.

```
<worksheet
 <!-- namespace declarations and attributes omitted -->
>
 <dimension ref="A1:C2"/>
 <sheetViews>
  <sheetView topLeftCell="A10" workbookViewId="0">
   <selection activeCell="E1" sqref="E1"/>
  </sheetView>
 </sheetViews>
 <sheetFormatPr defaultRowHeight="14.5" x14ac:dyDescent="0.35"/>
 <cols>
  <col min="1" max="1" width="9.1796875" bestFit="1" customWidth="1"/>
  <col min="2" max="2" width="18.36328125" bestFit="1" customWidth="1"/>
  <col min="3" max="3" width="12.90625" bestFit="1" customWidth="1"/>
 </cols>
 <sheetData>
  <row r="1" spans="1:3" x14ac:dyDescent="0.35">
    <c r="A1" t="s">
     <v>0</v>
    </c>
    <c r="B1" t="s">
     <v>2</v>
    </c>
    <c r="C1" t="s">
     <v>1</v>
    </c>
   </row>
   <row r="2" spans="1:3" x14ac:dyDescent="0.35">
    <c r="A2" t="s">
     <v>3</v>
    </c>
    <c r="B2" t="s">
     <v>4</v>
    </c>
    <c r="C2" t="s">
     <v>5</v>
    </c>
   </row>
 </sheetData>
 <!-- tags omitted -->
</worksheet>
```

In above example, we can know that

+ In `<dimension ref="A1:C2"/>`, the range `A1:C2` is referenced.
+ There are one sheet view that references to the id of workbook view equals to `0`.</br>Additionally, when it is opened, it will navigate to the cell `A10` (here, the cell `A10` is on the top-left corner).
+ In the sheet view, it references the selection `E1` and the active cell is `E1` in current section.
+ The default row height of the sheet is `14.5` point and specifies a dynamic descent of 0.35 pixels for bottom-aligned text in the rows of this sheet.
+ In the sheet view that references to id of workbook view equals to `0`, there are three columns that are used or their formatting are specified.

  - In `A` column, the width is `9.1796875` points.</br>And the width can be customized, meaning that the width is NOT automatically adjusted to the the value specified in `width` attribute.</br>Additionally, it should be best fit, meaning that the app should always adjust the column width so that it exactly fits to the content of the column. (i.e. The column width is automatically adjusted to the maximum of width the content holds for each cell in the column).   
  - In `B` column, the width is `18.36328125` points.</br>And the width can be customized, meaning that the width is NOT automatically adjusted to the the value specified in `width` attribute.</br>Additionally, it should be best fit, meaning that the app should always adjust the column width so that it exactly fits to the content of the column.
  - In `C` column, the width is `12.90625` points.</br>And the width can be customized, meaning that the width is NOT automatically adjusted to the the value specified in `width` attribute.</br>Additionally, it should be best fit, meaning that the app should always adjust the column width so that it exactly fits to the content of the column.

+ About the sheet data (defined under `<sheetData>` tag)
   
   - there are two rows here (we can know it from the clue, there are two `<row>` tag under `<sheetData>` tag)
   - In the first row (`<row r="1" spans="1:3" x14ac:dyDescent="0.35">`),

      + it spins from column `A` to `C`, then it overrides the `x14ac:dyDescent` attribute (inside `<sheetFormatPr defaultRowHeight="14.5" x14ac:dyDescent="0.35"/>`) to `0.35`, which is accidentally same.

      + there are three cells (we can know it from the clue, there are three `<c>` tag under `<row>` tag)

          - In the first cell (`<c r="A1" t="s">`), it refers to the cell `A1` in the worksheet. And indicates that it contains a string value which its actual value is the 0th index (from the clue, `<v>0</v>`) in the shared string table (which resides in `~/xl/sharedStrings.xml`), which is `plain text` here.
          - In the second cell (`<c r="B1" t="s">`), it refers to the cell `B1` in the worksheet. And indicates that it contains a string value which its actual value is the 2th index (from the clue, `<v>2</v>`) in the shared string table (which resides in `~/xl/sharedStrings.xml`), which is `encryption alogrithm` here.
          - In the third cell (`<c r="C1" t="s">`), it refers to the cell `C1` in the worksheet. And indicates that it contains a string value which its actual value is the 1th index (from the clue, `<v>1</v>`) in the shared string table (which resides in `~/xl/sharedStrings.xml`), which is `encrypted text` here.
    
   - In the second row (`<row r="2" spans="1:3" x14ac:dyDescent="0.35">`),

      + it spins from column `A` to `C`, then it overrides the `x14ac:dyDescent` attribute (inside `<sheetFormatPr defaultRowHeight="14.5" x14ac:dyDescent="0.35"/>`) to `0.35`, which is accidentally same.

        - In the first cell (`<c r="A2" t="s">`), it refers to the cell `A2` in the worksheet. And indicates that it contains a string value which its actual value is the 0th index (from the clue, `<v>3</v>`) in the shared string table (which resides in `~/xl/sharedStrings.xml`), which is `I Love you` here.
        - In the second cell (`<c r="B2" t="s">`), it refers to the cell `B2` in the worksheet. And indicates that it contains a string value which its actual value is the 2th index (from the clue, `<v>4</v>`) in the shared string table (which resides in `~/xl/sharedStrings.xml`), which is `unknown` here.
        - In the third cell (`<c r="C2" t="s">`), it refers to the cell `C2` in the worksheet. And indicates that it contains a string value which its actual value is the 1th index (from the clue, `<v>5</v>`) in the shared string table (which resides in `~/xl/sharedStrings.xml`), which is `I Hate you` here.

And thus, you will see a worksheet like this.

<img width="959" alt="image" src="https://github.com/user-attachments/assets/b9e68667-3ed9-4f1a-b33b-25e8a6077a6e" />

Here is, the part of xml content of `~/xl/sharedString.xml` file:

<img width="959" alt="image" src="https://github.com/user-attachments/assets/f10bf490-690b-4d6a-bafa-6af30af7ea00" />

 
#### exaple 9.1 -- file version
```
<fileVersion appName="xl" lastEdited="7" lowestEdited="6" rupBuild="20417"/>
```

In above example, we can know that

+ the last edit is in Office Excel.
+ the last edit id is `7`.
+ the earlieast edit id is `6`.
+ the rollup build id is `20417`.

#### exaple 9.2 -- extensibility list
```
<extLst>
    <ext xmlns:x15="http://schemas.microsoft.com/office/spreadsheetml/2010/11/main" uri="{140A7094-0E35-4892-8432-C4D2E57EDEB5}">
        <x15:workbookPr chartTrackingRefBase="1"/>
    </ext>
</extLst>
```

In above example, we can know that

+ there is a defined extension which targets `xml:x15` namepsace to `http://schemas.microsoft.com/office/spreadsheetml/2010/11/main`.
+ And it guid is `140A7094-0E35-4892-8432-C4D2E57EDEB5`.

#### exaple 10.1 -- metadata of the Excel
See [explanation of xml content in `~/docProps/app.xml` file under `aaa3.xlsx` file](https://github.com/40843245/OOXML/blob/main/examples/spreadsheet/Excel/aaa3.xlsx/docsProps/app.xml/app.xml.md)

See [explanation of xml content in `~/docProps/core.xml` file under `aaa3.xlsx` file](https://github.com/40843245/OOXML/blob/main/examples/spreadsheet/Excel/aaa3.xlsx/docsProps/core.xml/core.xml.md)
