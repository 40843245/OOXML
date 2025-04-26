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

it defines a core properties within OPC.

The core properties within OPC is targeted to the URI `http://schemas.openxmlformats.org/package/2006/metadata/core-properties`, 

meaning that it uses Open Xml format in version 2006 (according to `xmlns:cp="http://schemas.openxmlformats.org/package/2006/metadata/core-properties"`).

The set of Dublin Core Metadata Element is in version id 1.1 (according to `xmlns:dc="http://purl.org/dc/elements/1.1/"`).

The Dublin Core Metadata Terms is targeted to the URI `http://purl.org/dc/terms/` (according to `xmlns:dcterms="http://purl.org/dc/terms/"`).

The DCMI (Dublin Core Metadata Initiative) Type is targeted to the URI `http://purl.org/dc/dcmitype/` (according to `xmlns:dcmitype="http://purl.org/dc/dcmitype/"`).

The XML Schema instance is targeted to the URI `http://www.w3.org/2001/XMLSchema-instance` (according to `xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"`)

+ In `<dc:title/>`, it specifies the title of Dublin Core to empty.

Within the Dublin Core standard, title is defined as

```
a name given to the resource.
```

+ In `<dc:subject/>`, it specifies the subject Dublin Core to empty.

Within the Dublin Core standard, subject is defined as

```
topic of the content of the resource
```

+ In `<dc:creator>Jay Huang (黃奕捷)</dc:creator>`, it indicates that "Jay Huang" (with his Chinese name "黃奕捷" in parentheses) is the creator of the resource being described by this metadata.
+ In `<cp:keywords/>`, no keywords have been entered.
+ In `<dc:description/>`, there is no description in Dublin Core Metadata.

Within the Dublin Core standard, description is defined as

```
 an account of the content of the resource.
```

+ In `<cp:lastModifiedBy>Jay Huang (黃奕捷)</cp:lastModifiedBy>`, it indicates that the resource (likely a document or some other packaged content) was last modified by an individual named Jay Huang (黃奕捷).
+ In `<cp:revision>1</cp:revision>`, it store the revision id to 1, meaning that it is changed or updated 1 time.
+ In `<dcterms:created xsi:type="dcterms:W3CDTF">2025-04-07T08:50:00Z</dcterms:created>`
is commonly associated with the Dublin Core Metadata Initiative's terms vocabulary. This vocabulary extends the basic Dublin Core with more specific element refinements and encoding schemes. The local name created clearly indicates that this element specifies the date and time when the resource was created. Here, it is created at time zone `2025-04-07T08:50:00Z`.

+ In `<dcterms:modified xsi:type="dcterms:W3CDTF">2025-04-07T08:51:00Z</dcterms:modified>`, it indicates that last modified is at `2025-04-07T08:51:00Z`.
