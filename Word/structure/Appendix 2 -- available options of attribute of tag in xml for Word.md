# Appendix 2 -- available options of attribute of tag in xml for Word
## tables
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
| :---------- | :----------- | :----- | :--- | :-- | :-- |

### `<w:lvl>` -> `w:ilvl` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"0"` | | | defines the formatting for the first level of the list.  | zero-based | | 
| `"1"` | | |  defines the top-most or first level of the list.| | | 
| etc | | | | | | 


> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"SingleLevel"` | | single level | indicates that this list definition is designed for a simple (or exactly siad, single-level) list. |  
