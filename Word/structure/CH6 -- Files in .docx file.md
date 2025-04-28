# CH6 -- Files in .docx file
## objectives
In this chapter, you will learn

+ Which files are located under a ziparchive that is renamed from `*.docx` file in different circumstance?
+ What does these file mean?

## CH6.1 -- Which files are located under a ziparchive that is renamed from `*.docx` file in different circumstance?
### circustimance 1 -- when an image is inserted from local device
When an image is inserted from local device, you will see the image will in the worksheet.

In ziparchive, the image will be copied under `~/document/media` directory, and be named `{guid}.{fileExtension}`

where 

`{guid}` is the guid of the image that you inserted. 

`{fileExtension}` is the file extension of the image that you inserted, and so on.

For example,

I insert an image named `Ai.jpg` from local device, the image will be named as `e7b5f2f4-8ffa-467d-9d08-319f16fc3621.jpg` and be copied under `~/document/media` directory.

then I insert an image named `Midori.jpg` from local device, the image will be named as `fd3e32a4-3dce-44e8-852b-8f16121497ed.jpg` and be copied under `~/document/media` directory.
