# Appendix 1.3 -- Dublin Core Properties namespace
The `Dublin Core Properties` is usually declared in `cp` namespace
## `cp` namespace
### element in `cp` namespace
| element | meaning | description | note | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<cp:coreProperties>` | | acts like a container containing all core properties. | | |
| | | | | |
| `<cp:title>` | | title of Dublin Core Metadata | | |
| `<cp:subject>` | | subject of Dublin Core Metadata | | |
| `<cp:creator>` | | | creator of Dublin Core Metadata | | |
| `<cp:lastModifiedBy>` | | | person who last modifies Dublin Core Metadata | | |
| `<cp:created>` | | | date and time that Dublin Core Metadata is created | | |
| `<cp:modified>` | | | date and time that Dublin Core Metadata is last modified | | |
| `<cp:keywords>` | | | a set of keywords or phrases associated with the document | | |
| `<cp:description>` | | | description of Dublin Core Metadata | | |
| `<cp:revision>` | | | revision number of Dublin Core Metadata. It can store the number of time that Dublin Core Metadata is changed or updated | | |
| `<cp:version>` | | | version number of Dublin Core Metadata. | | |
| `<cp:contentStatus>` | | | status of content of Dublin Core Metadata. | | |
| `<cp:contentType>` | | | content type of Dublin Core Metadata. | | |

> [!IMPORTANT]
> You'll often see the `cp` namespace declared alongside other namespaces like `dc` (Dublin Core), `dcterms` (Dublin Core Terms), `dcmitype` (Dublin Core Metadata Initiative Type Vocabulary), and `xsi` (XML Schema Instance)
>
> because the core properties often utilize elements and attributes from these related vocabularies.


