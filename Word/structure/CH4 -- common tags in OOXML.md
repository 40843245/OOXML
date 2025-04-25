# CH4 -- common tags in OOXML
## objectives
In this chapter, you will learn

+ common tags in OOXML

## CH4.1 -- tags about DrawingML
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

#### about shape property
#### `<a:style>`
defines shape style

##### `<a:spPr>`
defines properties about shape.

##### `<a:prstGeom>`
specifies a preset shape geometry.

##### `<a:custGeom>`
defines a custom shape geometry.

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

### about reference
#### about reference of chart
##### `<a:chart>`
references a chart which is actual defined in `<c:chart>` tag.

<img width="864" alt="image" src="https://github.com/user-attachments/assets/f33787d4-b429-489c-9c2d-d7b1009dff69" />

<img width="544" alt="image" src="https://github.com/user-attachments/assets/c798d7ac-318b-4054-a6ba-c29def1f6d33" />
