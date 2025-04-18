###### example 4 -- a full chart
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

Let's breakdown the above example.

+ In `<c:chartSpace>`, it defines a chart space, containing all charts (and, of course, its configuration).
+ In `<c:roundedCorners val="0"/>`, it specifies that all charts in this chart space are NOT round-shaped. They are rectangular.
+ In `<c:chart>`, it defines a chart.
+ In `<c:autoTitleDeleted val="0"/>`, it indicates that the user has NOT deleted the auto-generated title yet.
+ In
