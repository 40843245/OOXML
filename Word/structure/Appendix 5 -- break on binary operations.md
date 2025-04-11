# Appendix 5 -- break on binary operations
## intro
According to `ISO/IEC 29500-1 (1st Edition)`,

Specifying the behaviour on break on binary operations determines how binary operators are treated when they coincide with a line break. If this element is omitted, the line break occurs before the binary operator. That is, the binary operator is the first element on the wrapped line.

## related tag in OOXML
### brkBin
#### intro
The `<brkBin>` tag specifies the behaviour on break on binary operations.

Whether the element is absent or present without the `val` attribute, the default of the `val` attribute is before.

### brkBinSub
## reference
[BreakBinary class (MSDS)](https://learn.microsoft.com/en-us/dotnet/api/documentformat.openxml.math.breakbinary?view=openxml-3.0.1)
