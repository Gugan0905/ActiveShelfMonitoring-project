# Data Collection Tasks
## Choosing the Dataset
Most of the large-scale datasets such as Google AI Open Images, ImageNet, COCO, Youtube-8M focus on everyday photography or urban street scenes, which makes them of limited use for many industrial applications. Furthermore, the amount and diversity of labelled training data is usually much lower in industrial settings. To train a visual warehouse system, for instance, the user typically only has a handful of images of each product in a fixed setting. Nevertheless, at runtime, the products need to be robustly detected in very diverse settings. Only a few datasets focus on industry-relevant challenges in the context of warehouses. The Freiburg Groceries Dataset, SOIL-47, and the Supermarket Produce Dataset contain images of supermarket products, but only provide class annotations on image level. The MVTec D2S Grocery dataset, RP2K, Grocery Products Dataset and GroZi-120 include bounding box annotations that can be used for object detection. However, in Grocery Products Dataset and GroZi-120 not all object instances in the images are labeled separately.
So, the datasets on grocery products with bounding box annotations for each instance of an object are MVTec D2S Grocery dataset and RP2K. MVTec’s grocery dataset has 7980 images with boundary box information for 60 products whereas, RP2K has 500,000 images on 2000 products. However, there are some issues with the RP2K dataset website due to which the dataset was not accessible. Also, training half a million images on limited resources is also not viable. So, the MVTec D2S Grocery dataset is chosen. 
![](https://i.imgur.com/lFlnqDi.png)

## MVTec D2S Supermarket dataset
Out of the 7980 images which are labelled in the MVTec dataset, 4380 images only contain objects of a single class on a homogeneous background are used for training, while the remaining 3600 images are much more complex and diverse. So, I split the 3600 diverse images into a 50-50 split for validation and testing.  
Now, dataset is split into :
* Training - 4380 images 
* Validation -1800 images 
* Test - 1800 images  

Training dataset : 
  - Has same background
  - No clutter
  - 6900 objects in 4380 images 
  - Average number of objects per image is 1.58  
  
Validation and testing datasets :
- Has variation in background
- Has clutter
- 15654 objects in 3600 images
- Average number of objects per image is 4.35
- More number of images with occlusion

## Dataset Link : https://www.mvtec.com/company/research/datasets/mvtec-d2s/