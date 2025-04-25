# CH3 -- syntax
## content of tag in OOXML
### `field instruction`
#### syntax of `field instruction` in `<w:instrText>` tag

With [RE (regular expression)](https://learn.microsoft.com/en-us/dotnet/standard/base-types/regular-expression-language-quick-reference),

```
<w:instrText xmlns:space={spacing}>{fieldInstruction}</w:instrText>
```

where

```
{fieldInstruction}:= {whitespaces}{fieldIdentifier}{whitespaces}{switches}?{whitespaces}{arguments}?{whitespaces}
```

```
{whitespaces}:= {whitespace}+

{whitespace}:= ({space}|{tab})

{space}:= ` `

{tab}:= \t
```


```
{spacing}:= ("default"|"preserve")
```

Meaning: The value of `xmlns:space` MUST be either `"default"` or `"preserve"` 

```
{switches}:= (\\@{uppercaseLetters}|\\\*{uppercaseLetters})

{uppercaseLetters}:={uppercaseLetter}+

{uppercaseLetter}:= [A-Z]
```

Meaning: The switch MUST start with `\@` or `\*`, followed by a word that consist of uppercase alphabet.

#### syntax of `field instruction` in `<w:fldChar>` tag

With [RE (regular expression)](https://learn.microsoft.com/en-us/dotnet/standard/base-types/regular-expression-language-quick-reference),

```
<w:fldChar w:fldCharType={fieldCharacterType}>{fieldInstruction}</w:fldChar>
```

where

```
{fieldCharacterType}:= ("begin"|"seperate"|"end")
```

Meaning: it MUST be one of `begin`,`seperate`, and `end`.

About `{fieldInstruction}`, it is described in [syntax of `field instruction` in `<w:instrText>` tag section](https://github.com/40843245/OOXML/blob/main/Word/structure/CH1%20--%20syntax.md#syntax-of-field-instruction-in-winstrtext-tag)
