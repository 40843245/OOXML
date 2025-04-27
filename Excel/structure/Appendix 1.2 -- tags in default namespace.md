# Appendix 1.2 -- tags in default namespace
## default namespace
### elements under default namespace
Required elements in `~/DocProps/app.xml` under a `.xlsx` file.

| elements under default namespace | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<Properties>` | | acts like a container containing all properties in Metadata. | | |
| `<Application>` | | the application used when the document is created. | | |
| `<DocSecurity>` | | determines whether the document has security policies. | | |
| `<ScaleCrop>` | | determines whether the drawing object in the document can be scaled or cropped. | | |
| `<Company/>` | | compnay or organization when the document is created. | | |
| `<LinksUpToDate>` | | determines whether the link in the document is up to date. | | |
| `<SharedDoc>` | | determines whether the document can be shared. | | |
| `<HyperlinksChanged>` | | determines whether hyperlink in the document has been changed. | | |
| `<HeadingPairs>` | | defines pairs of headings and the count of parts under those headings. | | |
| `<TitlesOfParts>` | | ists the titles of the individual parts of the document, in this case, worksheets. | | |

### elements under `<HeadingPairs>` element
#### children in `<HeadingPairs>` element
| children in `<HeadingPairs>` element | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:vector>` | | defines a vector for the heading of the Worksheet and acts like a container containing all properties about the vector. | | |

#### elements under `<vt:vector>` element
##### children in `<vt:vector>` element
| children in `<vt:vector>` element | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:variant>` | | acts like a container containing a single value within the vector. | | |

##### elements under `<vt:variant>` element
###### children in `<vt:variant>` element
| children in `<vt:variant>` element | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:lpwstr>` | | usually contains the string value representing the heading text. | | |
| `<vt:i4>` | | typically holds the integer value representing the count associated with the heading. | | |

### elements under `<TitlesOfParts>` element
#### children in `<TitlesOfParts>` element
| children in `<TitlesOfParts>` element | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:vector>` | | defines a vector for the title of the Worksheet and acts like a container containing all properties about the vector. | | |

#### elements under `<vt:vector>` element
##### children in `<vt:vector>` element
| children in `<vt:vector>` element | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:variant>` | | acts like a container containing a single value within the vector. | | |

##### elements under `<vt:variant>` element
###### children in `<vt:variant>` element
| children in `<vt:variant>` element | meaning | description | notes | notice |
| :-- | :-- | :-- | :-- | :-- |
| `<vt:lpwstr>` | | usually contains the string value representing the title text. | | |
