# sematic equivalence in OOXML
## value in `val` attribute v.s. element's content for a boolean value
### examples 
#### examples 1

1. 
```
<c:invertIfNegative val="0"/>
```

2. 
```
<c:invertIfNegative>0</c:invertIfNegative>
```

In above examples, they are sematically equivalent (i.e. they have same meaning).

In former one, the boolean value is represented as an attribute (in `val` attribute).

While, in latter one, the boolean value is represented as the element's text content.

The former one is more conventional and schema-consistent way to represent boolean attributes in the OOXML and more readable for humans. 

Thus, ideally, the latter one should be removed (and no longer see it).

However, the later one may appear in these scenarios.

+ In earlier version of OOXML: the first version of OOXML, the syntax with the former one is NOT allowed and the former one is straightword for reading, but is inducible to misunderstand.
+ Data serialization and deserialization from certain programming models: some programming models ***since serializing and deserializing an text content is more easier for some XML preprocessors (and thus, more efficient).***

> [!TIP]
> Why serializing and deserializing an text content is more easier for some XML preprocessors?
>
> There are two reasons:
>
> 
