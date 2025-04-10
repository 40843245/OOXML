# Appendix 2 -- available options of attribute of tag in xml for Word
## tables
> [!WARNING]
> Most content of these table are refered from Google Gemini's answer or from non-official website, which BOTH may be incorrect.
>
> Read with caution.

### `xml:space` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"preserve"` | | preserve | whitespace (i.e. ` `, `\t`, and `\n`) within the element's content should be preserved exactly as it appears in the XML source. The application processing the XML should not normalize or remove any of this whitespace. | | | 
| `"default"` | | default processing (not fully preserve) | Default whitespace handling of the XML processor should be applied to the content of this element. | See following for more details. | | 

> [!NOTE]
> If the `xml:space` attribute is not specified,
>
> it will use the value of the attribute in parent node (if it has a parent), or
>
> it usually use `"default"` value (if it has not parent (i.e. it is a root node)).

> [!NOTE]
> Typically, XML processor will handle the whitespace through normalization by default (if the whitespace should not be fully preserved).
> 
> Normalizing the whitespace involves these steps:
>
> + Collapsing sequences of whitespace characters into a single space.
> + Removing leading and trailing whitespace.
> + Treating line breaks as whitespace.

### `<w:tab>` -> `w:val` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `left` | | left-aligned | The text that flows into the tab stop will be left-aligned at that position. | |
| `right` | | right-aligned | The text that flows into the tab stop will be right-aligned at that position. | |
| `center` | | center-aligned | The text that flows into the tab stop will be center-aligned at that position. | |
| `decimal` | | decimal point | Numbers will be aligned by their decimal point. | |
| `bar` | | tab-bar | A vertical line (i.e. tab bar) will be inserted at the tab stop position | |
| `clear` | | clear | Removes a previously defined tab stop at the specified position. | |

### `<w:tcW>` -> `w:type` attribute
#### available options of attribute in tag

> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `dxa` | | dxa | its unit is dxa equivalent to twips (i.e. twentieth of a point) | | |
| `pct` | | percentage | This indicates that the width is specified as a percentage of the table's overall width. | <ol><li>pct stands for *p*er*c*en*t*ge</li><li>The value in the `w:w` attribute is interpreted as fiftieths of a percent.</ol> | |
| `auto` | | auto | Word will automatically determine the width of the table cell based on its content and the overall table layout. | the value in the `w:w` attribute is typically ignored. | |
| `nil` | | nil | the value is explicitly set to zero (even if the `w:w` is not set to zero) | | |

### `<w:tab>` -> `w:leader` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `none` | | nothing | No leader character | default value when not specified | |
| `dot` | | dot | dot (i.e. `.`) as leader character | | |
| `hyphen` | | hyphen | hyphen (i.e. `-`) as leader character | | |
| `underscore` | | underscore | underscore (i.e. `_`) as leader character | | |
| `middleDot` | | middle dot | middle dot (i.e. `·`) as leader character | | |

### `<w:docGrid>` -> `w:linePitch` attribute
#### available options of attribute in tag

> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `lines` | | | The grid controls the vertical spacing of lines. | | |
| `snapToChars` | | | The grid aligns to character boundaries. | | |
| `fixed` | | | A fixed horizontal and vertical grid. | | |

### `<w:plt>` -> `w:val` attribute
#### available options of attribute in tag
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"SingleLevel"`| | single-level | says that it is a single-level list | | |
| `"MultiLevel"`| | multi-level | says that it is a multi-level list | | |

### `<w:start>` -> `w:val` attribute
#### available options of attribute in tag
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"1"`| | | first item at this list level will be numbered or lettered starting from 1 (or equivalent corresponding symbol with different number formatting) | | |

### `<w:lvlJs>` -> `w:val` attribute
#### available options of attribute in tag
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"left"` | | left-aligned | this item will be left-aligned | In newer version (Microsoft Office 2007 or above), it is obsolete. It uses `"start"`. See above for more reason. | |
| `"start"` | | aligned from start (left-aligned in horizontal orientation, or top-aligned in vertical orientation) | this item will be aligned from start | This value is used at first release of `OOXML` which is implemented in Microsoft Word 2007. Thus, we can say that in Microsoft Office 2007, it uses `"start"` instead of `"left"` (which is obsolete) | |
| `"right"` | | right-aligned | this item will be right-aligned | In newer version (Microsoft Office 2007 or above), it is obsolete. It uses `"end"`. See above for more reason. | |
| `"end"` | | aligned from end (right-aligned in horizontal orientation, or bottom-aligned in vertical orientation) | this item will be aligned from end | This value is used at first release of `OOXML` which is implemented in Microsoft Word 2007. Thus, we can say that in Microsoft Office 2007, it uses `"end"` instead of `"right"` (which is obsolete) | |
| `"center"` | | center-aligned | this item will be center-aligned | | |
| `"both"` | | | justifies the text of the numbering symbol (if it were more than one character) between both margins.  | However, this does not affect inter-character spacing. | |
| `"distribute"` | | | justifies the text of the numbering symbol (if it were more than one character) between both margins.  | To achieve even distribution (i.e. with same space), it will affect both inter-word and inter-character spacing | |

### `<w:numFmt>` -> `w:val` attribute
#### available options of attribute in tag
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"decimal"` | | decimal number | the item in the list level will be numbered by number (for example, the list starts witg `1`, `2`, `3`, and so on. | | |
| `"lowerRoman"` | | lowercase roman number | the item in the list level will be numbered by lowercase of roman number (for example, the list starts with `i`, `ii`, `iii`, and so on. | | |
| `"upperRoman"` | | uppercase roman number | the item in the list level will be numbered by uppercase of roman number (for example, the list starts with `I`, `II`, `III`, and so on. | | |
| `"lowerLetter"` | | lowercase alphabet | the item in the list level will be numbered by lowercase of alphabet (for example, the list starts from `a`, `b`, `c`, and so on. | | |
| `"upperLetter"` | | uppercase alphabet | the item in the list level will be numbered by uppercase of alphabet (for example, the list starts from `A`, `B`, `C`, and so on. | | |
| `"bullet"` | | bullet | the item in the list level will be lettered by bullet character (for example, the list starts from `●`, `●`, `●`, and so on. | | |
| `"none"` | | nothing | the item in the list level will be listed without use of number, lettering, bullet character etc.  | | |

### `<w:lvl>` -> `w:ilvl` attribute

> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"0"` | | | defines the formatting for the first level of the list.  | zero-based | | 
| `"1"` | | |  defines the top-most or first level of the list.| | | 
| etc | | | | | | 

### `<w:bdr>` -> `w:val` attribute

> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
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

### `<w:pgBorders>` -> `w:display` attribute

> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"allPages"` | | all pages | the page borders defined for the section should be displayed on every page within that section. | default value | |
| `"firstPage"` | | first page | the page borders defined for the section should be displayed on the first page of the current section. | | |
| `"notFirstPage"` | | not first pages | the page borders defined for the section should be displayed on every page (except first page) within that section. | | |

### `<w:pgBorders>` -> `w:offsetFrom` attribute

> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

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

### `<w:pgBorders>` -> `w:zOrder` attribute

> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"front"` | | |  the page border should be rendered **above** any intersecting text and other objects on the page. | default value | |
| `"back"` | | |  the page border should be rendered **below** any intersecting text and other objects on the page. | | |
