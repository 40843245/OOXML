# CH4 -- namespaces and package parts in Office Word
## objectives
In this chapter, you will learn

+ namespaces in an Office Word file
+ package parts in an Office Word file

## CH4.1 -- namespaces in an Office Word file
| namespaces | description | required | notice |
| :-- | :-- | :-- | :-- |
| `WordprocessingML` | it's an indispensable namespace. package for processing an Office Word file. | required | |
| `DrawingML` | it's an indispensable namespace. package for processing drawing objects. | required | |
| `WordProcessing Canvas`| is used for drawing and layout within the Word document (particularly newer drawing features) | required | |
| `DrawingML Ink Schema` | is used for defining properties for inks, provide Digital Ink Support, and provide DrawingML Integration | optional | |
| `DrawingML 3D Model Schema` | is used for defining properties for 3D model, embed 3D models, and provide DrawingML Integration | optional | |
| `Data Types` | is often used for properties or values within the document. | required | |
| `Markup Compatibility` | is used for backward compatibility with different versions of Office Open XML. | usually required (Otherwise, it could be NOT compatible backward with different version) | |
| `Charts` | is used for charts. | optional | | 
| `Office` | is often related to general Office document properties (metadata of an Office Word file). | required | All tags that has the prefix `o` namespace stores the info about an Office file. |
| `Schema Library` | is possibly related to document templates or components. | optional | |
| `Relationship` | used for relationships between these package parts in an Office Word file | required | |
| `Math` | is used for math calculation | required | |

## CH4.2 -- package parts in an Office Word file
### about WordprocessingML
<img width="440" alt="image" src="https://github.com/user-attachments/assets/0bd0c0be-44a5-4803-8590-8f37f7fd98f0" />

<img width="443" alt="image" src="https://github.com/user-attachments/assets/01582c76-2155-43b0-b695-6779a122909c" />

refered to [Important WordprocessingML Parts](https://learn.microsoft.com/en-us/office/open-xml/word/structure-of-a-wordprocessingml-document?tabs=cs#important-wordprocessingml-parts)

provided by MSDS

#### reference
[Structure of a WordprocessingML document](https://learn.microsoft.com/en-us/office/open-xml/word/structure-of-a-wordprocessingml-document?tabs=cs#important-wordprocessingml-parts)
