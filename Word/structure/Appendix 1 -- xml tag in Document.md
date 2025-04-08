# Appendix 1 -- xml tag in Document.md
## overview
### namespace in xml tag
| namespace in xml tag | stands for (represented as tag native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `<w>` | `<word>` | Microsoft Word | indicates that it describes xml content of a Microsoft Word file.| w stands for Microsoft Word | |
| `<o>` | `<ol>` | ordered list | an ordered list (including a numbered list) | o stands for ordered, l stands for list | |

### element in xml tag
#### `<w>` namespace
| element in xml tag | stands for (represented as tag native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `<w:body>` | `<body>` | body | the main part of file in xml (and html5) | | |
| `<w:val>` | | value | assign the value that in the tag | you can think of assign it to the attr of the tag in native html5. See following example for more fully understanding | |
| `<w:p>` | `<p>` | paragraph | A paragraph | notice that if an end-user only inputs an whitespace in .docx file, it will have `<w:p>` tag, see `docx格式文档详解：xml解析并用html还原`[^1] | 
| `<w:pPr>` | | paragraph property | property of a paragraph (configure property of the tag that is inside `<w:p>` tag) in Microsoft Word file | Pr stands for *Pr*operty | |
| `<w:spacing>` | spacing | settings about spacing between paragraphs | | |
| `<w:jc>` | | justification | settings about justification (alignment) of the paragraph | jc stands for *j*ustifi*c*ation | |
| `<w:r>` | | run | defines a run in Word | r stands for run | |
| `<w:rPr>` | | run property | configure property of a run (configure property of the tag that is inside `<w:r>` tag) | | |
| `<w:rFonts>`| | run fonts | configure fonts of a run (configure property of the tag that is inside `<w:rPr>` tag) | |
| `<w:sz>` | | size | font size | defines a font size (that is inside `<w:rFonts>` tag) | |
| `<w:tbl>` | `<table>` | table | a table in Microsoft Word file | tbl stands for table | |
| `<w:tr>` | `<tr>` | table row | a row of a table | t stands for table, r stands row | |
| `<w:tblPr>` | | table property | configure property (such as style and appearance) of a table (configure property of the tag that is inside `<w:tbl>` tag) in Microsoft Word file | | |
| `<w:tblGrid>` | | table column | columns of a table in Microsoft Word file | you can think of a grid as a lots of columns in table | |
| `<w:tc>` | `<td>` | table cell | an cell of a table | c stands for cell | |
| `<w:tcPr>` | | table cell property | configure property of a table cell (configure property of the tag that is inside `<w:tc>` tag) | including width and grid span | |

[^1]:[`docx格式文档详解：xml解析并用html还原`](https://juejin.cn/post/7166821284087595038)
