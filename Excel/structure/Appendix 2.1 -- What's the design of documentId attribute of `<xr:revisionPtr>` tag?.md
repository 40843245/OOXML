# Appendix 2.1 -- What's the design of documentId attribute of `<xr:revisionPtr>` tag?
## Answer
`documentId` attribute in OOXML is an unique identifier of a document, which can identifiy a specific object or element within an Excel file.

You can think it's a fingerprint for that component.

To understand the regularity of document id, let's break it down.

In `~/xl/workbook.xml` under an Office Excel file,

we can know about its format. 

With RE (regular expression), it can be represented as

```
documentId="{documentId}"

{documentId}:= {revisionTrackingIdentifier}_{ncrStandsFor}:{instanceId}_\{{guid}\}
```

where 

+ `{revisionTrackingIdentifier}` is an id (a number) for revision tracking.
+ `_` is a seperator.
+ `{ncrStandsFor}` might relate to `No Conflict Resolution`.

However, it still remain speculative as without deeper internal documentation of Excel's revision tracking.

+ `{instanceId}` refers to the id of the instance of the specific revision tracking component identified by `{revisionTrackingIdentifier}_{ncrStandsFor}` (starting from 1).

For example, if the component is the first revision tracking component. Then `{instanceId}` could be `1`, and so on.

+ `{guid}` refers to 128-bit guid for revision tracking.

### examples
See following screenshot in following references.

### reference
#### from Google Gemini's answer
I ask it to Google Gemini.

<img width="655" alt="image" src="https://github.com/user-attachments/assets/396848cf-b66a-4fe8-97d7-c5078df2e74c" />

Then it answers that 

```
Knowing the context might help narrow down its exact purpose.
```

<img width="647" alt="image" src="https://github.com/user-attachments/assets/90a10f61-2576-475c-a098-510ab3167321" />

Then I copy the content of this file, then ask it and give the file path to Google Gemini

<img width="959" alt="image" src="https://github.com/user-attachments/assets/932d8585-664e-4863-aef9-17a3c830ca34" />

Then it answers that 

<img width="696" alt="image" src="https://github.com/user-attachments/assets/6e175681-92b7-4e0d-9d30-8fb7b55afea3" />

<img width="650" alt="image" src="https://github.com/user-attachments/assets/6917a700-cf99-42e2-939e-534a6d966974" />

<img width="665" alt="image" src="https://github.com/user-attachments/assets/0099c39f-3cfc-48b1-821c-ed76376a2683" />

<img width="620" alt="image" src="https://github.com/user-attachments/assets/3b0f1072-31cd-4281-9509-8fa5a4a243ea" />



