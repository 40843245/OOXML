# Appendix 2 -- available options of attribute of tag in xml for Word
## tables
> [!WARNING]
> Most content of these table are refered from Google Gemini's answer or from non-official website, which BOTH may be incorrect.
>
> Read with caution.

### about `xml` namespace
#### `xml:space` attribute
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

### about `v` namespace
#### `v:ext` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"edit"` | | editable | indicates that the shapes are **fully** editable within Office app. | | |
| `"view"` | | editable | indicates that the shapes are **NOT fully** editable within Office app. i.e. can only view or is ediatble but some capabilities are limited. | | |
| `"backwardCompatible"` | | | indicates that the VML extension is intended for backward compatibility with older versions of applications. | | Newer editors should render it, and ideally, allow some level of editing, while older editors might ignore or render it in a basic way without full understanding of the extended features. |

### about `w` namespace
#### `<w:adjustRightInd>` -> `w:val` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

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
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"auto"` | | | determined based on the height of its contents. | | The value of `w:h` is ignored. |
| `"exact"` | | | height of frame must be exactly the value of `w:h` attribute. | | If the height of its content is larger than the value of `w:h` attribute, then its content will be overflowed. |
| `"atLeast"` | | | height of frame must be at least the value of `w:h` attribute. height of frame is the max of value of `w:h` attribute and height of its content. | | |

#### `<w:framePr>` -> `w:hAnchor` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"page"` | | | anchors the frame horizontally to the page margins (with absolute position). | | |
| `"text"` | | | anchors the frame horizontally to the flow of the surrounding text. | | |
| `"margin"` | | | anchors the frame horizontally to the page margins (with relative position) (left or right, depending on other positioning attributes). | | |
| `"column"` | | | anchors the frame horizontally to the column boundaries in a multicolumn layout (with relative position)| | |

#### `<w:tab>` -> `w:val` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |

#### `<w:characterSpacingControl>` -> `w:val` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

> [!IMPORTANT]
> The available value of `w:val` attribute in `<w:characterSpacingControl>` is defined in `ST_CharacterSpacing` simple type, possible value listed in [Character-Level Whitespace Compression Settings](https://c-rex.net/samples/ooxml/e1/Part4/OOXML_P4_DOCX_ST_CharacterSpacing_topic_ID0E6AK2.html)

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `dontCompress` | | Don't Compress | specifies that no character compression shall be applied to any character when the document is displayed.  | | |
| `doNotCompress` | Do not Compress | specifies that characters shall not have whitespace compression applied to them | 
| `compressPunctuation` | | Compress Punctuation | specifies that only whitespace characters shall have whitespace compression applied to them. | | |
| `compressPunctuationAndJapaneseKana` | Compress Punctuation and Japanese kana (日本的假名) | specifies that whitespace and Japanese kana characters shall have whitespace compression applied to them. |

#### `<w:tab>` -> `w:val` attribute
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

#### `<w:tcW>` -> `w:type` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `dxa` | | dxa | its unit is dxa equivalent to twips (i.e. twentieth of a point) | | |
| `pct` | | percentage | This indicates that the width is specified as a percentage of the table's overall width. | <ol><li>pct stands for *p*er*c*en*t*ge</li><li>The value in the `w:w` attribute is interpreted as fiftieths of a percent.</ol> | |
| `auto` | | auto | Word will automatically determine the width of the table cell based on its content and the overall table layout. | the value in the `w:w` attribute is typically ignored. | |
| `nil` | | nil | the value is explicitly set to zero (even if the `w:w` is not set to zero) | | |

#### `<w:tab>` -> `w:leader` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `none` | | nothing | No leader character | default value when not specified | |
| `dot` | | dot | dot (i.e. `.`) as leader character | | |
| `hyphen` | | hyphen | hyphen (i.e. `-`) as leader character | | |
| `underscore` | | underscore | underscore (i.e. `_`) as leader character | | |
| `middleDot` | | middle dot | middle dot (i.e. `·`) as leader character | | |

#### `<w:docGrid>` -> `w:linePitch` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

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

#### `<w:start>` -> `w:val` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"1"`| | | first item at this list level will be numbered or lettered starting from 1 (or equivalent corresponding symbol with different number formatting) | | |

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
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"0"` | | | defines the formatting for the first level of the list.  | zero-based | | 
| `"1"` | | |  defines the top-most or first level of the list.| | | 
| etc | | | | | | 

#### `<w:bdr>` -> `w:val` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

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
| `"false"` | | false | should not have frame effect | default value | |

#### `<w:bdr>` -> `w:shadow` attribute
| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"true"` | | true | should have shadow effect | | |
| `"false"` | | false | should not have shadow effect | default value | |

#### `<w:pgBorders>` -> `w:display` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"allPages"` | | all pages | the page borders defined for the section should be displayed on every page within that section. | default value | |
| `"firstPage"` | | first page | the page borders defined for the section should be displayed on the first page of the current section. | | |
| `"notFirstPage"` | | not first pages | the page borders defined for the section should be displayed on every page (except first page) within that section. | | |

#### `<w:pgBorders>` -> `w:offsetFrom` attribute
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

#### `<w:pgBorders>` -> `w:zOrder` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"front"` | | |  the page border should be rendered **above** any intersecting text and other objects on the page. | default value | |
| `"back"` | | |  the page border should be rendered **below** any intersecting text and other objects on the page. | | |

#### `<w:latentStyles>` -> `w:defLockedState` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"false"` or `"0"` | | | | indicates new latent styles are not locked by default and can be modified. | | |
| `"true"` or `"1"` | | | | indicates new latent styles are locked by default and harder to be modified. | | |

#### `<w:latentStyles>` -> `w:defUnhideWhenUsed` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"false"` or `"0"` | | | | indicates that if a latent style is actually used in the document content, it will NOT become visible in the user interface. | | |
| `"true"` or `"1"` | | | | indicates that if a latent style is actually used in the document content, it will become visible in the user interface. | This allows styles that are relevant to the content to appear when needed. | |

#### `<w:latentStyles>` -> `w:defQFormat` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"false"` or `"0"` | | | | indicates that new latent styles will NOT appear in the Quick Styles gallery by default. | | |
| `"true"` or `"1"` | | | | indicates that new latent styles will appear in the Quick Styles gallery by default. |  | |

#### `<w:lsdException>` -> `w:name` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"false"` or `"0"` | | | | indicates that new latent styles will NOT appear in the Quick Styles gallery by default. | | |
| `"true"` or `"1"` | | | | indicates that new latent styles will appear in the Quick Styles gallery by default. |  | |

#### `<w:lsdException>` -> `w:semiHidden` attribute
> [!WARNING]
> I refers from Google Gemini's answer which may be incorrect.

| available options of attribute in tag | similar to options of attribute of tag in native xml or native html5)  | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- | :-- |
| `"false"` or `"0"` | | | | indicates that the style is not semi-hidden and will be visible in the Styles pane. | | |
| `"true"` or `"1"` | | | | indicates that the style is semi-hidden. it will be invisible unless it's actively in use in the document. | | |

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
