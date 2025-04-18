# example 4 -- a full chart
`~/word/charts/chart1.xml` file under `BarChartExample.docx` file.

```
<c:chartSpace xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart" xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main" xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships">
        <c:roundedCorners val="0"/>
        <c:chart>
            <c:autoTitleDeleted val="0"/>
            <c:plotArea>
                <c:layout/>
                <c:barChart xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart">
                    <c:barDir val="col"/>
                    <c:grouping val="clustered"/>
                    <c:gapWidth val="150"/>
                    <c:axId xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart" val="148921728"/>
                    <c:axId xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart" val="154227840"/>
                    <c:overlap val="0"/>
                    <c:dLbls xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart">
                        <c:showLegendKey val="0"/>
                        <c:showVal val="0"/>
                        <c:showCatName val="0"/>
                        <c:showSerName val="0"/>
                        <c:showPercent val="0"/>
                        <c:showBubbleSize val="0"/>
                        <c:showLeaderLines val="1"/>
                    </c:dLbls>
                    <c:ser>
                        <c:idx val="1"/>
                        <c:order val="1"/>
                        <c:tx>
                            <c:strRef>
                                <c:f/>
                                <c:strCache>
                                    <c:pt idx="0">
                                        <c:v>Brazil</c:v>
                                    </c:pt>
                                </c:strCache>
                            </c:strRef>
                        </c:tx>
                        <c:invertIfNegative>0</c:invertIfNegative>
                        <c:cat>
                            <c:strRef>
                                <c:f/>
                                <c:strCache>
                                    <c:ptCount val="4"/>
                                    <c:pt idx="0">
                                        <c:v>Food</c:v>
                                    </c:pt>
                                    <c:pt idx="1">
                                        <c:v>Housing</c:v>
                                    </c:pt>
                                    <c:pt idx="2">
                                        <c:v>Transportation</c:v>
                                    </c:pt>
                                    <c:pt idx="3">
                                        <c:v>Health Care</c:v>
                                    </c:pt>
                                </c:strCache>
                            </c:strRef>
                        </c:cat>
                        <c:val>
                            <c:numRef>
                                <c:f/>
                                <c:numCache>
                                    <c:formatCode>General</c:formatCode>
                                    <c:ptCount val="4"/>
                                    <c:pt idx="0">
                                        <c:v>125</c:v>
                                    </c:pt>
                                    <c:pt idx="1">
                                        <c:v>80</c:v>
                                    </c:pt>
                                    <c:pt idx="2">
                                        <c:v>110</c:v>
                                    </c:pt>
                                    <c:pt idx="3">
                                        <c:v>60</c:v>
                                    </c:pt>
                                </c:numCache>
                            </c:numRef>
                        </c:val>
                    </c:ser>
                </c:barChart>
                <c:catAx xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart">
                    <c:axId val="148921728"/>
                    <c:scaling>
                        <c:orientation val="minMax"/>
                    </c:scaling>
                    <c:delete val="0"/>
                    <c:axPos val="b"/>
                    <c:majorTickMark val="out"/>
                    <c:minorTickMark val="none"/>
                    <c:tickLblPos val="nextTo"/>
                    <c:crossAx val="154227840"/>
                    <c:crosses val="autoZero"/>
                    <c:auto val="1"/>
                    <c:lblAlgn val="ctr"/>
                    <c:lblOffset val="100"/>
                    <c:noMultiLvlLbl val="0"/>
                </c:catAx>
                <c:valAx xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart">
                    <c:axId val="154227840"/>
                    <c:scaling>
                        <c:orientation val="minMax"/>
                    </c:scaling>
                    <c:delete val="0"/>
                    <c:axPos val="l"/>
                    <c:numFmt sourceLinked="0" formatCode="General"/>
                    <c:majorGridlines/>
                    <c:majorTickMark val="out"/>
                    <c:minorTickMark val="none"/>
                    <c:tickLblPos val="nextTo"/>
                    <c:crossAx val="148921728"/>
                    <c:crosses val="autoZero"/>
                    <c:crossBetween val="between"/>
                </c:valAx>
            </c:plotArea>
            <c:legend>
                <c:legendPos val="l"/>
                <c:overlay val="0"/>
            </c:legend>
            <c:plotVisOnly val="1"/>
            <c:dispBlanksAs val="gap"/>
            <c:showDLblsOverMax val="0"/>
        </c:chart>
</c:chartSpace>
```

The above example illustrates the xml content of bar chart in `BarChartExample.docx` file, 

and bar chart will looks like this.

<img width="476" alt="image" src="https://github.com/user-attachments/assets/57d06375-14aa-4c39-9538-9d5bb7eb041f" />

Let's partition the above example into several code snippets and breakdown them.

## Part 1.

```
<c:chartSpace xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart" xmlns:a="http://schemas.openxmlformats.org/drawingml/2006/main" xmlns:r="http://schemas.openxmlformats.org/officeDocument/2006/relationships">
        <c:roundedCorners val="0"/>
        <c:chart>
            <c:autoTitleDeleted val="0"/>
            <c:plotArea>
                <c:layout/>
                <c:barChart xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart">
                    <c:barDir val="col"/>
                    <c:grouping val="clustered"/>
                    <c:gapWidth val="150"/>
                    <c:axId xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart" val="148921728"/>
                    <c:axId xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart" val="154227840"/>
                    <c:overlap val="0"/>
                    <c:dLbls xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart">
                        <c:showLegendKey val="0"/>
                        <c:showVal val="0"/>
                        <c:showCatName val="0"/>
                        <c:showSerName val="0"/>
                        <c:showPercent val="0"/>
                        <c:showBubbleSize val="0"/>
                        <c:showLeaderLines val="1"/>
                    </c:dLbls>
```

+ In `<c:chartSpace>`, it defines a chart space, containing all charts (and, of course, its configuration).
+ In `<c:roundedCorners val="0"/>`, it specifies that all charts in this chart space are NOT round-shaped. They are rectangular.
+ In `<c:chart>`, it defines a chart.
+ In `<c:autoTitleDeleted val="0"/>`, it indicates that the user has NOT deleted the auto-generated title yet.
+ In `<c:plotArea>`, it defines a plot area in the chart.
+ In `<c:layout/>`, it defines a layout in the plot area.
+ In `<c:barChart xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart">`, it specifies that it is a bar chart.
+ In `<c:barDir val="col"/>`, it sets the direction of bar is column, which specifies it is a column (bar) chart.
+ In `<c:grouping val="clustered"/>`, the series is grouped by clusters.
+ In `<c:gapWidth val="150"/>`, it specifies the gap width between two series is 150 twips.
+ In `<c:axId xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart" val="148921728"/>`, it defines an axis identifier which is `148921728`.
+ In `<c:axId xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart" val="154227840"/>`, it defines an axis identifier which is `154227840`.
+ In `<c:overlap val="0"/>`, it indicates that the series in the chart should be displayed side-by-side without any overlap.
+ In `<c:dLbls xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart">`, it defines data labels.
+ In `<c:showLegendKey val="0"/>`, it indicates that not legend is not shown.
+ In `<c:showVal val="0"/>`, it indicates that actual data value will NOT be shown on series.
+ In `<c:showCatName val="0"/>`, it indicates that the categories will NOT be shown.
+ In `<c:showSerName val="0"/>`, it indicates that the name of series will NOT be shown.
+ In `<c:showPercent val="0"/>`, it indicates that the percentage of actual data value takes (i.e. ratio of the actual data value and the total of actual data values.) will NOT be shown.
+ In `<c:showBubbleSize val="0"/>`, it sets the bubble size is zero, which means that it will not shown the bubble.
+ In `<c:showLeaderLines val="1"/>`, it indicates that the leader lines for data labels will be shown.

## Part 2.

```
                <c:ser>
                        <c:idx val="1"/>
                        <c:order val="1"/>
                        <c:tx>
                            <c:strRef>
                                <c:f/>
                                <c:strCache>
                                    <c:pt idx="0">
                                        <c:v>Brazil</c:v>
                                    </c:pt>
                                </c:strCache>
                            </c:strRef>
                        </c:tx>
                        <c:invertIfNegative>0</c:invertIfNegative>
```

+ In `<c:ser>`, it defines a series.
+ In `<c:idx val="1"/>`, it specifies the index of the series is 1, which means it's the second item to display (since the index (`<c:idx/>`) is zero-based in OOXML). (from Google Gemin's answer)
+ In `<c:order val="1"/>`, it indicates it's the first item to be handled with (since the order (`<c:order/>`) is first-based in OOXML). (from Google Gemin's answer)
+ In `<c:tx>`, it defines a text (including its style and formatting) in the series.
+ In `<c:strRef>`, it specifies the text in the series is referenced to a cell or a range within spreadsheet that contains
the data.
+ In `<c:f/>`, it contains the formula of a cell or a range within spreadsheet that is referenced by the `val` attribute of `<c:strRef>`.
+ In 

```
<c:strCache>
        <c:pt idx="0">
                <c:v>Brazil</c:v>
        </c:pt>
</c:strCache>
```

`<c:strCache>` specifies the cached copy of text value of the series. 

and it holds the cached text value from the first cell of the formula (which is specified by the `val` of `<c:f/>`), which is `Brazil`, meaning that the title of the series is `Brazil`.

+ In `<c:invertIfNegative>0</c:invertIfNegative>`, it indicates that the fill color of the data markers in the series should not be inverted when the actual data value is negative.

## Part 3.

```
                <c:ser>
                        <!-- tags appeared in Part 2. omitted -->
                        <!-- ... -->

                        <c:cat>
                            <c:strRef>
                                <c:f/>
                                <c:strCache>
                                    <c:ptCount val="4"/>
                                    <c:pt idx="0">
                                        <c:v>Food</c:v>
                                    </c:pt>
                                    <c:pt idx="1">
                                        <c:v>Housing</c:v>
                                    </c:pt>
                                    <c:pt idx="2">
                                        <c:v>Transportation</c:v>
                                    </c:pt>
                                    <c:pt idx="3">
                                        <c:v>Health Care</c:v>
                                    </c:pt>
                                </c:strCache>
                            </c:strRef>
                        </c:cat>
```

+ In `<c:cat>`, it defines the categories of the series.
+ In `<c:strRef>`, it specifies the text in the series is referenced to a cell or a range within spreadsheet that contains
the data.
+ In `<c:f/>`, it contains the formula of a cell or a range within spreadsheet that is referenced by the `val` attribute of `<c:strRef>`.
+ In

```
                                <c:strCache>
                                    <c:ptCount val="4"/>
                                    <c:pt idx="0">
                                        <c:v>Food</c:v>
                                    </c:pt>
                                    <c:pt idx="1">
                                        <c:v>Housing</c:v>
                                    </c:pt>
                                    <c:pt idx="2">
                                        <c:v>Transportation</c:v>
                                    </c:pt>
                                    <c:pt idx="3">
                                        <c:v>Health Care</c:v>
                                    </c:pt>
                                </c:strCache>
```

it specifies the cached copy of text values. 

There are four categories here (according to `<c:ptCount val="4"/>`) -- 

`Food`, `Housing`, `Transportation`, and `Health Care` respectively.

## Part 4.

```
                <c:ser>
                        <!-- tags appeared in Part 2. and Part 3. omitted -->
                        <!-- ... -->

                        <c:val>
                            <c:numRef>
                                <c:f/>
                                <c:numCache>
                                    <c:formatCode>General</c:formatCode>
                                    <c:ptCount val="4"/>
                                    <c:pt idx="0">
                                        <c:v>125</c:v>
                                    </c:pt>
                                    <c:pt idx="1">
                                        <c:v>80</c:v>
                                    </c:pt>
                                    <c:pt idx="2">
                                        <c:v>110</c:v>
                                    </c:pt>
                                    <c:pt idx="3">
                                        <c:v>60</c:v>
                                    </c:pt>
                                </c:numCache>
                            </c:numRef>
                        </c:val>
                    </c:ser>
```

+ In `<c:val>`, it specifies the actual data values.
+ In `<c:numRef>`, it specifies the numerical value in the series is referenced to a cell or a range within spreadsheet that contains the data.
+ In `<c:f/>`, it contains the formula of a cell or a range within spreadsheet that is referenced by the `val` attribute of `<c:numRef>`.
+ In `<c:formatCode>General</c:formatCode>`, it specifies the number formatting is `General`, which means the numerical values will be displayed as closely as possible to how it is entered.
+ In

```
                                <c:numCache>
                                    <c:formatCode>General</c:formatCode>
                                    <c:ptCount val="4"/>
                                    <c:pt idx="0">
                                        <c:v>125</c:v>
                                    </c:pt>
                                    <c:pt idx="1">
                                        <c:v>80</c:v>
                                    </c:pt>
                                    <c:pt idx="2">
                                        <c:v>110</c:v>
                                    </c:pt>
                                    <c:pt idx="3">
                                        <c:v>60</c:v>
                                    </c:pt>
                                </c:numCache>
                            </c:numRef>
```

it specifies a cached copy of numerical values.

There are four numeric value (represents actual data value) -- `125`, `80`, `110`, `60`.

Look at Part 3 and Part 4., we can know that the data of the chart is as follows.

| index to display (from left to right) | category name | actual value |
| :-- | :-- | :-- |
| `1` | `Food` | `125` |
| `2` | `Housing` | `80` |
| `3` | `Transportation` | `110` |
| `4` | `Health Care` | `60` |


## Part 5.

```
                <c:catAx xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart">
                    <c:axId val="148921728"/>
                    <c:scaling>
                        <c:orientation val="minMax"/>
                    </c:scaling>
                    <c:delete val="0"/>
                    <c:axPos val="b"/>
                    <c:majorTickMark val="out"/>
                    <c:minorTickMark val="none"/>
                    <c:tickLblPos val="nextTo"/>
                    <c:crossAx val="154227840"/>
                    <c:crosses val="autoZero"/>
                    <c:auto val="1"/>
                    <c:lblAlgn val="ctr"/>
                    <c:lblOffset val="100"/>
                    <c:noMultiLvlLbl val="0"/>
                </c:catAx>
```

+ In `<c:catAx xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart">`, it defines the axis for categories.
+ In `<c:axId val="148921728"/>`, it sets the axis id for category to `148921728`.
+ In

```
                    <c:scaling>
                        <c:orientation val="minMax"/>
                    </c:scaling>
```

it specifies configurations about scaling, and the axis should be oriented from the minimun value to the maximum value.

+ In `<c:delete val="0"/>`, it indicates that the axis for categories is NOT be marked for deletion and should be displayed in the chart.
+ In `<c:axPos val="b"/>`, it indicates that axis about categories is positioned at the bottom of the plotting area.
+ In `<c:majorTickMark val="out"/>, the major tick on y-axis line is outside on the chart. And thus, here it is located on the left of the y-axis line.
+ In `<c:minorTickMark val="none"/>`, it indicates the minor tick is NOT shown in this chart.
+ In `<c:tickLblPos val="nextTo"/>`, it indicates that the tick mark labels are positioned adjacent to the axis line.
+ In `<c:crossAx val="154227840"/>`, it sets ID of the axis that this axis crosses to `154227840`.
+ In `<c:crosses val="autoZero"/>`, it specifies the crossing point of an axis.
+ In `<c:auto val="1"/>`, it indicates that its settings for that property is automatic,
+ In `<c:lblAlgn val="ctr"/>`, it indicates that the text within the data labels on the chart should be horizontally
centered. 
+ In `<c:lblOffset val="100"/>` , the offset of data lavel 100 twips.
+ In  `<c:noMultiLvlLbl val="0"/>` ,it indicates that the chart axis should allow the display of multi-level labels if the underlying category data supports it.

## Part 6.

```
                <c:valAx xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart">
                    <c:axId val="154227840"/>
                    <c:scaling>
                        <c:orientation val="minMax"/>
                    </c:scaling>
                    <c:delete val="0"/>
                    <c:axPos val="l"/>
                    <c:numFmt sourceLinked="0" formatCode="General"/>
                    <c:majorGridlines/>
                    <c:majorTickMark val="out"/>
                    <c:minorTickMark val="none"/>
                    <c:tickLblPos val="nextTo"/>
                    <c:crossAx val="148921728"/>
                    <c:crosses val="autoZero"/>
                    <c:crossBetween val="between"/>
                </c:valAx>
```

+ In `<c:valAx xmlns:c="http://schemas.openxmlformats.org/drawingml/2006/chart">`, it defines a axis for actual data value.
+ In ` <c:axId val="154227840"/>`, it sets the value axis to `154227840`.
+ In

  ```
                      <c:scaling>
                        <c:orientation val="minMax"/>
                      </c:scaling>
  ```

it specifies configurations about scaling, and the y-axis should be oriented from the minimun value to the maximum value.

+ In `<c:delete val="0"/>`, it indicates that it has NOT be marked for deletion yet.
+ In `<c:axPos val="l"/>`, it indicates the y-axis is positioned at the left of the plot area so that the major tick is displayed at left of the plotting area.
+ In `<c:numFmt sourceLinked="0" formatCode="General"/>`, it specifies the number formatting for y-axis.

`sourceLinked="0"` (or false) indicates that the number format is explicitly defined by the formatCode attribute and is not inherited from the source data.

`formatCode="General"` indicates that the number format is `General` which means that it is NOT unformatted.

+ In `<c:majorGridlines/>`, it indicates that it will show major gridlines.'
+ In `<c:majorTickMark val="out"/>`, it indicates that the major tick marks are displayed outside the plotting area.
+ In `<c:minorTickMark val="none"/>`, it indicates that the minor tick marks will NOT be displayed.
+ In `<c:tickLblPos val="nextTo"/>`, it indicates that the tick mark labels are positioned adjacent to the axis line.
+ In `<c:crossAx val="148921728"/>`, it sets the ID of the axis that this axis crosses to `148921728`.
+ In `<c:crosses val="autoZero"/>`, it indicates that this particular chart axis is set to cross the other axis</br>(specified by the corresponding <c:crossAx> tag on the other axis) at the zero point of that other axis, if zero is within its range. </br>Otherwise, it will cross at the minimum or maximum value of the other axis that is closest to zero.
+ In `<c:crossBetween val="between"/>`, it indicates that the value axis of the chart will intersect the category axis at a position between the category labels.

## Part 7.

```
<c:legend>
        <c:legendPos val="l"/>
        <c:overlay val="0"/>
</c:legend>
```

+ In `<c:legend>`, it defines a legend for this chart.
+ In `<c:legendPos val="l"/>`, it indicates that the legend is positioned at left of the plotting area.
+ In `<c:overlay val="0"/>`, it indicates that the legend is NOT overlapped to the plotting area.

## Part 8.

```
<c:plotVisOnly val="1"/>
<c:dispBlanksAs val="gap"/>
<c:showDLblsOverMax val="0"/>
```

+ In `<c:plotVisOnly val="1"/>`, it ensures that only the visible data points in the chart's source data will be plotted. Any hidden data (due to filtering or manual hiding) will be excluded from the chart.
+ In `<c:dispBlanksAs val="gap"/>`, it indicates that it will leave a gap in the chart when either a blank cell or missing data point occurs.
+ In `<c:showDLblsOverMax val="0"/>`, it indicates that data labels whose values are higher than the axis's maximum will **NOT** be shown on the chart.
