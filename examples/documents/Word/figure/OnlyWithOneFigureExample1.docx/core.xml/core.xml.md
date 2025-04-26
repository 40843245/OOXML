# examples
## example 1
```
<cp:coreProperties xmlns:cp="http://schemas.openxmlformats.org/package/2006/metadata/core-properties" xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:dcterms="http://purl.org/dc/terms/" xmlns:dcmitype="http://purl.org/dc/dcmitype/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <dc:title/>
  <dc:subject/>
  <dc:creator>Jay Huang (黃奕捷)</dc:creator>
  <cp:keywords/>
  <dc:description/>
  <cp:lastModifiedBy>Jay Huang (黃奕捷)</cp:lastModifiedBy>
  <cp:revision>1</cp:revision>
  <dcterms:created xsi:type="dcterms:W3CDTF">2025-04-07T08:50:00Z</dcterms:created>
  <dcterms:modified xsi:type="dcterms:W3CDTF">2025-04-07T08:51:00Z</dcterms:modified>
</cp:coreProperties>
```

In above example, we can know that

+ In

```
<cp:coreProperties xmlns:cp="http://schemas.openxmlformats.org/package/2006/metadata/core-properties" xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:dcterms="http://purl.org/dc/terms/" xmlns:dcmitype="http://purl.org/dc/dcmitype/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
```

it defines a core properties.

The core properties targets to Office Word 2006 (according to `xmlns:cp="http://schemas.openxmlformats.org/package/2006/metadata/core-properties"`).

The Dublin Core Metadata Element Set is in version id 1.1 (according to `xmlns:dc="http://purl.org/dc/elements/1.1/"`).

The Dublin Core Metadata Terms is targeted to the URI `http://purl.org/dc/terms/` (according to `xmlns:dcterms="http://purl.org/dc/terms/"`).

The DCMI (Dublin Core Metadata Initiative) Type is targeted to the URI `http://purl.org/dc/dcmitype/` (according to `xmlns:dcmitype="http://purl.org/dc/dcmitype/"`).

is targeted to the URI `http://www.w3.org/2001/XMLSchema-instance` (according to `xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"`)
