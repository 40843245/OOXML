# examples
## example 1
```
<Properties
xmlns="http://schemas.openxmlformats.org/officeDocument/2006/extended-properties"
xmlns:vt="http://schemas.openxmlformats.org/officeDocument/2006/docPropsVTypes">
  <Application>Microsoft Excel</Application>
  <DocSecurity>0</DocSecurity>
  <ScaleCrop>false</ScaleCrop>
  <HeadingPairs>
    <vt:vector size="2" baseType="variant">
      <vt:variant>
        <vt:lpstr>工作表</vt:lpstr>
      </vt:variant>
      <vt:variant>
        <vt:i4>3</vt:i4>
      </vt:variant>
    </vt:vector>
  </HeadingPairs>
  <TitlesOfParts>
    <vt:vector size="3" baseType="lpstr">
      <vt:lpstr>工作表1</vt:lpstr>
      <vt:lpstr>動漫或動畫等角色介紹</vt:lpstr>
      <vt:lpstr>動漫或動畫等介紹</vt:lpstr>
    </vt:vector>
  </TitlesOfParts>
  <Company/>
  <LinksUpToDate>false</LinksUpToDate>
  <SharedDoc>false</SharedDoc>
  <HyperlinksChanged>false</HyperlinksChanged>
  <AppVersion>16.0300</AppVersion>
</Properties>
```

In above example, we can know that 

+ In

```
<Properties
xmlns="http://schemas.openxmlformats.org/officeDocument/2006/extended-properties"
xmlns:vt="http://schemas.openxmlformats.org/officeDocument/2006/docPropsVTypes">
```

The xmlns namespace targets to `http://schemas.openxmlformats.org/officeDocument/2006/extended-properties`, meaning that it uses extension properties in Office Excel 2006.

The xmlns declares the vt namespace and targets to `http://schemas.openxmlformats.org/officeDocument/2006/docPropsVTypes`, meaning that the its variant type uses the Document Properties Variant Types schema in Office Excel 2006.

+ In `<Application>Microsoft Excel</Application>`, it is created by Microsoft Office Excel.
+ In `<DocSecurity>0</DocSecurity>`, there are no security for this spreadsheet.
+ In `<ScaleCrop>false</ScaleCrop>`, it indicates that the drawing objects should maintain its original aspect ratio and might not completely fill the shape.
+ In

```
  <HeadingPairs>
    <vt:vector size="2" baseType="variant">
      <vt:variant>
        <vt:lpstr>工作表</vt:lpstr>
      </vt:variant>
      <vt:variant>
        <vt:i4>3</vt:i4>
      </vt:variant>
    </vt:vector>
  </HeadingPairs>
```

  - In `<HeadingPairs>`, it stores all information about headings using a structure way.
  - In `<vt:vector size="2" baseType="variant">`, it indicates that the vector belongs to the Document Properties Variant Types schema,
  
    has two elements inside this tag and its element is `<vt:variant>`. 
    
  - In

    ```
      <vt:variant>
        <vt:lpstr>工作表</vt:lpstr>
      </vt:variant>
    ```

    It defines a variant whose long pointer points to a string -- `工作表` (which translates from Chinese to `Worksheet`).

  - In

    ```
      <vt:variant>
        <vt:i4>3</vt:i4>
      </vt:variant>
    ```

    The `<vt:i4>` indicates that the data type is a 4-byte integer.

    And there are 3 associated parts (maybe the number of worksheets in the Excel workbook, if this snippet came from an `.xlsx` file)

+ In

```
  <TitlesOfParts>
    <vt:vector size="3" baseType="lpstr">
      <vt:lpstr>工作表1</vt:lpstr>
      <vt:lpstr>動漫或動畫等角色介紹</vt:lpstr>
      <vt:lpstr>動漫或動畫等介紹</vt:lpstr>
    </vt:vector>
  </TitlesOfParts>
```

  - In `<TitlesOfParts>`, it stores all information about titles using a structure way.
  - In `<vt:vector size="3" baseType="lpstr">`, it indicates that the vector belongs to the Document Properties Variant Types schema,
  
    has three elements inside this tag and its element is `<vt:lpstr>`.

  - In `<vt:lpstr>工作表1</vt:lpstr>`, its long pointer points to a string -- `工作表1`
  
    (likely indicates the title of first worksheet is `工作表1`)

  - In `<vt:lpstr>動漫或動畫等角色介紹</vt:lpstr>`, its long pointer points to a string -- `動漫或動畫等角色介紹`
  
    (likely indicates the title of second worksheet is `動漫或動畫等角色介紹`)

  - In `<vt:lpstr>動漫或動畫等介紹</vt:lpstr>`, its long pointer points to a string -- `動漫或動畫等介紹`
  
    (likely indicates the title of third worksheet is `動漫或動畫等介紹`)
