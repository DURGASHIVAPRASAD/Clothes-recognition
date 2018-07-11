Dear readers: If you are reading this NOW (last update 11th July 2018). Works still on going, and commits might be incomplete. 

# Clothes-recognition
Clothes recognition: This is a task given by a company as part of the interview process for an internship role, and deadline is 1 week (17July2018). Due to time constraint, I'm going to tackle this using a few techniques I have already know, since I have ready codes, as baseline. Then if I have more time, I will try out something I don't know, i.e fashionet, based on a paper dated 2016.

## Task details: Copy paste directly from email.
```
Deep Learing based Person Cloth Attribute Indicator
Purpose – Develop or train a deep learning model that can identify the type of cloth (upper and lower body) of person.
Expected Results
·   Deep learning model in Keras/Tensorflow/Caffe that can indicate type of upper and lower cloth of a person.
·   You can determine the number of class for type on your own that you would like to train (please to inform us once you have decided on the type ), example could be long sleeves shirt, short sleeve shirt, sleeveless shirt, suit, jacket etc. for upper body, and short pants, long pants, skirt, jeans etc. for lower body.
·   You can add even more type of person attribute if you could find relevant dataset and confident that they can deliver within the given assignment time.

Requirements, Constraints and Hints
·   The trained model should be robust to viewing angle on a person and different camera.
.   Dataset link is confidential (sorry guys)
·   For your information, the label in the above dataset contains the location of the cloth and its type in their respective images in xml format.
·   If you felt these dataset is not suitable for your test case or you need more data to make the model more accurate, you can use other material in the internet for open source dataset.
·   The targeted accuracy would be at least 90% in determining the type of the cloth.
·   You are also free to use any resources to accomplish the assignment, including: code samples, open source libraries, research materials etc.

Assignment Deliverables
·   Model that can be used in Python/C++ with Keras/Tensorflow/Caffe.
·   A code which input your model and output the results of a selected image.
·   A short write-up/presentation describing your approach/architecture for the deep learning.

Feel free to come back to us for any further clarification on the assignments. Once competed please send the source code, model and report regarding the chosen algorithms and results. You are free to use any resources to accomplish the assignment, including: code samples, open source libraries, research materials etc.
 
Your assignment ranking will be based on the robustness and generalization of the solution and the thought process behind your approach and implementation.
```

## Plan of attack
I have 1 week to do this. After reading [DeepFashion paper ](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Liu_DeepFashion_Powering_Robust_CVPR_2016_paper.pdf), I knew a simple CNN and any transfer learning models is NOT going to give any good result. However its the only few methods I know for now. And I have codes ready for testing. So I went ahead, at least I have some results to show before deadline.

### Timeline: (I am updating this as I move along)
- 9July: Researching. Looking at Github, youtube, blogs, papers. Problem is  First, clothes often have large variations in style, texture, and cutting, which confuse existing systems. Second, clothing items are frequently subject to deformation and occlusion. Third, clothing images often exhibit serious variations when they are taken under different scenarios, such as selfies vs. online shopping
photos 
- 10July : Looking at dataset. It comes with xml annotation and jpg. But not sure what .txt file is for. Spend a bit of time moving to respective classes to its folder names [shorts','dress','tee','jeans','skirt','blouse'], as Keras requirement.
- 11July : Custom CNN using Keras - for baseline. 

Epoch 200/200: 20s 108ms/step - loss: 0.2652 - acc: 0.9001 - val_loss: 0.9794 - val_acc: 0.7589

[Juypter notebook on this: Custom CNN via Keras](https://github.com/noelcodes/Clothes-recognition/blob/master/Custom%20CNN%20baseline.ipynb)

- 11July : Transfer learning VGG16 - another baseline

- 11July : Clean up dataset - some images really sucks
