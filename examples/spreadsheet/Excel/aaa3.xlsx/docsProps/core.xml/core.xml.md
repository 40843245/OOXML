# examples
## example 1
```
<cp:coreProperties
xmlns:cp="http://schemas.openxmlformats.org/package/2006/metadata/core-properties"
xmlns:dc="http://purl.org/dc/elements/1.1/" xmlns:dcterms="http://purl.org/dc/terms/"
xmlns:dcmitype="http://purl.org/dc/dcmitype/"
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
  <dc:creator>userJay30</dc:creator>
  <cp:lastModifiedBy>Jay Huang (黃奕捷)</cp:lastModifiedBy>
  <dcterms:created xsi:type="dcterms:W3CDTF">2015-06-05T18:19:34Z</dcterms:created>
  <dcterms:modified xsi:type="dcterms:W3CDTF">2025-04-29T06:30:44Z</dcterms:modified>
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

it configures the Dublin core properties.

The `xmlns:cp` namespace targets to `http://schemas.openxmlformats.org/package/2006/metadata/core-properties`, meaning that

the core properties adopts the core properties schema of Open Xml formats in version 2006.

The `xmlns:dc` targets to `http://purl.org/dc/elements/1.1/`, meaning that 

Dublin Core Metadata Element with version 1.1 is used.

The `xmlns:dcterms` targets to `http://purl.org/dc/terms/`, meaning that

the terms about Dublin Core refers to the URI `http://purl.org/dc/terms/`.

The `xmlns:dcmitype` targets to `http://purl.org/dc/dcmitype/`, meaning that

the Dublin Core Mime type refers to the URI `http://purl.org/dc/dcmitype/`.

The `xmlns:xsi` targets to `http://www.w3.org/2001/XMLSchema-instance`, meaning that

the Xml Schema instance refers to `http://www.w3.org/2001/XMLSchema-instance` (released at year 2001)

+ In `<dc:creator>userJay30</dc:creator>`, the metadata is created by user account name -- `userJay30`.
+ In `<cp:lastModifiedBy>Jay Huang (黃奕捷)</cp:lastModifiedBy>`, the metadata is last modified by `Jay Huang (黃奕捷)`.
+ In `<dcterms:created xsi:type="dcterms:W3CDTF">2015-06-05T18:19:34Z</dcterms:created>`,

the element conforms `W3C Date and Time Format` (ISO 8601). 

And the metadata is created at `June 5th, 2015, at 18:19:34 Coordinated Universal Time (UTC).

+ In `<dcterms:modified xsi:type="dcterms:W3CDTF">2025-04-29T06:30:44Z</dcterms:modified>`,

the element conforms `W3C Date and Time Format` (ISO 8601). 

And the metadata is last modified at April 29th, 2025, at 06:30:44 UTC.
