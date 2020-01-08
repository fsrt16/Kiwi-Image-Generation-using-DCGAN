# Kiwi-Image-Generation-using-DCGAN


# Introduction
## Generative Adversarial Networks (GANs)
How GANs Work
GANs Process
Examples
Generative Adversarial Networks (GANs)
Generative Adversarial Networks are used to generate images that never existed before. They learn about the world (objects, animals and so forth) and create new versions of those images that never existed.

They have two components:

# A Generator -
this creates the images.
# A Discriminator - 
this assesses the images and tells the generator if they are similar to what it has been trained on. These are based off real world examples.
When training the network, both the generator and discriminator start from scratch and learn together.

# How GANs Work
G for Generative - this is a model that takes an input as a random noise singal and then outputs an image.



A for Adversarial - this is the discriminator, the opponent of the generator. This is capable of learning about objects, animals or other features specified. For example: if you supply it with pictures of dogs and non-dogs, it would be able to identify the difference between the two.



Using this example, once the discriminator has been trained, showing the discriminator a picture that isn't a dog it will return a 0. Whereas, if you show it a dog it will return a 1.



N for Network - meaning the generator and discriminator are both neural networks.

# GANs Process
## Step 1 - 
we input a random noise signal into the generator. The generator creates some images which is used for training the discriminator. We provide the discriminator with some features/images we want it to learn and the discriminator outputs probabilities. These probabilities can be rather high as the discriminator has only just started being trained. The values are then assessed and identified. The error is calculated and these are backpropagated through the discriminator, where the weights are updated.



Next we train the generator. We take the batch of images that it created and put them through the discriminator again. We do not include the feature images. The generator learns by tricking the discriminator into it outputting false positives.

The discriminator will provide an output of probabilities. The values are then assessed and compared to what they should have been. The error is calculated and backpropagated through the generator and the weights are updated.



## Step 2 - 
This is the same as step 1 but the generator and discriminator are trained a little more. Through backpropagation the generator understands its mistakes and starts to make them more like the feature.

This is created through a Deconvolutional Neural Network.

# Examples
GANs can be used for the following:

## Generating Images
## Image Modification
## ## Super Resolution
## Assisting Artists
## Photo-Realistic Images
## Speech Generation
## Face Ageing
