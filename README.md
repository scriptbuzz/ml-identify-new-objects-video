Use Transfer Learning to train an already trained TensorFlow model to recognize new objects.

With these two experiments, I explore Transfer Learning using TensorFlow.js to train an existing model on how to 1) recognize the six sides of a dice and to 2) recognize random scribbles apart.


# 1) Identify The Six Faces Of a Dice: https://youtu.be/ztLTs8Y4ttM #

![tensorflow dice](tensorflow-dice-face-recognition.jpg)


# 2) Identify Random Scribbles: https://youtu.be/gaK89Frg5Zs #

![tensorflow scribble](tensorflow-scribble-recognition.jpg)


The demos shows how to leverge a KNN classifier that can be trained live using webcam captured image.  The captured image from the webcam is  processed by an activation of MobileNet. This network is already trained to recognize many  classes from the popular ImageNet dataset, and is optimized to be compact, making it deployable in the browser.

Instead of reading the prediction values from the MobileNet network, we take the second to last layer in the neural network and feed it into a KNN (k-nearest neighbors) classifier so we can train using custom classes.

By using few samples we can train a classifier that can recognize patterns like smiles or surprised looks, or human genstures. This approach is called Transfer Learning.
