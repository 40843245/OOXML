# CH6 -- Files in .xlsx file
## objectives
In this chapter, you will learn

+ Which files are located under a ziparchive that is renamed from `*.xlsx` file in different circumstance?
+ What does these file mean?

## CH6.1 -- Which files are located under a ziparchive that is renamed from `*.xlsx` file in different circumstance?
### circustimance 1 -- when an image is inserted from local device
When an image is inserted from local device, you will see the image will in the worksheet. 

In ziparchive, the image will be copied under `~/xl/media` directory, and be named `image1.{fileExtension}`

where `{fileExtension}` is the file extension of the image that you inserted, and so on.

For example, 

I insert an image named `五十嵐雙葉.png` from local device, the image will be named as `image1.png` and be copied under `~/xl/media` directory.

then I insert an image named `死神娜娜.jpeg` from local device, the image will be named as `image2.jpeg` and be copied under `~/xl/media` directory.

### circustimance 2 -- when a video is embedded from local device
When a video is embedded from local device, you will see an hyperlink of an image in the worksheet.

<img width="190" alt="image" src="https://github.com/user-attachments/assets/f73f08c3-631c-461a-8569-549edbc7d3cd" />

When you double-click it with left mouse, you will try to open the video. 

<img width="707" alt="image" src="https://github.com/user-attachments/assets/2becf823-1255-4629-bb4d-41df8436616d" />

In ziparchive, you will see a file named `oleObject1.bin` under `~/xl/embeddings` directory

and a `*.emf` file named `image1.emf under `~/xl/media` directory.

<img width="198" alt="image" src="https://github.com/user-attachments/assets/cabf9f25-79e0-41d4-9304-1141d46eb0ea" />

> [!WARNING]
> Under  `~/xl/media` directory, if the image name is used (regardless the file extension, it will named with `image` followed by next index followed by `.emf`).

For example, 

I insert an image named `五十嵐雙葉.png` from local device, the image will be named as `image1.png` and be copied under `~/xl/embeddings` directory.

then I insert an image named `死神娜娜.jpeg` from local device, the image will be named as `image2.jpeg` and be copied under `~/xl/media` directory.

next, I insert an embedded video named `アノーイングさんさんウィーク.mp4` from local device, 

the `oleObject1.bin` will be copied under `~/xl/embeddings` directory, 

and `image3.emf` under `~/xl/media` directory.
