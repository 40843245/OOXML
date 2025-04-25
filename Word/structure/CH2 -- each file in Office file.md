# CH2 -- each file in Office file
## objectives
In this chapter, you will learn

+ knowledgement of each file in Office file

## CH2.1 -- knowledgement of each file in Office file
### Word (`.docx`)
In [CH1.3 -- basic structure of an Office file](https://github.com/40843245/OOXML/blob/main/Word/structure/CH1%20--%20structure%20of%20a%20Document.md#word-docx),

we have discussed basic structure of an Office Word file, illustrated with a structure tree.

![image](https://github.com/user-attachments/assets/2feb2ea4-c7cb-4a4b-ac22-df93e446f54f)

Let's dive into each files.

| file name | under which directory | description | required</br>(MUST exists) | notice |
| :-- | :-- | :-- | :-- | :-- |
| `xxx.docx` | root node | the Office Word file | required | |
| `document.xml` | `~/word` | main content of the Office Word file -- `xxx.docx` | required | |
| `numbering.xml` | `~/word` | defines the numbering format that will be used in `~/word/document.xml`| required | |
| `styles.xml` | `~/word` | defines the styles that will be used in `~/word/document.xml` | required | |
| `settings.xml` | `~/word` | configures the settings (such as which Office Word is used to render it) that will be used in `~/word/document.xml` | required | |
| `footnotes.xml` | `~/word` | defines the footnotes that will be used in `~/word/document.xml` | optional | |
| `footer1.xml` | `~/word` | defines the footer that will be used in `~/word/document.xml` | optional | |
| `endnotes.xml` | `~/word` | defines the endnotes that will be used in `~/word/document.xml` | optional | |
| `header1.xml` | `~/word` | defines the header that will be used in `~/word/document.xml` | optional | |
| `theme1.xml` | `~/word/theme1` | configures the properties of a visual theme that will be used in `~/word/document.xml`. It typically configures<ol><li>Color Scheme</li><li>Font Scheme</li><li>Format Scheme (Effects Scheme)</li><li>and more</li></ol> | optional | |
| `chart1.xml` | `~/word/charts` | defines the chart that will be used in `~/word/document.xml` | optional | |
| `.rels` | `~/rels` | is a package-level relationship file, which may contains<ol><li>The nature of the relationship (e.g., the main document, core properties). These types are defined by XML namespaces.</li><li>Target: The location of the target part within the ZIP archive</li></ol> | required | |
| `document.xml.rels` | `~/word/rels` | defines the relationship between `~/word/document.xml` and other parts of the document package. The relationship can include<ol><li>Images</li><li>Headers</li><li>Footers</li><li>Footnotes</li><li>Endnotes</li><li>Hyperlinks</li><li>Theme</li><li>Styles</li><li>External Resources</li></ol> | required | |



