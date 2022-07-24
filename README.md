# PhD-Task
In literature, I found that deep learning model called ARU-Net [1] works on historical documents by detecting lines of text. The ARU-Net model performs pixel-labelling. For achieving this task, ARU-Net model is used that takes historical document image as input and predicts lines of text and gives output in binarized image.
Once the output of ARU-Net is produced which is binarized image containing lines of text on that location in form of pixels, both original historical document image and binarized image are combined with image processing techniques to highlight lines below the text in original image. Two main post-processing tasks were performed to combine and blend image using image resize and weighted function from opencv library. Image resizing is performed to make sure both images are of same size so that both images can easily be combined. After that, two experiments are performed. Experiment one involves using addWeighted function in which weight for original image was 0.8 and for binarized image, it was 0.5 to make more visible line below the text. Experiment one involves selecting pixels with white color from predicted image are highlighted with red color on original image.

#Challenges

Challenge 01: Most of these historical documents are dark and contains text whose pixel values are matching with paper pixels values so to separate both, it is much difficult.
•	Solution: Need to perform background subtraction based on text and different operations will be involved, depending on different types of text

Challenge 02: Some images were different, so ARU-Net model didn't detect even single line.
•	Solution: Need to train model on these types of images, for training, again preprocessed dataset is required
