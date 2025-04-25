# CH5 -- common tags in OOXML
## objectives
In this chapter, you will learn

+ common tags in OOXML

## CH5.1 -- tags about DrawingML
In OOXML, the namespace `a` is used for DrawingML.

### about graphics
#### `<a:graphic>`
acts as a container that wraps the actual DrawingML content.

Think that it contains all definition of graphic data

#### `<a:graphicData>`
references of graphic data.

### about picture
#### `<a:pic>`
represents a picture object.

### about shape
#### `<a:shape>`
defines a basic geometric shapes and more complex predefined shape.

#### `<a:grpSp>`
defines a group of shape.

#### `<a:cxnSp>`
defines a connector shape.

#### about properies of shape 
#### `<a:style>`
defines shape style

##### `<a:spPr>`
defines properties about shape.

##### `<a:prstGeom>`
specifies a preset shape geometry.

##### `<a:custGeom>`
defines a custom shape geometry.

##### `<a:pathLst>`
acts like an container containing a list of paths for a custom geometry.

##### `<a:path>`
defines a single path within a custom geometry.

#### anout shape style
##### `<a:fillStyleLst>`
acts like an container containing a list of style for filling.

##### `<a:lnStyleLst>`
acts like an container containing a list of line style.

##### `<a:sp3d>`
defines 3D shape properties.

##### `<a:scene3d>`
defines 3D scene properties.

##### `<a:txXfrm>`
defines the transform for text within a shape.

### about line
#### `<a:ln>`
defines the properties of a line.

#### about line style
##### `<a:prstDash>`
specifies a preset dash pattern.

##### `<a:custDash>`
defines a custom dash pattern.

##### `<a:round>`
indicates that the join between these lines should be rounded.

Instead of a sharp corner (miter join) or a beveled (cut-off) corner, a smooth arc will connect the two line segments.   

##### `<a:bevel>`
specifies how the edges of a 3D shape or table cell should be rounded or angled, creating a visual depth effect. 

### about text body
#### `<a:txBody>`
adds and formats text within a graphical object.

#### about properties of text body
##### `<a:bodyPr>`
defines the overall properties of the text body.

### about effects
#### about shadow effects
##### `<a:outerShdw>`
defines an outer shadow effect.

##### `<a:innerShdw>`
defines an inner shadow effect.

#### about shape effects
##### `<a:effectLst>`
acts like an container containing a list of shape effects.

#### about glow effects
##### `<a:glow>`
specifies a glow effect.

#### about reflection effects
##### `<a:reflection>`
defines a reflection effect.

#### about blur effects
##### `<a:blur>`
specifies a Gaussian blur effect.

#### about fill overlay effects
##### `<a:fillOverlay>`
defines a fill overlay effect.

#### about diagram-specific effects
##### `<a:effectDag>`
defines a diagram-specific effect.

### about reference
#### about reference of chart
##### `<a:chart>`
references a chart which is actual defined in `<c:chart>` tag.

<img width="864" alt="image" src="https://github.com/user-attachments/assets/f33787d4-b429-489c-9c2d-d7b1009dff69" />

<img width="544" alt="image" src="https://github.com/user-attachments/assets/c798d7ac-318b-4054-a6ba-c29def1f6d33" />

## CH4.2 -- tags about WordprocessingML
The namespace `w` refers to WordprocessingML.

### about entire document
#### `<w:document>`
defines a document. 

It must reside at the root node of `~/word/document.xml`

#### `<w:glossaryDocument>`
is the root element of a Glossary document part within a WordprocessingML package.

> [!IMPORTANT]
> A Glossary document part stores AutoText entries.

> [!IMPORTANT]
> AutoText entries are reusable pieces of content, such as formatted text, graphics, and tables, that users can quickly insert into their documents.

### about main body
#### `<w:body>`
defines the main body.

It must a child of `<w:document>` tag,

### about section
#### about properties of section 
##### `<w:sectPr>`
defines properties for a section in the document.

### about page
#### about header
##### `<w:hdr>`
specifies the header.

##### `<w:evenAndOddHeaders>`
specifies different headers for even and odd pages.

##### `<w:firstPageHeader>`
specifies a different header for the first page.

#### about footer
##### `<w:ftr>`
specifies the footer.

##### `<w:evenAndOddFooters>`
specifies different footers for even and odd pages.

##### `<w:firstPageFooter>`
specifies a different footer for the first page.

##### `<w:fldChar>`
defines a field character for page.

> [!NOTE]
> a field character is usually used for the header or footer.

> [!IMPORTANT]
> In a non-corrupted Office Word file,
>
> It must follow if it defines a field character in a paragraph.
>
> + the first ocurrence of `<w:fldChar>` tag must be set its type to `begin` (i.e. `w:fldCharType="begin"`). Thus, look like this: `<w:fldChar w:fldCharType="begin"/>`
> + the second ocurrence of `<w:fldChar>` tag must be set its type to `separate` (i.e. `w:fldCharType="separate"`). Thus, look like this: `<w:fldChar w:fldCharType="separate"/>`
> + the third ocurrence of `<w:fldChar>` tag must be set its type to `end` (i.e. `w:fldCharType="end"`). Thus, look like this: `<w:fldChar w:fldCharType="end"/>`
> + the `<w:instrText>` tag must be between the first occurence and the second occurence of `<w:fldChar>` tag.
>
> For fully understanding, see an example in [`example 23 -- defines a footer` in `Appendix 1 -- xml tag in Document`](https://github.com/40843245/OOXML/blob/main/Word/structure/Appendix%201%20--%20xml%20tag%20in%20Document.md#example-23----defines-a-footer)

##### `<w:instrText>`
sets the field instruction of the field character.

> [!NOTE]
> It's usually inside `<w:fldChar>` tag.

> [!IMPORTANT]
> To set the field instruction in the field character.
>
> See [`example 23 -- defines a footer` in `Appendix 1 -- xml tag in Document`](https://github.com/40843245/OOXML/blob/main/Word/structure/Appendix%201%20--%20xml%20tag%20in%20Document.md#example-23----defines-a-footer)

##### `<w:fldSimple>`
defines a simple field.

### about paragraph
#### `<w:p>`
defines a new paragraph.

#### about properties of paragraph
##### `<w:pPr>`
defines properties of the paragraph.

### about run
#### `<w:r>`
defines a run.

#### about properties of run
##### `<w:rPr>`
defines the properties of a run (e.g., font, size, bold, italic).

### about text
#### `<w:t>`
represents the actual text content within a run.

### about break line
#### `<w:br>`
defines a break line (i.e. `\n`)

### about table
#### `<w:tbl>`
defines a table.

#### about properties of table
##### `<w:tblPr>`
defines the properties of a table.

##### about table borders
###### `<w:tblBorders>`
defines the table borders.

#### about columns in table
##### `<w:tblGrid>`
defines the header with an array of field name in a table.

> [!TIP]
> Think:
>
> you can think it acts like a header in a table and in native html5, it is `<thead>` tag.

##### about grid in header
###### `<w:gridCol>`
defines a grid in the header (`<w:tblGrid>).

> [!TIP]
> Think:
>
> you can think header acts like an array while grid acts like an element of the header. in native html5, it is `<th>` tag.
#### about row in table
##### `<w:tr>`
defines a row in a table.

#### about a cell in table
##### `<w:tc>`
defines a cell in a table.

##### about properties of a cell in table
###### `<w:tcPr>`
defines properties of a cell in a table.

### about list
#### about properties of list
##### `<w:numPr>`
defines numbering properties for lists.

##### about level
###### `<w:lvl>`
defines the formatting for a specific numbering level in an abstract number.

###### `<w:ilvl>`
specifies the indentation level of a list item.

###### `<w:lvlOverride>`
overrides properties for a specific numbering level.

#### about number
##### `<w:numId>`
references a specific numbering definition.

##### `<w:num>`
defines a numbering instance.

##### `<w:abstractNum>`
defines an abstract numbering scheme.

### about style
#### `<w:styles>`
acts like an container containing all definitions of lists.

#### `<w:style>`
defines a specific style.

#### `<w:name>`
specifies the name of style.

#### `<w:next>`
specifies the style to apply after a paragraph with the current style.

#### about configuring properties of style
##### `<w:color>`
specifies the color of font.

##### `<w:shd>`
specifies the shadow of font.

##### `<w:b>`
specifies whether the font is bold.

##### `<w:i>`
specifies whether the font is italic.

##### `<w:u>`
specifies whether the font is underlined.

##### `<w:strike>`
specifies whether the font is strikethrough.

##### `<w:vertAlign>`
specifies the vertical alignment of the font.

##### `<w:borders>`
specifies the borders.

##### `<w:top>`
specifies the top border of the borders.

##### `<w:left>`
specifies the left border of the borders.

##### `<w:bottom>`
specifies the bottom border of the borders.

##### `<w:right>`
specifies the right border of the borders.

##### `<w:insideH>`
specifies internal horizontal border. i.e. specifies horizontal border between rows (within a paragraph or table etc).

##### `<w:insideV>`
specifies vertical border between columns within a table.

#### about reference of style
##### `<w:pStyle>`
references a paragraph style.

##### `<w:rStyle>`
references a run style.

#### OO design pattern in Style package part
##### `<w:basedOn>`
inherits the specific defined style.

### about drawing objects
#### `<w:drawing>`
acts like an container containing all definitions of drawing objects.

#### about embedded objects
##### `<w:object>`
represents an embedded object (e.g., OLE object).

#### about picture
##### `<w:pict>`
represents a picture.

### about hyperlink
#### `<w:hyperlink>`
defines a hyperlink.

### about bookmark
#### `<w:bookmarkStart>`
defines a start point of a bookmark.

#### `<w:bookmarkEnd>`
defines a end point of a bookmark.

### about notes
#### about footnotes
##### `<w:footnotes>`
acts like a container containing many footnotes.

##### `<w:footnote>`
defines a footnote.

##### about properties of a footnote
###### `<w:footnotePr>`
defines the properties of the footnote.

#### about endnotes
##### `<w:endnotes>`
acts like a container containing many endnotes.

##### `<w:endnote>`
defines a endnote.

##### about properties of a endnote
###### `<w:endnotePr>`
defines the properties of the endnote.

### about revision tracking elements
#### `<w:ins>`
represents inserted content.

#### `<w:del>`
represents deleted content.

#### `<w:moveFrom>`
represents moved content. It indicates the content is moved from. 

#### `<w:moveTo>`
represents moved content. It indicates the content is moved to.

### about theme
#### about theme font
##### `<w:themeFont>`
defines theme fonts.

#### about theme color
##### `<w:colorScheme>`
defines a color scheme.

Here, color scheme means the palette of colors available within a theme.

### about comments
#### `<w:comments>`
acts like a container containing lots of comments.

#### `<w:comment>`
defines a comment.

#### about properties of a comment
##### `<w:commentPr>`
defines properties of the comment.

##### `<w:themeColor>`
references a specific color defined in the active color scheme (defined by `<w:colorScheme>`).

> [!IMPORTANT]
> What is the different between `<w:colorScheme>` and `<w:themeColor>`?
>
> <img width="533" alt="image" src="https://github.com/user-attachments/assets/4f55c074-9198-4401-9210-cebc930412a2" />
>
> provided by Google Gemini.
