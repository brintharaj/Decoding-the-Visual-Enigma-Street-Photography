# Decoding-the-Visual-Enigma-Street-Photography

## Requirements
To install the required dependencies, run: pip install -r requirements.txt

## Background
Visual styles are perceived subjectively, but useful information can be extracted from images that may lend insights into what makes them similar or dissimilar. This also implies that visual preferences and image recommendations may be inferred from existing user preferrence. What makes this task a challenge is the high diensional structure of the data matrix, and how less meaningful euclidean distance metrics become in high dimension.

This notebook explores the use of ISOMAP and LocallyLinearEmbedding for dimensionality reduction and manifold learning of visual styles pertaining to street photography. Visual features are engineered to generate the data matrix, considering features such as histogram of colour hues, saturation and birdgtness, as well as image composition, texture, contrast. Over 300 images are sourced from the open web for this exercise.

## Notebook Instructions
1. Replace the folder path.
2. Load the desired images in stated folder.
3. Run the notebook.

## Summary
The results indicate ISOMAP Method 1 (radius: 116 and number of components: 110) gives exact same recommendations as ISOMAP Method 2 (number of neighbours: 153, number of components: 7). METHOD 2 tuning process is observed to be faster (expected to vary in reality, depending on parameter grid chosen). This implies METHOD 2, with the lower dimension and denser adjacency matrix, may be preffered if the computational gains can be scaled in volume, to real applications for visual preference manifold learing.

Comparing ISOMAP with LLE by visual inspection of the recommended images, it does appear ISOMAP performs better (according to what I perceive as stylistically similar in accordance to the features defined and engineered from the images). However, given subjectivity of visual preferrences, large scale A/B testing will be required to experiment and develop a generalized model that can cater to a variety of stylistic preferrences and subjectivity in image analysis (not just mine).
