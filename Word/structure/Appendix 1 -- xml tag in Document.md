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
| `<w:p>` | `<p>` | paragraph | A paragraph | notice that if an end-user only inputs an whitespace in .docx file, it will have `<w:p>` tag, see `docx格式文档详解：xml解析并用html还原`[^1] | 
| `<w:pPr>` | | paragraph property | property of a paragraph in Microsoft Word file | Pr stands for Property | |
| `<w:spacing>` | spacing | settings about spacing between paragraphs | | |
| `<w:jc>` |
| `<w:tbl>` | `<table>` | table | a table in Microsoft Word file | tbl stands for table | |
| `<w:tr>` | `<tr>` | table row | a row of a table | t stands for table, r stands row | |
| `<w:tblPr>` | | table property | property (such as style and appearance) of a table in Microsoft Word file | | |
| `<w:tblGrid>` | | table column | columns of a table in Microsoft Word file | you can think of a grid as a lots of columns in table | |
| `<w:tc>` | `<td>` | table cell | an cell of a table | c stands for cell | |
| `<w:tcPr>` | | table cell property | property of table cell property | including width and grid span | |
| 

[^1]:[`docx格式文档详解：xml解析并用html还原`](https://juejin.cn/post/7166821284087595038)
