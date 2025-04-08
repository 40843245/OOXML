# Appendix 1 -- xml tag in Document.md
## overview
### namespace in xml tag
| namespace in xml tag | stands for (represented as tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `<w>` | `<word>` | Microsoft Word | indicates that it describes xml content of a Microsoft Word file.| w stands for Microsoft Word | |
| `<o>` | `<ol>` | ordered list | an ordered list (including a numbered list) | o stands for ordered, l stands for list | |

### element in xml tag
#### `<w>` namespace
| element in xml tag | stands for (represented as tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `<w:body>` | `<body>` | body | the main part of file in xml (and html5) | | |
| `<w:p>` | `<p>` | paragraph | A paragraph | notice that if an end-user only inputs an whitespace in .docx file, it will have `<w:p>` tag, see `docx格式文档详解：xml解析并用html还原`[^1] | 
| `<w:pStyle>` | | paragraph style | applies style (according to value of `w:val` attribute) to paragraph (that is inside `<w:p>` tag) | the style to apply is defined in `~/word/style.xml` file | |
| `<w:pPr>` | | paragraph property | property of a paragraph (that is inside `<w:p>` tag) in Microsoft Word file | Pr stands for *Pr*operty | |
| `<w:spacing>` | spacing | settings about spacing between paragraphs | | |
| `<w:jc>` | | justification | settings about justification (alignment) of the paragraph | jc stands for *j*ustifi*c*ation | |
| `<w:r>` | | run | defines a run in Word | r stands for run | |
| `<w:rPr>` | | run property | configure property of a run (that is inside `<w:r>` tag) | | |
| `<w:rFonts>`| | run fonts | configure fonts of a run (that is inside `<w:rPr>` tag) | |
| `<w:sz>` | | size | font size | defines a font size for standard characters (that is inside `<w:rPr>` tag) |  |
| `<w:szCs>` | | size | font size | defines a font size for complex script characters (that is inside `<w:rPr>` tag) | Cs stands for *C*omplex *s*cript | |
| `<w:tbl>` | `<table>` | table | a table in Microsoft Word file | tbl stands for table | |
| `<w:tr>` | `<tr>` | table row | a row of a table | t stands for table, r stands row | |
| `<w:tblPr>` | | table property | configure property (such as style and appearance) of a table (configure property of the tag that is inside `<w:tbl>` tag) in Microsoft Word file | | |
| `<w:tblGrid>` | | table column | columns of a table in Microsoft Word file | you can think of a grid as a lots of columns in table | |
| `<w:tc>` | `<td>` | table cell | an cell of a table | c stands for cell | |
| `<w:tcPr>` | | table cell property | configure property of a table cell (configure property of the tag that is inside `<w:tc>` tag) | including width and grid span | |
| | | | | | | | 
| `<w:bookmarkStart>`| 
###### attribute in `<w:p>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:val` | `value` in native html5 | value | assign the value that in the tag | you can think of assign the value to the attr of the tag in native html5. | |
| `w:rsidR` | | revision id for run | assign the value of revision id for run  | rs stands for *r*evi*s*ion, R stands for *R*un | |
| `w:rsidRDefault` | | revision id for run default | assign the default value of revision id for run  | rs stands for *r*evi*s*ion, R stands for *R*un | |

##### examples and explanations
###### example 1
```
<w:r>
  <w:rPr>
    <!-- ... -->
    <w:rFonts w:ascii="標楷體" w:eastAsia="標楷體" w:hAnsi="標楷體"/>
    <w:sz w:val="52"/>
    <w:szCs w:val="52"/>
    <!-- ... -->
  </w:rPr>
</w:r>
```

In this example, we can know 

1. In `<w:r>`, it defines a run.
2. In `<w:rPr>`, it configures the property of the run.
3. In `<w:rFonts w:ascii="標楷體" w:eastAsia="標楷體" w:hAnsi="標楷體"/>`,

it configure the default fonts of the run,

the default fonts are `標楷體`, `標楷體`, `標楷體` when it is decoded as ascii characters, East Asian characters, high Ansi characters respectively.

4. In `<w:sz w:val="52"/>`,

it also configure the default size is 52 half-points for **standard characters** (i.e. non-complex script characters) (like English, French, German etc).

> [!TIP]
> You can think it as setting the `style` attr as `"font-size:52"` in native html5.

5. In `<w:szCs w:val="52"/>`,

it also configure the default size is 52 for **complex script characters** (like Arabic, Hebrew, Devanagari etc).

> [APPRECIATION]
> Thanks to Google Gemini, it refers from Google Gemini's answer.

[^1]:[`docx格式文档详解：xml解析并用html还原`](https://juejin.cn/post/7166821284087595038)
