# Appendix 2 -- available options of attribute of tag in xml for Word
## NOTICE
See [`NOTICE.md`](https://github.com/40843245/OOXML/blob/main/NOTICE/NOTICE.md)

## Important concept
See [`important concept.md`](https://github.com/40843245/OOXML/blob/main/concept/important%20concept.md)

### about `xml` namespace
#### `xml:space` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"preserve"` | | preserve | whitespace (i.e. ` `, `\t`, and `\n`) within the element's content should be preserved exactly as it appears in the XML source. The application processing the XML should not normalize or remove any of this whitespace. | | | 
| `"default"` | | default processing (not fully preserve) | Default whitespace handling of the XML processor should be applied to the content of this element. | See following for more details. | | 

### about `v` namespace
#### `v:ext` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"edit"` | | editable | indicates that the shapes are **fully** editable within Office app. | | |
| `"view"` | | editable | indicates that the shapes are **NOT fully** editable within Office app. i.e. can only view or is ediatble but some capabilities are limited. | | |
| `"backwardCompatible"` | | | indicates that the VML extension is intended for backward compatibility with older versions of applications. | | Newer editors should render it, and ideally, allow some level of editing, while older editors might ignore or render it in a basic way without full understanding of the extended features. |

### about `a` namespace
#### `<a:blip>` -> `a:cstate` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"none"` | | | no compression | | |
| `"store"` | | | store without compression | It is equivalent to `"none"`. | |
| `"deflate"` | | deflation | compress it with deflate algorithm | | |
| `"lzma"` | | lzma | compress it with lzma (Lempel–Ziv–Markov chain) algorithm | | |

##### examples and explanations
###### example 1 -- grouping lots of series in a chart
```
<c:barChart xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart">
  <c:barDir val="col"/>
  <c:grouping val="clustered"/>

  <!-- other tags about bar charts omitted -->
  <!-- ... -->

</c:barChart>
```

In above example, 

the bar chart will be grouped by cluster. 

Looks like the following figure.

![image](https://github.com/user-attachments/assets/bd96c19f-286c-44cc-8ac8-cf1023d0c319)

###### example 2 -- grouping lots of series in a chart
```
<c:barChart xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart">
  <c:barDir val="col"/>
  <c:grouping val="stacked"/>

  <!-- other tags about bar charts omitted -->
  <!-- ... -->

</c:barChart>
```

In above example, 

the bar chart will be grouped by stacked. 

Looks like the following figure.

![image](https://github.com/user-attachments/assets/dce5d19d-7952-4f62-b9b1-1d67e42ef639)

#### `<c:overlap>` -> `val` attribute
It's range is from `-100` to `100`.

The default value is 0.

+ Case 1: value is 0.

No overlap 

+ Case 2: value is greater than 0.

Indicates that the bars will overlap by that percentage.

+ Case 3: value is less than 0.

Indicate that there will be a gap in addition to the normal gap.

This effectively increases the spacing between the bars.

#### `<c:showLegendKey>` -> `val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | show legend for each series. | | |
| `"false"` | | | **NOT** show legend for each series. | | |

#### `<c:showVal>` -> `val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | show value for each series. | | |
| `"false"` | | | **NOT** show value for each series. | | |

#### `<c:showCatName>` -> `val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | show category name for each series. | | |
| `"false"` | | | **NOT** show category name for each series. | | |

#### `<c:showSerName>` -> `val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | show name of data series for each series. | | |
| `"false"` | | | **NOT** show name of data series for each series. | | |

#### `<c:showPercent>` -> `val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | show percentage that a data point takes of its total for each series | | |
| `"false"` | | | **NOT** show percentage that a data point takes of its total for each series | | |

#### `<c:invertIfNegative>` -> `val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | the color (of bar charts or column charts) will be inverted when its value it represents is negative. | | |
| `"false"` | | | the color (of bar charts or column charts) will be **NOT** inverted when its value it represents is negative. | | |

#### `<c:lengendPos>` -> `val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"l"` | | left | specifies the position of the legend is **left** of the plot area of the chart  | | |
| `"t"` | | top | specifies the position of the legend is **top** of the plot area of the chart | | |
| `"r"` | | right | specifies the position of the legend is **right** of the plot area of the chart | | |
| `"b"` | | bottom | specifies the position of the legend is **bottom** of the plot area of the chart | | |
| `"tr"` | | *t*op-*r*ight | specifies the position of the legend is **top-right** of the plot area of the chart | | it may overlay the plot area. |

##### examples and explanation
###### examples 1 -- cross between different axis
```
<c:chart>
  <c:plotArea>
    <c:valAX>      
      <c:crossBetween val="between"/>
    </c:valAX>
  </c:plotArea>
</c:chart>
```

Imagine we have a bar chart showing sales for three months: January, February, and March.

In this scenario, 

the month labels ("January", "February", "March") would typically appear centered between the vertical gridlines 

representing the tick marks for each month. The bars representing the sales for each month would also be centered in these spaces.

```
      |       |       |
Sales |   |   |   |
      |---|---|---|
      | Jan | Feb | Mar |
      -------------------
```

###### examples 2 -- cross between different axis
```
<c:chart>
  <c:plotArea>
    <c:valAX>      
      <c:crossBetween val="between"/>
    </c:valAX>
  </c:plotArea>
</c:chart>
```

Imagine we have a bar chart showing sales for three months: January, February, and March.

In this scenario,

the month labels would align with the tick mark at the end of each category's interval. 

Consequently, the bars representing the sales for each month would also be positioned to align with these tick marks.

```
      |       |       |
Sales |    |    |    |
      |-----|-----|-----|
        Jan   Feb   Mar
      -------------------
```

### about `w` namespace
#### `<w:style>` -> `w:customStyle` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | indicates that it is a custom style | | |
| `"false"` | | | indicates that it is NOT a custom style | | |

#### `<w:style>` -> `w:type` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"paragraph"` | | | For paragraph-level formatting (affects the entire paragraph) | | |
| `"character"` | | | For character-level formatting (affects selected text within a paragraph). | | |
| `"table"` | | | For table-level formatting (affects the entire table). | | |
| `"numbering"` | | | For numbering definition formatting. | | |

#### `<w:style>` -> `w:default` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | indicates that this style is the default style for its style type  | | |
| `"false"` | | | indicates that this style is NOT the default style for its style type  | | |

#### `<w:kinsoku>` -> `w:val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"on"` | | | explicitly enable the kinsoku line-breaking rules for the paragraph. Word would then adjust line breaks to avoid having prohibited characters at the beginning or end of lines. | | |
| `"off"` | | explicitly turns off the application of kinsoku line-breaking rules for the current paragraph. | | |

#### `<w:keepLines>` -> `w:val` attribute  
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | keep lines. | it instructs Word to keep all lines of the paragraph together on the same page.| default value. |
| `"false"` | | | NOT keep lines. | it allows Word to break the paragraph across page breaks if necessary to fit the content. | When `<w:keepLines>` tag is not used, we can think that it will NOT keep lines. (same effect of `<w:keepLines w:val="false">`) |

#### `<w:keepNext>` -> `w:val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | to prevent a page break from occurring between the current paragraph and the one immediately after it. | If the two paragraphs together cannot fit on the current page, both will be moved to the next page. | default value. |
| `"false"` | | | NOT keep lines. | it allows Word to break the paragraph across page breaks if necessary to fit the content. | When `<w:keepLines>` tag is not used, we can think that it will NOT keep lines. (same effect of `<w:keepLines w:val="false">`) |

#### `<w:adjustRightInd>` -> `w:val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | adjust right indentation due to different windows size. | | |
| `"false"` | | | NOT adjust right indentation due to different windows size. | | |

#### `<w:adjustLeftInd>` -> `w:val` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | adjust left indentation due to different windows size. |
| `"false"` | | | NOT adjust left indentation due to different windows size. |

#### `<w:framePr>` -> `w:hRule` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"auto"` | | | determined based on the height of its contents. | | The value of `w:h` is ignored. |
| `"exact"` | | | height of frame must be exactly the value of `w:h` attribute. | | If the height of its content is larger than the value of `w:h` attribute, then its content will be overflowed. |
| `"atLeast"` | | | height of frame must be at least the value of `w:h` attribute. height of frame is the max of value of `w:h` attribute and height of its content. | | |

#### `<w:framePr>` -> `w:hAnchor` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"page"` | | | anchors the frame horizontally to the page margins (with absolute position). | | |
| `"text"` | | | anchors the frame horizontally to the flow of the surrounding text. | | |
| `"margin"` | | | anchors the frame horizontally to the page margins (with relative position) (left or right, depending on other positioning attributes). | | |
| `"column"` | | | anchors the frame horizontally to the column boundaries in a multicolumn layout (with relative position)| | |

#### `<w:tab>` -> `w:val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |

#### `<w:mirrorIndents>` -> `w:val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | | When this tag is present, Word will swap the left and right indent settings if the document or section is set to a right-to-left reading order.  | | 
| `"false"` | | | | Word will swap NOT the left and right indent settings  | |

#### `<w:characterSpacingControl>` -> `w:val` attribute
> [!IMPORTANT]
> The available value of `w:val` attribute in `<w:characterSpacingControl>` is defined in `ST_CharacterSpacing` simple type, possible value listed in [Character-Level Whitespace Compression Settings](https://c-rex.net/samples/ooxml/e1/Part4/OOXML_P4_DOCX_ST_CharacterSpacing_topic_ID0E6AK2.html)

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `dontCompress` | | Don't Compress | specifies that no character compression shall be applied to any character when the document is displayed.  | | |
| `doNotCompress` | Do not Compress | specifies that characters shall not have whitespace compression applied to them | 
| `compressPunctuation` | | Compress Punctuation | specifies that only whitespace characters shall have whitespace compression applied to them. | | |
| `compressPunctuationAndJapaneseKana` | Compress Punctuation and Japanese kana (日本的假名) | specifies that whitespace and Japanese kana characters shall have whitespace compression applied to them. |

#### `<w:spacing>` -> `w:lineRule` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `auto` | | | automatically adjusts the line spacing based on the font size and any other formatting of the text within the lines. | | | 
| `exact` | | | line spacing will be exactly the value specified in the w:line attribute, regardless of the font size or other elements on the line | | | 
| `atLeast` | | | line spacing will be at least the value specified in the w:line attribute | | | 

#### `<w:tab>` -> `w:val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `left` | | left-aligned | The text that flows into the tab stop will be left-aligned at that position. | |
| `right` | | right-aligned | The text that flows into the tab stop will be right-aligned at that position. | |
| `center` | | center-aligned | The text that flows into the tab stop will be center-aligned at that position. | |
| `decimal` | | decimal point | Numbers will be aligned by their decimal point. | |
| `bar` | | tab-bar | A vertical line (i.e. tab bar) will be inserted at the tab stop position | |
| `clear` | | clear | Removes a previously defined tab stop at the specified position. | |

#### `<w:tcW>` -> `w:type` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `dxa` | | dxa | its unit is dxa equivalent to twips (i.e. twentieth of a point) | | |
| `pct` | | percentage | This indicates that the width is specified as a percentage of the table's overall width. | <ol><li>pct stands for *p*er*c*en*t*ge</li><li>The value in the `w:w` attribute is interpreted as fiftieths of a percent.</ol> | |
| `auto` | | auto | Word will automatically determine the width of the table cell based on its content and the overall table layout. | the value in the `w:w` attribute is typically ignored. | |
| `nil` | | nil | the value is explicitly set to zero (even if the `w:w` is not set to zero) | | |

#### `<w:tab>` -> `w:leader` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `none` | | nothing | No leader character | default value when not specified | |
| `dot` | | dot | dot (i.e. `.`) as leader character | | |
| `hyphen` | | hyphen | hyphen (i.e. `-`) as leader character | | |
| `underscore` | | underscore | underscore (i.e. `_`) as leader character | | |
| `middleDot` | | middle dot | middle dot (i.e. `·`) as leader character | | |

#### `<w:instrText>` -> `xml:space` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"default"` | | | The XML processor handles whitespace according to the default rules (collapsing sequences of whitespace characters into a single space, removing leading and trailing whitespace). | | |
| `"preserve"` | | | All whitespace characters within the element are preserved exactly as they appear in the XML. This is crucial for field instructions because the spaces and formatting within the instruction text often have semantic meaning. | | |

#### field instruction in `<w:instrText>`
| available field instruction in tag | description | notes | notice |
| :---------- | :----------- | :----- | :--- |
| About `Page Numbers` | | | |
| `PAGE` | Displays the current page number. | | |
| `NUMPAGES` | Displays the total number of pages in the document. | | |
| `SECTIONPAGES` | Displays the total number of pages in the current section. | | |
| `PAGE \* MERGEFORMAT` | preserves formatting applied to the field result, even if it is refreshed. | | |
| About `Dates and Times` | | | |
| `DATE` | Displays the current date. | | |
| `TIME` | Displays the current time. | | |
| `DATE \@ "MMMM d, yyyy"` | Displays the date in a specific format (e.g., "April 19, 2025"). | The `\@` switch controls the formatting. | |
| About `Document Information` | | | |
| `TITLE` | Displays the document title (from File > Info). | | |
| `AUTHOR` | Displays the document author. | | |
| `FILENAME` | Displays the document's file name. | | |
| About `Table of Contents` | | | |
| `TOC \o "1-3" \h \z \u` |  A complex instruction that generates a table of contents based on heading styles 1 through 3. | The `\o`, `\h`, `\z`, `\u` switches control various aspects of the TOC generation. | |
| About `Cross-references` | | | |
| `REF _RefID \h` | Creates a hyperlink to the element with the bookmark `_RefID` | The `\h` switch makes it a hyperlink. | |
| About `Mail Merge Fields` | | | |
| `MERGEFIELD FirstName` | Inserts the data from the "FirstName" column of the mail merge data source. | | |
| About `Mail Merge Fields` | | | |

> [!IMPORTANT]
> It is better to understand the syntax and field instruction about `<w:instrText>`.
>
> For more details, see [syntax of `field instruction` in `<w:instrText>` tag](https://github.com/40843245/OOXML/blob/main/Word/structure/CH1%20--%20syntax.md#syntax-of-field-instruction-in-winstrtext-tag)

#### `<w:fldChar>` -> `w:fldCharType` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `begin` | | | It marks the beginning of the field's instructions and result. | | |
| `separate` | | | It divides the field's instructions (the code that tells Word what to do) from the field's result (the currently displayed output). | | Not all fields have a `separate` character.|
| `end` | | | It marks the end of a field, concluding both the instructions and the result (if present). | | |

#### `<w:footnote>` -> `w:type` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"normal"` | | | indicates a standard footnote | | it is default value. |
| `"separator"` | | | specifies a footnote separator | | there MUST be at most one `"separator"` in `footnotes` part (inside parent element `<w:footnotes>`). |
| `"continuationSeparator"` | | | specifies a footnote continuation separator | | same as above. |
| `"continuationNotice"` | | | specifies a footnote continuation notice | | same as above. |

#### `<w:footerReference>` -> `w:type` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"default"` | | | applies the footer to any pages (first page, odd-numbered pages, and even-numbered pages) | | it is default value. |
| `"first"` | | | applies the footer to first page  | | |
| `"even"` | | | applies the footer to even-numbered pages | | |

#### `<w:hyperlink>` -> `w:history` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | the hyperlink has been visited. | | |
| `"false"` | | | the hyperlink has **NOT** been visited. | | |

#### `<w:docGrid>` -> `w:linePitch` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `lines` | | | The grid controls the vertical spacing of lines. | | |
| `snapToChars` | | | The grid aligns to character boundaries. | | |
| `fixed` | | | A fixed horizontal and vertical grid. | | |

#### `<w:plt>` -> `w:val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"SingleLevel"`| | single-level | says that it is a single-level list | | |
| `"MultiLevel"`| | multi-level | says that it is a multi-level list | | |

#### `<w:footnote>` -> `w:id` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| positive integer | | | Used for regular footnotes. | | |
| `"-1"` | | | used to identify the footnote separator. | | |
| `"0"` | | | used to identify the footnote continuation separator (the separator shown when footnotes span multiple pages). | | |
| (sometimes `"1"`) or another negative number  | | | (sometimes) or another negative number  | | |

#### `<w:footnote>` -> `w:type` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"normal"` | | |  Indicates a regular footnote containing content. | | |
| `"separator"` | | |  Indicates a footnote separator line. | | |
| `"continuationSeparator"` | | | Indicates a footnote continuation separator line. | | |
| `"continuationNotice"` | | |  Indicates the footnote continuation notice text. | | |

#### `<w:footnote>` -> `w:numFmt` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"decimal"` | | | (1, 2, 3, ...) | | |
| `"upperRoman"` | | | (I, II, III, ...) | | |
| `"lowerRoman"` | | | (i, ii, iii, ...) | | |
| `"upperLetter"` | | | (A, B, C, ...) | | |
| `"lowerLetter"` | | | (a, b, c, ...) | | |
| `"ordinal"` | | | (1st, 2nd, 3rd, ...) | | |
| `"cardinalText"` | | | (One, Two, Three, ...) | | |
| `"ordinalText"` | | | (First, Second, Third, ...) | | |

#### `<w:footnote>` -> `w:restart` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | Footnote numbering continues from the previous section. | | |
| `"false"` | | | Footnote numbering restarts at the beginning of the current section. | | |

#### `<w:start>` -> `w:val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"1"`| | | first item at this list level will be numbered or lettered starting from 1 (or equivalent corresponding symbol with different number formatting) | | |
| etc | | | | | |

#### `<w:lvlJs>` -> `w:val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"left"` | | left-aligned | this item will be left-aligned | In newer version (Microsoft Office 2007 or above), it is obsolete. It uses `"start"`. See above for more reason. | |
| `"start"` | | aligned from start (left-aligned in horizontal orientation, or top-aligned in vertical orientation) | this item will be aligned from start | This value is used at first release of `OOXML` which is implemented in Microsoft Word 2007. Thus, we can say that in Microsoft Office 2007, it uses `"start"` instead of `"left"` (which is obsolete) | |
| `"right"` | | right-aligned | this item will be right-aligned | In newer version (Microsoft Office 2007 or above), it is obsolete. It uses `"end"`. See above for more reason. | |
| `"end"` | | aligned from end (right-aligned in horizontal orientation, or bottom-aligned in vertical orientation) | this item will be aligned from end | This value is used at first release of `OOXML` which is implemented in Microsoft Word 2007. Thus, we can say that in Microsoft Office 2007, it uses `"end"` instead of `"right"` (which is obsolete) | |
| `"center"` | | center-aligned | this item will be center-aligned | | |
| `"both"` | | | justifies the text of the numbering symbol (if it were more than one character) between both margins.  | However, this does not affect inter-character spacing. | |
| `"distribute"` | | | justifies the text of the numbering symbol (if it were more than one character) between both margins.  | To achieve even distribution (i.e. with same space), it will affect both inter-word and inter-character spacing | |

#### `<w:numFmt>` -> `w:val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"decimal"` | | decimal number | the item in the list level will be numbered by number (for example, the list starts witg `1`, `2`, `3`, and so on. | | |
| `"lowerRoman"` | | lowercase roman number | the item in the list level will be numbered by lowercase of roman number (for example, the list starts with `i`, `ii`, `iii`, and so on. | | |
| `"upperRoman"` | | uppercase roman number | the item in the list level will be numbered by uppercase of roman number (for example, the list starts with `I`, `II`, `III`, and so on. | | |
| `"lowerLetter"` | | lowercase alphabet | the item in the list level will be numbered by lowercase of alphabet (for example, the list starts from `a`, `b`, `c`, and so on. | | |
| `"upperLetter"` | | uppercase alphabet | the item in the list level will be numbered by uppercase of alphabet (for example, the list starts from `A`, `B`, `C`, and so on. | | |
| `"bullet"` | | bullet | the item in the list level will be lettered by bullet character (for example, the list starts from `●`, `●`, `●`, and so on. | | |
| `"none"` | | nothing | the item in the list level will be listed without use of number, lettering, bullet character etc.  | | |

#### `<w:lvl>` -> `w:ilvl` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"0"` | | | defines the formatting for the first level of the list.  | zero-based | | 
| `"1"` | | |  defines the top-most or first level of the list.| | | 
| etc | | | | | | 

#### `<w:bdr>` -> `w:val` attribute
> [!IMPORTANT]
> About `Art Border Styles`, they can always be used in `w:val` attribute inside page border elements (`<w:top>`,`<w:left>`,`<w:bottom>`,`<w:right>`).
>
> While, they sometimes could not be used in in `w:val` attribute in line border elements (`<w:bdr>`). It depends on the context.

> [!IMPORTANT]
> Due to
>
> 1. there are so many Art Border Styles and
> 2. some may be deprecated even removed or added in different version of Microsoft Office Word.
>
> I only list them which appears on the earlier version than Microsoft Office Word 2003.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| Line Border Styles | | | | | |
| `"nil"` | | nil | no border | | | 
| `"none"` | | none | no border | equivalent to `""nil` | | 
| `"single"` | | single | a single solid line | | | 
| `"thick"` | | thick | a thicker single solid line | | | 
| `"double"` | | double | a double solid line | | | 
| `"dotted"` | | dotted | a dotted line | | | 
| `"dashed"` | | dashed | a dashed line with larger gaps | | | 
| `"dotDash"` | | dot, dash | a line with alternating dots and dashes. | | | 
| `"dotDotDash"` | | dot, dot, dash | a line with repeating pattern -- dot, dot, dash. | | | 
| `"mediumDashed"` | | | a dashed line with medium thickness dashes. | | | 
| `"mediumDashDot"` | | | a line with alternating medium dashes and meduim dots. | | | 
| `"mediumDashDotDot"` | | | a line with repeating pattern -- meduim dash, meduim dot, meduim dot. | | | 
| `"slantDashDot"` | | | a line with alternating slanting dashes and slanting dots. | | | 
| `"triple"` | | triple | three parallel solid lines. | | | 
| `"wave"` | | wave | a single wavy line. | | | 
| `"doubleWave"` | | double wave | a double wavy line. | | | 
| `"dashSmallGap"` | | | a dashed line with smaller gaps. | | | 
| `"dashDotStroked"` | | | a line with alternating thin and thick dashes. | | | 
| `"threeDEmboss"` | | |  a border that appears embossed (raised) | | | 
| `"threeDEngrave"` | | | a border that appears engraved (sunken). | | | 
| `"outset"` | | | a border that appears to be outside the frame. | | | 
| `"inset"` | | | a border that appears to be inside the frame. | | | 
| `"hair"` | | hairline |  a hairline (i.e. a very thin line). | | | 
| `"thinThickSmallGap"` | | | a thin line, a thick line, and another thin line, with small gaps. | | | 
| `"thickThinSmallGap"` | | | a thick line, a thin line, and another thick line, with small gaps. | | | 
| `"thinThickThinSmallGap"` | | | a thin line, a thick line, and a thin line, with small gaps. | | | 
| `"thinThickMediumGap"` | | | a thin line, a thick line, and another thin line, with medium gaps. | | | 
| `"thickThinMediumGap"` | | | a thick line, a thin line, and another thick line, with medium gaps. | | | 
| `"thinThickThinMediumGap"` | | | a thin line, a thick line, and a thin line, with medium gaps. | | |
| `"thinThickLargeGap"` | | | a thin line, a thick line, and another thin line, with large gaps. | | | 
| `"thickThinLargeGap"` | | | a thick line, a thin line, and another thick line, with large gaps. | | | 
| `"thinThickThinLargeGap"` | | | a thin line, a thick line, and a thin line, with large gaps. | | |
| | | | | | |
| Art Border Styles | | | | | |
| `"apples"` | | | a border made of repeating apple illustrations. | | |
| `"archedScallops"` | | | a border with a repeating arched scallop design | | |
| `"babyPacifier"` | | | a border featuring repeating baby pacifier images | | |
| `"babyRattle"` | | | a border with repeating baby rattle illustrations | | |
| `"balloons3Colors"` | | | a border with a repeating arched scallop design | | |
| `"bats"` | | | a border with repeating bat silhouettes | | |
| `"birds"` | | | a border featuring repeating bird illustrations | | |
| `"cakeSlice"` | | | a border with repeating slices of cake. | | |
| `"candyCorn"` | | | a border made of repeating candy corn images | | |
| `"celticKnotwork"` | | | a border with an intricate, repeating Celtic knot design. | | |
| `"certificateBanner"` | | | a border resembling a decorative banner often found on certificates. | | |
| `"chamomile"` | | | a border featuring repeating chamomile flower illustrations. | | |
| `"christmasTree"` | | | a border made of repeating Christmas tree images. | | |
| `"circles"` | | | a border with repeating circular shapes. | | |
| `"clover"` | | | a border featuring repeating clover leaves. | | |
| `"compass"` | | | a border with repeating compass rose illustrations. | | |
| `"confetti"` | | | a border that looks like scattered confetti. | | |
| `"cornerClusters"` | | | a border with decorative clusters in the corners. | | |
| `"couponCutoutDashes"` | | | a border that resembles a cutout line on a coupon, made of dashes. | | |
| `"couponCutoutDots"` | | | a border that resembles a cutout line on a coupon, made of dots. | | |
| `"crossStitch"` | | | a border that looks like a cross-stitch pattern | | |
| `"decoArch"` | | | a border with a repeating decorative arch design. | | |
| `"decoBlock"` | | | a border made of repeating decorative rectangular blocks. | | |
| `"diamonds"` | | | a border with repeating diamond shapes. | | |
| `"dogPawPrints"` | | | a border featuring repeating dog paw prints. | | |
| `"doubleD"` | | | a border with a repeating "D" shape, often interlocked or doubled. | | |
| `"downDiamonds"` | | | a border with repeating diamond shapes pointing downwards. | | |
| `"dragons"` | | | a border featuring repeating dragon illustrations. | | |
| `"easterEggs"` | | | a border made of repeating Easter egg images | | |
| `"edgeOfTheWorld"` | | | a border with a design that evokes a landscape or horizon. | | |
| `"elephants"` | | | a border featuring repeating elephant illustrations. | | |
| `"fence"` | | | a border that looks like a repeating fence pattern. | | |
| `"fireworks"` | | | a border with repeating firework burst illustrations. | | |
| `"flowersMultiple"` | | | a border featuring repeating illustrations of multiple flowers. | | |
| `"flowersSingle"` | | | a border with repeating illustrations of a single type of flower. | | |
| `"follyBalloon"` | | | a border with repeating whimsical balloon illustrations. | | |
| `"grapes"` | | | a border made of repeating grape illustrations. | | |
| `"groovy"` | | | a border with a retro, wavy, or psychedelic design. | | |
| `"hearts"` | | | a border featuring repeating heart shapes | | |
| `"heirloom"` | | | a border with a traditional or antique-looking design. | | |
| `"holly"` | | | a border made of repeating holly leaves and berries, often used for Christmas themes. | | |
| `"houseFunky"` | | | a border with repeating stylized or whimsical house illustrations. | | |
| `"hypnotic"` | | | a border with a repeating pattern that creates a visually mesmerizing or swirling effect. | | |
| `"iceCreamCones"` | | | a border featuring repeating ice cream cone illustrations. | | |
| `"lightBulb"` | | | a border with repeating light bulb illustrations. | | |
| `"lightning1"` | | | a border made of repeating lightning bolt shapes (style 1). | | |
| `"lightning2"` | | | a border made of repeating lightning bolt shapes (style 2). | possibly different from `lightning1`. | |
| `"mapPins"` | | | a border featuring repeating map pin icons. | | |
| `"marquee"` | | | a border that resembles a decorative marquee or ribbon. | | |
| `"marqueeToothed"` | | | a marquee-style border with a toothed or jagged edge. | | |
| `"moons"` | | | a border with repeating moon illustrations. | | |
| `"mosaic"` | | | a border that looks like a repeating mosaic tile pattern. | | |
| `"musicNotes"` | | | a border featuring repeating musical note symbols. | | |
| `"northwest"` | | | a border with a design that might evoke a Northwestern or geometric style. | | |
| `"ornaments1"` | | | a border made of repeating decorative ornaments (style 1). | | |
| `"ornaments2"` | | | a border made of repeating decorative ornaments (style 2). | possibly different from `ornaments1` | |
| `"paperClips"` | | | a border featuring repeating paper clip illustrations. | | |
| `"pencils"` | | | a border with repeating pencil illustrations. | | |
| `"people"` | | | a border featuring repeating stylized human figures. | | |
| `"peopleWaving"` | | | a border with repeating illustrations of people waving. | | |
| `"pineTrees"` | | | a border made of repeating pine tree illustrations. | | |
| `"puzzlePieces"` | | | a border with repeating jigsaw puzzle piece shapes. | | |
| `"pyramids"` | | | a border featuring repeating pyramid shapes. | | |
| `"rings"` | | | a border made of repeating ring shapes. | | |
| `"romanArc"` | | | a border with a repeating Roman arch design. | | |
| `"rose"` | | | a border featuring repeating rose illustrations. | | |
| `"sawtooth"` | | | a border with a repeating jagged, tooth-like edge | | |
| `"shootingStar"` | | | a border with repeating shooting star illustrations. | | |
| `"snowflake"` | | | a border made of repeating snowflake illustrations. | | |
| `"southwest"` | | | a border with a design that might evoke a Southwestern or geometric style. | | |
| `"stars"` | | | a border featuring repeating star shapes. | | |
| `"starsTop"` | | | a border with repeating stars, possibly positioned along the top edge. | | |
| `"sun"` | | | a border with repeating sun illustrations. | | |
| `"swirlArrows"` | | | a border made of repeating swirling arrow shapes. | | |
| `"swordArrows"` | | | a border with repeating sword and arrow illustrations. | | |
| `"treeBalloon"` | | | a border featuring repeating illustrations of trees shaped like balloons. | | |
| `"triangleParty"` | | | a border made of repeating triangles in a festive arrangement. | | |
| `"triangles"` | | | a border with repeating triangular shapes. | | |
| `"twistedLines1"` | | | a border with repeating twisted line designs (style 1). | | |
| `"twistedLines2"` | | | a border with repeating twisted line designs (style 2). | possibly different from `twistedLines1` | |
| `"vine"` | | | a border featuring repeating vine or leaf illustrations. | | |
| `"mapPins"` | | | a border featuring repeating map pin icons. | | |
| `"wavyDouble"` | | | a border with two parallel wavy lines. | | |
| `"wavyLine"` | | | a single wavy line. | | |
| `"weavedmat"` | | | a border that looks like a repeating woven mat pattern. | | |
| `"zigzag"` | | | a border featuring repeating map pin icons. | | |

#### `<w:pgBorders>` -> <w:top> -> `w:val` attribute
Same as `<w:bdr>` -> `w:val` attribute.

#### `<w:pgBorders>` -> <w:left> -> `w:val` attribute
Same as `<w:bdr>` -> `w:val` attribute.

#### `<w:pgBorders>` -> <w:right> -> `w:val` attribute
Same as `<w:bdr>` -> `w:val` attribute.

#### `<w:pgBorders>` -> <w:down> -> `w:val` attribute
Same as `<w:bdr>` -> `w:val` attribute.

#### `<w:bdr>` -> `w:color` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"auto"` | | auto | automatic color | | |
| `"<RGB>"` | | rgb color | should be a string consist of six hexadecimal digit.</br>The value indicates its rgb color. | `#` symbol is not used for color elements in OOXML. | |

#### `<w:bdr>` -> `w:themeColor` attribute
Ranging is same as `<w:bdr>` -> `w:color` attribute.

But the value indicates its theme color.

#### `<w:bdr>` -> `w:themeTint` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"<lightness>"` | | lightness | should be a string consist of two hexadecimal digit.</br>The value indicates the lightness of theme color.</br>`00`: darkest</br>`FF`: lightest | `#` symbol is not used for color elements in OOXML. | |

#### `<w:bdr>` -> `w:themeShade` attribute
Ranging is same as `<w:bdr>` -> `w:themeTint` attribute.

But the value indicates its theme shade.

#### `<w:bdr>` -> `w:frame` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | true | should have frame effect | | |
| `"false"` | | false | should **NOT** have frame effect | default value | |

#### `<w:bdr>` -> `w:shadow` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | true | should have shadow effect | | |
| `"false"` | | false | should **NOT** have shadow effect | default value | |

#### `<w:pgBorders>` -> `w:display` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"allPages"` | | all pages | the page borders defined for the section should be displayed on every page within that section. | default value | |
| `"firstPage"` | | first page | the page borders defined for the section should be displayed on the first page of the current section. | | |
| `"notFirstPage"` | | not first pages | the page borders defined for the section should be displayed on every page (except first page) within that section. | | |

#### `<w:pgBorders>` -> `w:offsetFrom` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"page"` | | page | the `w:space` attribute of the individual border elements (`<w:top>`, `<w:left>`, `<w:bottom>`, `<w:right>`) is interpreted as the distance from the **edge of the page** to the beginning of the border.  | | |
| `"text"` | | text | the `w:space` attribute of the individual border elements (`<w:top>`, `<w:left>`, `<w:bottom>`, `<w:right>`) is interpreted as the distance from the **text margins** to the beginning of the border.  | | |

> [!NOTE]
> `w:offsetFrom` determines the reference point from which the spacing of the page borders is measured.
>
> Choosing `page` makes the border spacing absolute relative to the paper's edges.
>
> While choosing `text` makes it relative to the document's text boundaries, which are defined by the page margins.

#### `<w:pgBorders>` -> `w:zOrder` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"front"` | | |  the page border should be rendered **above** any intersecting text and other objects on the page. | default value | |
| `"back"` | | |  the page border should be rendered **below** any intersecting text and other objects on the page. | | |

#### `<w:latentStyles>` -> `w:defLockedState` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | | indicates new latent styles are locked by default and harder to be modified. | | |
| `"false"` | | | | indicates new latent styles are **NOT** locked by default and can be modified. | | |

#### `<w:latentStyles>` -> `w:defUnhideWhenUsed` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"`| | | | indicates that if a latent style is actually used in the document content, it will become visible in the user interface. | This allows styles that are relevant to the content to appear when needed. | |
| `"false"` | | | | indicates that if a latent style is actually used in the document content, it will **NOT** become visible in the user interface. | | |

#### `<w:latentStyles>` -> `w:defQFormat` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | | indicates that new latent styles will appear in the Quick Styles gallery by default. |  | |
| `"false"`| | | | indicates that new latent styles will **NOT** appear in the Quick Styles gallery by default. | | |

#### `<w:lsdException>` -> `w:name` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"No List"` | | | | | |
| `"Title"` | | | | | |
| `"Subtitle"` | | | | | |
| `"Normal"` | | | | | |
| `"Outline List 1"` | | | | | |
| `"Outline List 2"` | | | | | |
| `"Outline List 3"` | | | | | |
| `"Outline List 4"` | | | | | |
| `"Outline List 5"` | | | | | |
| `"Outline List 6"` | | | | | |
| `"Outline List 7"` | | | | | |
| `"Outline List 8"` | | | | | |
| `"Outline List 9"` | | | | | |
| `"Heading 1"` | | | | | |
| `"Heading 2"` | | | | | |
| `"Heading 3"` | | | | | |
| `"Heading 4"` | | | | | |
| `"Heading 5"` | | | | | |
| `Heading 6"` | | | | | |
| `"Heading 7"` | | | | | |
| `"Heading 8"` | | | | | |
| `"Heading 9"` | | | | | |
| `"Numbering 1"` | | | | | |
| `"Numbering 2"` | | | | | |
| `"Numbering 3"` | | | | | |
| `"Numbering 4"` | | | | | |
| `"Numbering 5"` | | | | | |
| `Numbering 6"` | | | | | |
| `"Bullet 1"` | | | | | |
| `"Bullet 2"` | | | | | |
| `"Bullet 3"` | | | | | |
| `"Bullet 4"` | | | | | |
| `"Bullet 5"` | | | | | |
| `Bullet 6"` | | | | | |

#### `<w:lsdException>` -> `w:semiHidden` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | | | indicates that the style is semi-hidden. it will be invisible unless it's actively in use in the document. | | |
| `"false"` | | | | indicates that the style is **NOT** semi-hidden and will be visible in the Styles pane. | | |

### about `m` namespace
#### `<m:brkBin>` -> `m:val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"before"` | | | If a line break is necessary in an expression with a binary operator, the binary operator should be **at the beginning of the new line.** | | | 
| `"after"` | | | If a line break is necessary in an expression with a binary operator, the binary operator should be **at the end of the preceeding line.** | | | 

#### `<m:smallFrac>` -> `m:val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"on"` | | | fractions appearing within the text would typically be rendered with a smaller font size for the numerator and denominator, and possibly a shorter fraction bar, to better integrate with the line height of the surrounding text. | | | 
| `"off"` | | |  fractions will be displayed in their full size, even when they are part of the regular text flow. | | | 

#### `<m:defJc>` -> `m:val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"left"` | | left-aligned | default settings of math equation is left-aligned | | | 
| `"right"` | | right-aligned | default settings of math equation is right-aligned | | | 
| `"center"` | | center-aligned | default settings of math equation is center-aligned | | | 
| `"inside"` | | | default settings of math equation is aligned inside the page | For left-to-right languages, this is equivalent to `"left"`.</br>For right-to-left languages, it's equivalent to `"right"` | | 
| `"outside"` | | | opposite of the value `"inside"` | For left-to-right languages, this is equivalent to `"right"`.</br>For right-to-left languages, it's equivalent to `"left"` | | 
| `"centerGroup"` | | center group | default settings of math equation is center-aligned and applied for a group of element (such as numerator is a fraction) | | <ol><li> It is not a standard option on native OOXML.</li><li>the presence of centerGroup strongly implies a scenario are:<ul><li>Math elements are treated as groups or columns within a larger structure.</li><li>The justification is applied to ensure these groups or columns are centered relative to each other or some central axis within the math zone.</li></ul></li></ol>| 

#### `<m:intLim>` -> `m:val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `undOvr` | | *und*er, *ov*e*r* | indicates that lower limit and upper limit of integration operators should be displayed in the **under-over position**,</br>meaning that the lower limit is placed below the integral symbol and the upper limit is placed above it. This is the more traditional and common way of displaying integral limits. | | | |
| `subSup` | | *sub*-script, *sup*er-script | indicates that lower limit and upper limit of integration operators should be displayed in the **subscript-superscript position**,</br>meaning that the lower limit is placed as a subscript and the upper limit as a superscript to the integral symbol.</br>This is often used for inline integrals or when space is constrained. | | | |

> [!NOTE]
>
> See [`<m:intLim>` tag (OOXML docs)](https://c-rex.net/samples/ooxml/e1/Part4/OOXML_P4_DOCX_intLim_topic_ID0EVMUZB.html?hl=intlim) for more information.

#### `<m:naryLim>` -> `m:val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `undOvr` | | *und*er, *ov*e*r* | specifies that the limit of n-ary operators should be displayed in the **under-over position** | | |
| `subSup` | | *sub*-script, *sup*er-script | indicates limit of n-ary operators should be displayed in the **subscript-superscript position**. | | | |

> [!NOTE]
> See [`<m:naryLim>` tag (OOXML docs)](https://c-rex.net/samples/ooxml/e1/Part4/OOXML_P4_DOCX_naryLim_topic_ID0EZ43ZB.html) for more information.
