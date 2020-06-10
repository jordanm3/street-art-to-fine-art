   # Street Art to Fine Art: *Art Recommendation using Deep Learning*

[Michael Jordan](https://www.linkedin.com/in/michaeljoshuajordan/)  
April 2020

<p align="center">
Click image below for a video presentation demonstrating the recommendation tool in action:
</p>

<p align="center">
<a href="https://www.youtube.com/watch?v=VMcK-Z3naK4&feature=youtu.be" target="_blank"><img       src="https://cdn.buttercms.com/jq9R20pTEmusaIsCE3TU" 
alt="Street Art to Fine Art" width="480" height="360" border="10" /></a>
</p>

## Table of Contents
* [Overview and Motivation](#overview-and-motivation)
* [Methodology](#methodology)
* [Results](#results)
* [Conclusion](#conclusion)
* [Acknowledgments](#ackowledgments)

## Overview and Motivation
- For this project, my motivation was to develop a recommendation tool that could take a user-uploaded image of street art and return images of fine art, along with relevant information about the artwork, that are most visually similar. 

## Methodology 
Implementation of this project involved: 

1. Build a corpus of 35,000+ images and metadata using the public APIs from the following sources:   
      a. [The Metropolitan Museum of Art (The Met)](https://github.com/jordanm3/street-art-to-fine-art/blob/master/data_collection/met_data.ipynb)  
      b. [The Museum of Modern Art (MoMA)](https://github.com/jordanm3/street-art-to-fine-art/blob/master/data_collection/moma_data.ipynb)

2. Create a single master dataframe containing the metadata from the images scraped from both The Met and MoMA. [Code for this step can be found here.](https://github.com/jordanm3/street-art-to-fine-art/blob/master/data_collection/metadata_final.ipynb)

3. Train a convolutional neural network autoencoder. Perform dimensionality reduction by taking the images of my corpus and passing them through 3 convolutional and pooling layers that learn the image’s features. Produce a narrow encoded layer that contains the lowest possible dimensions of the input data, allowing comparison between images to be computationally feasible. [Code found here.](https://github.com/jordanm3/street-art-to-fine-art/blob/master/models/autoencoder_model.ipynb)

4. Use the narrow encoded layer to encode the corpus of fine art images and a test street art image, resulting in a set of feature tensors. Use cosine similarity to compare the street art image to every fine art image in the corpus to find the most visually similar matches. [Code found here.](https://github.com/jordanm3/street-art-to-fine-art/blob/master/models/image_comparison.ipynb) 

## Results

## Conclusion

## Acknowledgments

