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
| `<w:body>` | `<body>` | body | the main part of file in native xml (and native html5) | | |
| `<w:lang>` | `<lang>` | language | the language for characters | lang stands for *lang*uage | |
| | | | | | | | 
| `<w:p>` | `<p>` | paragraph | A paragraph | notice that if an end-user only inputs an whitespace in .docx file, it will have `<w:p>` tag, the article `docx格式文档详解：xml解析并用html还原`[^1] says this situation. | 
| | | | | | | | 
| `<w:pStyle>` | | paragraph style | applies style (according to value of `w:val` attribute) to paragraph (that is inside `<w:p>` tag) | the style to apply is defined in `~/word/style.xml` file | |
| `<w:pPr>` | | paragraph property | property of a paragraph (that is inside `<w:p>` tag) in Microsoft Word file | Pr stands for *Pr*operty | |
| | | | | | | | 
| `<w:b/>` | `<b>` and `<b/>` in native html5 | bold | determine the text is bold | | |
| `<w:spacing>` | spacing | settings about spacing between paragraphs | | |
| `<w:jc>` | | justification | settings about justification (alignment) of the paragraph | jc stands for *j*ustifi*c*ation | |
| | | | | | | | 
| `<w:r>` | | run | defines a run in Word | r stands for run | |
| | | | | | | | 
| `<w:rPr>` | | run property | configure property of a run (that is inside `<w:r>` tag) | | |
| `<w:rFonts>`| | run fonts | configure fonts of a run (that is inside `<w:rPr>` tag) | |
| | | | | | | | 
| `<w:sz>` | | size | defines a font size for standard characters (that is inside `<w:rPr>` tag) |  |
| `<w:szCs>` | | size | defines a font size for complex script characters (that is inside `<w:rPr>` tag) | Cs stands for *C*omplex *s*cript | |
| | | | | | | | 
| `<w:tbl>` | `<table>` | table | a table in Microsoft Word file | tbl stands for table | |
| `<w:tblPr>` | | table property | configure property (such as style and appearance) of a table (that is inside `<w:tbl>` tag) in Microsoft Word file | | |
| `<w:tblGrid>` | `<tr>` (first occurence) | table grid | defines a grid (header) of a table in Microsoft Word file | you can think of a grid like a header row ( consists of lots of columns ) in table | |
| `<w:gridCol>` | `<th>` | table grid column | defines a cell in a grid of a table in Microsoft Word file | | it must be inside `<w:tblGrid>` tag. Otherwise, the Word file is corrupted. |
| `<w:tr>` | `<tr>` | table row | a row of a table | t stands for table, r stands row | |
| `<w:tc>` | `<td>` | table cell | an cell of a table | c stands for cell | |
| `<w:tcPr>` | | table cell property | configure property of a table cell (that is inside `<w:tc>` tag) | including width and grid span | |
| `<w:tblStyle>` | | table style | applies style (according to value of `w:val` attribute) to paragraph (that is inside `<w:tbl>` tag) | the style to apply is defined in `~/word/style.xml` file | |
| | | | | | | | 
| `<w:sectPr>` | | sect property | configure property of a sect | sect stands for section | |
| `<w:pgSz>` | | page size | configures a page size (that is inside `<w:sectPr>` tag) | pg stands for *p*a*g*e | |
| `<w:pgMar>` | | page margin | configures a page margin (that is inside `<w:sectPr>` tag) | Mar stands for *Mar*gin | |
| | | | | | | | 
| `<w:bookmarkStart>` | | bookmark start | defines a bookmark with start point | | One `<w:bookmarkStart>` tag must match one `<w:bookmarkEnd>` tag. Otherwise, the file is corrupted. | 
| `<w:bookmarkEnd>` | | bookmark end | defines a bookmark with end point to enclose a bookmark | | Same as above | 
| | | | | | | | 

###### attribute in `<w:p>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:rsidR` | | revision id for run | assign the value of revision id for run  | rs stands for *r*evi*s*ion, R stands for *R*un | |
| `w:rsidRDefault` | | revision id for run default | assign the default value of revision id for run  | rs stands for *r*evi*s*ion, R stands for *R*un | |
| `w:rsidSect` | | revision id for section | assign the default value of revision id for section | rs stands for *r*evi*s*ion | |

###### attribute in `<w:p>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:rsidR` | | revision id for run | assign the value of revision id for run  | rs stands for *r*evi*s*ion, R stands for *R*un | |
| `w:rsidRDefault` | | revision id for run default | assign the default value of revision id for run  | rs stands for *r*evi*s*ion, R stands for *R*un | |
| `w:rsidSect` | | revision id for section | assign the default value of revision id for section | rs stands for *r*evi*s*ion | |

###### attribute in `<w:sz>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:val | `value` in native html5 | assign the value to determine default font size for **non-complex script characters** (that is inside `<w:pPr>` tag) | its unit is half-point. | |

###### attribute in `<w:szCs>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:val | `value` in native html5 | assign the value to determine default font size for **complex script characters** (that is inside `<w:pPr>` tag) | its unit is half-point. | |

###### attribute in `<w:pgSz>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:w | `width` in css | assign the value to determine width of page size (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| w:h | `height` in css | assign the value to determine height of page size (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |

###### attribute in `<w:pgMar>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:top | `margin-top` in css | assign the value to determine top of page margin (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| w:right | `margin-right` in css | assign the value to determine right of page margin (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| w:bottom | `margin-bottom` in css | assign the value to determine bottom of page margin (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |
| w:left | `margin-left` in css | assign the value to determine left of page margin (that is inside `<w:sectPr>` tag) | its unit is twips (twentieths of a point). | |

###### attribute in `<w:cols>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:space | | assign an value  (that is inside `<w:sectPr>` tag) will apply to | its unit is twips (twentieths of a point). | |


###### attribute in `<w:pStyle>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:val | `value` in native html5 | assign an Guid as value that determines what the paragraph (that is inside `<w:p>` tag) will apply to | | |

###### attribute in `<w:tblStyle>`
Way to parsing it is similar to parsing `<w:pStyle>`.

| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| w:val | `value` in native html5 | assign an Guid as value that determines what the table (that is inside `<w:tbl>` tag) will apply to | | |

###### attribute in `<w:bookmarkStart>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:id` | `id` in native html5 | id of start point of bookmark | assign the id of start point of bookmark that in the tag | | |
| `w:name` | `name` in native html5 | name of start point of bookmark | assign the name of start point of bookmark that in the tag | | |

###### attribute in `<w:bookmarkEnd>`
| attribute in xml tag | stands for (represented as attribute in tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `w:id` | `id` in native html5 | id of end point of bookmark | assign the id of end point of bookmark that in the tag | |


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

In this example, we can know that

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

###### example 2

```
<w:tbl>
  <w:tblPr>
    <w:tblStyle w:val="TableGrid"/>
    <w:tblW w:w="5000" w:type="auto"/>
    <w:tblLook w:val="04A0"/>
  </w:tblPr>
  <w:tblGrid>
    <w:gridCol w:w="1892.5"/>
  </w:tblGrid>
  <w:tr>
    <w:tc>
      <w:tcPr>
        <w:tcW w:w="15140" w:type="dxa"/>
        <w:gridSpan w:val="9"/>
      </w:tcPr>
    </w:tc>
    <w:p>
      <w:pPr>
        <w:jc w:val="left"/>
      </w:pPr>
      <w:r>
        <w:rPr>
          <w:rFonts w:ascii="標楷體" w:hAnsi="標楷體" w:cs="標楷體" w:eastAsia="標楷體"/>
          <w:sz w:val="32"/>
          <w:szCs w:val="32"/>
          <w:b/>
        </w:rPr>
        <w:t>text 1</w:t>
      </w:r>
    </w:p>
  </w:tr>
</w:tbl>
```

In this example, we can know that

1. In `<w:tr>`, it defines 

[^1]:[`docx格式文档详解：xml解析并用html还原`](https://juejin.cn/post/7166821284087595038)
