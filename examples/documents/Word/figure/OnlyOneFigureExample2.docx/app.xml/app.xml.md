# examples
## example 1
```
<Properties
xmlns="http://schemas.openxmlformats.org/officeDocument/2006/extended-properties"
xmlns:vt="http://schemas.openxmlformats.org/officeDocument/2006/docPropsVTypes">
  <Template>Normal.dotm</Template>
  <TotalTime>1</TotalTime>
  <Pages>1</Pages>
  <Words>0</Words>
  <Characters>1</Characters>
  <Application>Microsoft Office Word</Application>
  <DocSecurity>0</DocSecurity>
  <Lines>1</Lines>
  <Paragraphs>1</Paragraphs>
  <ScaleCrop>false</ScaleCrop>
  <Company/>
  <LinksUpToDate>false</LinksUpToDate>
  <CharactersWithSpaces>1</CharactersWithSpaces>
  <SharedDoc>false</SharedDoc>
  <HyperlinksChanged>false</HyperlinksChanged>
  <AppVersion>16.0000</AppVersion>
</Properties>
```

In above example, we can know that

+ In

```
<Properties
xmlns="http://schemas.openxmlformats.org/officeDocument/2006/extended-properties"
xmlns:vt="http://schemas.openxmlformats.org/officeDocument/2006/docPropsVTypes">
```

it defines the properties of Open Xml format.

It is targeted by Office Document 2006 extension pack.

It indicates the variant type of document properties is in Office Document 2006.

+ In `<Template>Normal.dotm</Template>`, it indicates that the document is created by `Normal.dotm` template. 
+ In `<TotalTime>1</TotalTime>`, editing the document spent on one unit in total. One unit usually refers to one minute.
+ In `<Pages>1</Pages>`, there is one page in total.
+ In `<Words>0</Words>`, there is zero words in total.
+ In `<Characters>1</Characters>`, there is one character (exclusive space) in total.
+ In `<Application>Microsoft Office Word</Application>`, the document is created by Microsoft Office Word.
+ In `<DocSecurity>0</DocSecurity>`, it indicates that there are no document security.
+ In `<Lines>1</Lines>`, there is one line in total.
+ In `<Paragraphs>1</Paragraphs>`, there is one paragraph in total.
+ In `<ScaleCrop>false</ScaleCrop>`, it indicates that scaling or cropping a drawing object is disabled.
+ In `<Company/>`, it indicates that there are no company in this document.
+ In `<LinksUpToDate>false</LinksUpToDate>`, it indicates the link is NOT up to date.
+ In `<CharactersWithSpaces>1</CharactersWithSpaces>`, there is one character (with space) in this document.
+ In `<SharedDoc>false</SharedDoc>`, the document can NOT be shared.
+ In `<HyperlinksChanged>false</HyperlinksChanged>`, the hyperlink has NOT been changed.
+ In `<AppVersion>16.0000</AppVersion>`, this document is created in version id `16.0000`.
