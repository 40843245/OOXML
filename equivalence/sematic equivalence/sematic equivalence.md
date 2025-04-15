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
+ Data serialization and deserialization from certain programming models: some programming models serialize and deserialize using the latter approach ~~since serializing and deserializing an text content is more easier for some XML preprocessors (and thus, more efficient)~~. The reason why it is I don't know.

About this topic, see [Is serializing innerText of a tag with XML preprocessor is faster than serializing value of an attribute?](https://github.com/40843245/OOXML/blob/main/Q%26A/about%20serialization/Is%20serializing%20innerText%20of%20a%20tag%20with%20XML%20preprocessor%20is%20faster%20than%20serializing%20value%20of%20an%20attribute%3F.md)

### chats with Google Gemini
Let's hear Google Gemini's answer about this question.

<img width="684" alt="image" src="https://github.com/user-attachments/assets/949a6d0e-641b-4c5a-bd76-e39fc738bafb" />

<img width="645" alt="image" src="https://github.com/user-attachments/assets/c9cbe17d-450f-47ec-914a-86b29851fa3f" />

<img width="653" alt="image" src="https://github.com/user-attachments/assets/5b4349d3-87d2-49c7-b274-cdfb62812a54" />

<img width="644" alt="image" src="https://github.com/user-attachments/assets/1d7b9ce4-f8a7-42a5-83c5-2ebba71be0e0" />

<img width="671" alt="image" src="https://github.com/user-attachments/assets/f54dbb0c-a5e9-47f8-81fb-a8f39094d3ab" />

<img width="652" alt="image" src="https://github.com/user-attachments/assets/e4012c17-9b8c-4050-a996-3a7e4eeae6d1" />
