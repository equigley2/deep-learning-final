<h1> CNN Image classification </h1>

<h6>Team:</h6> Kevin Handel, Ross Kantor, Chris Lawton, Emily Levis, Emily Quigley  

<h6> Data Set:</h6> CIFAR-10

<h3> Plan </h3>
MVP: CNN
<br>
MVP 2: VGG16


<h3> Team Organization </h3>
<u>Wednesday Meeting:</u>
<br>
<br>
Met Wednesday for group meeting
<br>
Read through repo and discussed models
<br>
Agreed to individually research questions discussed
<br>
Goal was to start Thursday with data ready and preliminary model ready for testing
<br>
<br>
<u>Thursday Structure:</u>
<br>
CNN team: Chris & Ross
<br>
VGG team: Emily L, Emily Q, Kevin
<br>
All team members: glorified error handlers

<h3> Data Structure </h3>
Downloaded the files which came as tarball file with 5 pickled batch files in sets of 10,000, 1 labels file, and a test file.
<br>
<br>
Data was organized as a dictionary as shown below.
<br>
<br>
dict_keys([ ' batch label ' , ' labels ' , ' data ' , ' filenames ' ])
<br>
<br>
One image was made up of 32x32x3 but in an compact structure.

<h3> CNN Modeling </h3>



1. 5 hidden layers
2. Each layer used padding
3. Optimizer used was Adadelta
4. Every activation was ReLU except the end was Softmax

One issue we encountered was downsampling beyond a 1 X 1 image.
<br>
We poured significant effort into perfecting a Convolutional Neural Network.  After numerous errors Chris perfected the network.

<img src="10Images.png">
<img src="history.png">
<img src="full_model_acc_loss.png">

<h3> VGG16  Modeling </h3>
<img src="vgg_macroarchitecture.png">
1. VGG is  pretrained model so all of the inner workings you see in the photo, we aren't able to make changes
2. VGG 16 indicates 16 weight layers
<!-- <img src="vgg_macroarchitecture.png" alt="Smiley face" height="100" width="100"> -->
<br>
3. First, we ran through one batch of 10,00 to test on a smaller segment of photos
4. Model clearly did not perform well because the true label wasn't in our top 3 predictions
5. We assume our images didn't classify well due to the low resolution

<img src="percentages.png" height="500">

<img src="value3.png">
<img src="value6.png">
<img src="value7.png">
<img src="value9.png">
<img src="value1.png">
<img src="value2.png">
<img src="value14.png">
<img src="value16.png">

<h3> Complications </h3>
* Data organization issues
* Naming issues
* Sizing the images after pooling, used padding to solve
* Initial model was guessing 10%
* Data sizing issues to make batches and then resize larger for the VGG model

<h3> Learnings </h3>
* Be patient, models take time to improve,  if you don't wait long enough you might change something pre-emptively

<h3> Future Work </h3>
* Build and perfect a model the night before.
* Understand shapes
* Drop $2500 for high-end computing power (stand up Amazon account sooner)
* Transfer Learning
<br>
* Test with new images from online
* Use better resolution photos to improve our model
* Test with VGG19
