# Myntra-HackerRamp: WeForShe
Team: ALPHA GEEKS

Almost everyone wishes to try items before they buy them but are unable to do so due to the online shopping mode. The pandemic has further made comfortable online shopping the need of the hour.The lack of physical shopping experience causes approximately 23% of all clothing to get returned, and 64% of consumers say incorrect fit is the primary reason they return clothing as it is not easy to predict that which size would best fit on them.


# Proposed Idea
We are offering a secure solution where a user can capture his/her entire body picture and upload it on Myntra app. The system will scan the body size and suggest the best fit of a particular clothing that the customer has selected.
FUTURE GOAL
The customer can also virtually try on the clothes to decide whether it looks good on their specific body type or not. This will increase the customer satisfaction and thus the sales of the Myntra App.

#Installation
!pip install opencv-python==4.4.0.40
!pip install scikit-image
!pip install pixellib


# Requirement from the User
•	Images of their full body
•	Height and Leg Length in cm

# Instructions for uploading Images
•	BACKGROUND :
Background should be a plain. It should not contain any switches, sofa, wall papers or any other objects.


CORRECT 

![image](https://user-images.githubusercontent.com/60663789/114011695-28f1b900-9883-11eb-8434-22b1d7c0500c.png)           

WRONG

![image](https://user-images.githubusercontent.com/60663789/114011883-5b031b00-9883-11eb-9251-191f9024b1ff.png)

WARNING: The colour of your outfit should not be similar to that of your background.


•	POSE :
Users have to provide the photos in the following given poses.


![image](https://user-images.githubusercontent.com/60663789/114013812-97377b00-9885-11eb-8ea5-cd28a8e07695.png)  ![pose2](https://user-images.githubusercontent.com/60663789/114013925-b2a28600-9885-11eb-8b10-f9fef2037344.PNG) ![image](https://user-images.githubusercontent.com/60663789/114013987-c5b55600-9885-11eb-8dc9-ec82fd14067f.png)



NOTE: Wear tight fitted clothes for accurate measurement


•	Distance :
Stand at a distance from the camera such that it covers your whole body(head to toe),  also make sure that no extra space(floor) or object is covered in the frame.

#Technologies

> Python Programming Language

> Google Collab: For writing and executing our code.

> ML library stack(pandas, numpy, matplotlib, scikit learn etc)

> Open CV: For Image Processing and Editing

> Dataset: Pre-Trained Model (mask_rcnn_coco) which is a data model of common objects through pixellib package.



#Solution

1.Taking input from the user : In this step, the users will be providing their full body images in two poses (Front and Side).
2.Image Segmentation: Detecting human body and forming a rectangle around the picture ( Using an Open CV function).
3.Image Cropping and Resizing: Cropping the image to separate it from its background and Resizing it in a particular format.
4.Detection of Body Parts: Flood-Fill Algorithm of Computer Graphics is used in this phase to detect various body parts of a person.
5.Measurement of Body Parts:

	1. Pixel Counts: The concept of Head to Height Ratio(1/7.5) is used to calculate the pixel counts of the detected body parts in the previous step.

 	2. Actual Measurement: To find the relation between the pixels and the exact value, Linear Regression is used.

6.Size Estimation: We used a general measurement chart for our reference and converted it into a dataset to compare our results with an actual reference and thus giving out the best size as an output.










                                                                                             
