# examples
## example 1
```
<cp:coreProperties
xmlns:cp="http://schemas.openxmlformats.org/package/2006/metadata/core-properties"
xmlns:dc="http://purl.org/dc/elements/1.1/"
xmlns:dcterms="http://purl.org/dc/terms/"
xmlns:dcmitype="http://purl.org/dc/dcmitype/"
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <dc:title/>
  <dc:subject/>
  <dc:creator>Vincent Wang (王晏宗)</dc:creator>
  <cp:keywords/>
  <dc:description/>
  <cp:lastModifiedBy>Jay Huang (黃奕捷)</cp:lastModifiedBy>
  <cp:revision>2</cp:revision>
  <dcterms:created xsi:type="dcterms:W3CDTF">2025-04-07T09:03:00Z</dcterms:created>
  <dcterms:modified xsi:type="dcterms:W3CDTF">2025-04-07T09:03:00Z</dcterms:modified>
</cp:coreProperties>
```

In above example, we can know that

+ In

```
<cp:coreProperties
xmlns:cp="http://schemas.openxmlformats.org/package/2006/metadata/core-properties"
xmlns:dc="http://purl.org/dc/elements/1.1/"
xmlns:dcterms="http://purl.org/dc/terms/"
xmlns:dcmitype="http://purl.org/dc/dcmitype/"
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
```

it defines the core properties within OPC.

The core properties within OPC targets the URI `http://schemas.openxmlformats.org/package/2006/metadata/core-properties`, 

meaning that it uses Open Xml formats in version 2006 (according to `xmlns:cp="http://schemas.openxmlformats.org/package/2006/metadata/core-properties"`).

The set of Dublin Core Metadata Elements is in version id 1.1 (according to `xmlns:dc="http://purl.org/dc/elements/1.1/"`).

The Dublin Core Metadata Terms is targeted to the URI `http://purl.org/dc/terms/` (according to `xmlns:dcterms="http://purl.org/dc/terms/"
`).

The Dublin Core Metadata Initiative Type is targeted to the URI `http://purl.org/dc/dcmitype/` (according to `xmlns:dcmitype="http://purl.org/dc/dcmitype/"
`).

The Xml schema instance is targeted to the URI `http://www.w3.org/2001/XMLSchema-instance` (according to `xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"`).

+ In `<dc:title/>`, it specifies the title of Dublin Core Metadata to empty.
+ In `<dc:subject/>`, it specifies the subject of Dublin Core Metadata to empty.
+ In `<dc:creator>Vincent Wang (王晏宗)</dc:creator>`, it indicates the creator of Dublin Core Metadata is `Vincent Wang (王晏宗)`.
+ In `<cp:keywords/>`, it indicates that there are no keywords.
+ In `<dc:description/>`, it indicates that the description of the content of the source is empty.
+ In `<cp:lastModifiedBy>Jay Huang (黃奕捷)</cp:lastModifiedBy>`, it indicates that `Jay Huang (黃奕捷)` modifies Dublin Core Metadata at recent.
+ In `<cp:revision>2</cp:revision>`, it indicates that it is changed or updated 2 times.
+ In `<dcterms:created xsi:type="dcterms:W3CDTF">2025-04-07T09:03:00Z</dcterms:created>`, it indicates that it is created at `2025-04-07T09:03:00Z`.
+ In `<dcterms:modified xsi:type="dcterms:W3CDTF">2025-04-07T09:03:00Z</dcterms:modified>`, it indicates that it is last modified at `2025-04-07T09:03:00Z`.
