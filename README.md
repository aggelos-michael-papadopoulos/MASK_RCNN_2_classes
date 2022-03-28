# MASK_RCNN-2_classes-

Architecture (Faster RCNN + MASK):

![The-structure-of-the-Mask-R-CNN-architecture](https://user-images.githubusercontent.com/65830412/159546562-639569f0-86d8-4451-8a84-7d509f979463.png)



MASK R-CNN for instance segmantation for two classes:

  1) Glass
   
  2) Pen.

Code from: https://github.com/matterport/Mask_RCNN.
--

Following the steps from AarohiSingla's youtube video:
--
https://www.youtube.com/watch?v=t1MrzuAUdoE&list=PLAIlFCosqqHYcs6MTyVoXmrGjyL_VpjiZ&index=2&t=894s&ab_channel=CodeWithAarohi.
--
But with a few important changes (i uploaded all my files that i executed), because i could not run it otherwise.

Annotation tool: VGG Image Annotator (VIA).
--
# prerequisites
1) Tensorflow 1.15.2
2) Keras 2.3.1
3) h5py < 3.0.0 so 1.21.5 (!pip install 'h5py<3.0.0')
4) scikit-image==0.16.2
5) you can download COCO weights (that you will need in custom.py) from here: https://github.com/matterport/Mask_RCNN/releases/download/v2.0/mask_rcnn_coco.h5

# TRAINING

I run the mask_rcnn_train.ipynb (what we do here in essence is run the custom.py from google colab) and as a result we get the training weights from the last epoch (20th epoch) in a logs file that will create after we ran the traning.

# TESTING
I run the test_glass_pen_model.ipynb with the same prerequisites

As a final result we can see that the Mask-RCNN has done a beautiful job at my testing images 

here are some examples:

///// some pics from my desk /////

![download](https://user-images.githubusercontent.com/65830412/160298939-e4a2c0db-bc9d-4e14-b910-3c49a8e7e37d.png)

![download (1)](https://user-images.githubusercontent.com/65830412/160298949-0f68f1cc-df0f-4d71-b9f9-0cadad889390.png)

///// and one that i downloaded from google ///// :

![download (2)](https://user-images.githubusercontent.com/65830412/160299034-c1cd1aae-ab7d-49c8-89ea-28f821f3f17c.png)


But you can implement the code for whatever photo you like.


--- I ran the whole project on Google Colab (on Colab's GPU), so you have to change the paths on both .ipynb files and on custom.py to fit your paths! ---
