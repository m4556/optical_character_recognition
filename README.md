# custom OCR 

###  Project Overview
<img src="https://github.com/m4556/t/blob/main/SE_-OCR_1(2).png" width="600" >

Goal: Create OCR pipeline from scratch to detect and extract information from invoice documents. The model is trained to identify 3 essential classes from the invoices: Invoice number, Billing Date, and Total amount.

Using Deep Learning for OCR is a three-step process:
1. **Data collection:** Collect data.
2. **Text Detection/Localization:** Next phase is to locate the text in images, by creating bounding boxes(rectangles) over the text. 
3. **Text Recognition:** Once the text location is identified, each bounding box is sent to the text recognition model.

### Data collection
Dataset contains different image of digital invoices. After that, annotation tool was used to make annotations for targeted classses. 
<img src="https://github.com/m4556/t/blob/main/New%20Project(1).png" width="600" >
 
### Text detection model

There are many approaches for text detection, such as:
- Region Proposal-based Methods: These methods propose potential regions of text in an image and then classify them as text or non-text. One popular approach is the FRCNN.
- Regression-based Methods: These methods directly regress the coordinates of the bounding boxes around the text in the image. Examples include YOLO.
- Segmentation-based Methods: These methods segment the text regions from the background by predicting pixel-level text masks. FCN and U-Net architectures are commonly used for text segmentation.

In this project we use transfer learning to fine tune YOLOV8 on a custom invoice dataset.


###  Text recognition model
Once the text location is identified, each bounding box is sent to the text recognition model which is usually a combination of RNNs, CNNs, and Attention networks,or open source models like  like Tesseract, MMOCR.

In this project we will use Tesseract pretrained LSTM for text recognition.


### Results
<img src="https://github.com/m4556/t/blob/main/new.png" width="600" >


