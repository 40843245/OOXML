# Appendix 1.2 -- tags in default namespace
## default namespace
### elements in default namespace
Required elements in `~/DocProps/app.xml` under a `.docx` file.

| namespace under default namespace | meaning | description | notes | notice |
| :---------- | :----------- | :----- | :--- | :-- |
| `<Properties>` | | acts like a container containing all properties in Metadata. | | |
| `<Application>` | | the application used when the document is created. | | |
| `<DocSecurity>` | | determines whether the document has security policies. | | |
| `<ScaleCrop>` | | determines whether the drawing object in the document can be scaled or cropped. | | |
| `<Company/>` | | compnay or organization when the document is created. | | |
| `<LinksUpToDate>` | | determines whether the link in the document is up to date. | | |
| `<SharedDoc>` | | determines whether the document can be shared. | | |
| `<HyperlinksChanged>` | | determines whether hyperlink in the document has been changed. | | |
| `<AppVersion>` | | the application version id when the document is created. | | |
| `<Template>` | | specifies whether the template is used when the document is created. | | |
| `<TotalTime>` | | time spent on editing the document in total | | |
| `<Pages>` | | number of pages in the document. | | |
| `<Words>` | | number of words in the document. | | |
| `<Characters>` | | number of characters (exclusive space) in the document. | | |
| `<CharactersWithSpaces>` | | number of characters (inclusive space) in the document. | | |
| `<Paragraphs>` | | number of paragraphs in the document. | | |
| `<Lines>` | | number of lines in the document. | | |

### examples
#### example 1.1
see [`~/docProps/app.xml` file under `OnlyWithOneFigureExample` and its explanation](https://github.com/40843245/OOXML/blob/main/examples/documents/Word/figure/OnlyWithOneFigureExample1.docx/app.xml/app.xml.md)
