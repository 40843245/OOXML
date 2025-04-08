# Appendix 1 -- xml tag in Document.md
## overview
### namespace in xml tag
| namespace in xml tag | stands for xml tag | meaning | description | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `<w>` | `<word>` | Microsoft Word | indicates that it describes xml content of a Microsoft Word file.| |
| `<o>` | `<ol>` | ordered list | an ordered list (including a numbered list) | |

### element in xml tag
#### `<w>` namespace
| element in xml tag | stands for xml tag | meaning | description | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `<w:body>` | `<body>` | body | the main part of file in xml (and html5) | |
| `<w:p>` | `<p>` | paragraph | A paragraph | notice that if an end-user only inputs an whitespace in .docx file, it will have `<w:p>` tag, see `docx格式文档详解：xml解析并用html还原`[^1] | 
| `<w:tbl>` | `<table>`| table | a table in Microsoft Word file | |
| `<w:tr>` | `<tr>` | <>

[^1]:[`docx格式文档详解：xml解析并用html还原`](https://juejin.cn/post/7166821284087595038)
