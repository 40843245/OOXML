# Prequisite Review 1 -- terms
## terms explanation
### about hyperlink
#### followed hyperlink
followed hyperlink is a link that has been clicked.

When a links has been clicked, it will be a followed hyperlink.

#### followed hyperlink style
followed hyperlink style is a style for followed hyperlink.

When a links has been clicked, it will be a followed hyperlink and apply followed hyperlink style.

### about font
#### pitch 
According to this article -- [`Adjusting Text Pitch`](https://wordribbon.tips.net/T013688_Adjusting_Text_Pitch.html), it is defined as 

```
In traditional typing, pitch is defined as a unit of measurement indicating the number of characters to a horizontal inch.
```

<img width="952" alt="image" src="https://github.com/user-attachments/assets/c7080e93-0684-42eb-8c76-36ee6b93e05f" />

##### reference
+ [`Adjusting Text Pitch`](https://wordribbon.tips.net/T013688_Adjusting_Text_Pitch.html)

#### panose 
PANOSE System is a method for classifying typefaces solely on their visual characteristics.

##### reference
+ [PANOSE (Wiki)](https://en.wikipedia.org/wiki/PANOSE)

### about unit measurements
See `Appendix 3`[^1] for more explanation.

### about list
#### single-level list
A signle-level list has these feature.

+ All items in same level (i.e. with same indentation).
+ If it is a numbered list, all items are marked with sequential number.

For example,

A single-level numbered list, 

It will look like this

1. First item
2. Second item
3. Third item

#### multi-level list
It is the opposite of single-level list.

For example,

A multi-level numbered list, 

It will look like this

1. First item

   1.1. First subitem in first item

   1.2. Second subitem in first item

### about indentation
#### hanging indentation
A hanging indent is used to indent all lines of a paragraph except the first.

![image](https://github.com/user-attachments/assets/5b7a9900-717c-4b1a-a0a2-24189b64d4ee)

### reference
+ [hanging indentation](https://www.scribbr.com/citing-sources/hanging-indent/)

### about role
#### document role
document role in OOXML determines what document should behaves when the property of an element in a Word file is not explicitly specified.

#### scheme mapping table
scheme mapping table stores the default behaviour of default scheme for document role. default scheme is only used iff the property of an element in a Word file is not explicitly specified.

> [!TIP]
> You can configure the scheme mapping table so that you don't have to set its attribute of tag many times.
>
> It is more maintenable and more readable.
  
[^1]: [Appendix 3 -- unit measurements](https://github.com/40843245/XmlOfOffice/blob/main/Word/structure/Appendix%203%20--%20unit%20measurements.md)
