# CH1 -- syntax
## content of tag in OOXML
### `field instruction`
#### syntax of `field instruction` in `<w:instrText>` tag

With [RE (regular expression)](https://learn.microsoft.com/en-us/dotnet/standard/base-types/regular-expression-language-quick-reference),

```
<w:instrText xmlns:space={spacing}>{fieldInstruction}</w:instrText>
```

where

```
{fieldInstruction}:= {fieldIdentifier} {switches}? {arguments}?
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
{fieldCharacterType}:= ("begin"|"seperator"|"end")
```

Meaning: it MUST be one of `begin`,`seperator`, and `end`.

About `{fieldInstruction}`, it is described in [syntax of `field instruction` in `<w:instrText>` tag section]()
