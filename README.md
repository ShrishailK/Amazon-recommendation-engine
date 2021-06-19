# Amazon-apparel-recommendation-engine

### Table of Content:

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Description](#file)
4. [Results and Improvements](#results)

## Installation : <a name="installation"></a>
   We need to install the gensim 4.0.1 and Cython 0.29.21 (Not the latest version) for using pretrained word2vec library by Google and matplotlib version 3.2.0 in order to print the heatmaps.  The code runs with no issues using Python version  3.*.
   
## Project Motivation : <a name="motivation"></a>
Building an unsupervised content based recommendation engine. We want to build a recommendation engine that recommends users of Amazon similar apparels to one they are currently browsing using text description of all the apparels. 

What are we intereseted in answering the following question:
1. Which Amazon products are similar to current product being browsed by the user?

## File Descriptions : <a name="file"></a>
This data set is a simplified version of the real Amazon app because the underlying simulator only has one product apparels whereas Amazon actually sells dozens of different kinds of products.

Here is the explanation of each pertinent variable in the file :

`topfashions.json`
- asin - Amazon Id of the product
- medium_image_url - Image of the product
- product_type_name - Type of apparel
- title - Text description of the products 
- formatted_price - Price of the products in $

## Results and Improvements:
Seeing our results we cannot determine which vectorization model is giving us better results. To find out which model is better we would have to first live test our recommendation models. We would divide our customers into random test groups of equal sizes and live test a model on each group. Second step would be to collect various response parameters or business parameters such as purchase conversion percentage of recommendations, recommendation opening percentage etc. Third step would be to perform multivariate A/B testing using these parameters after collecting sufficiently large data to select the best performing model.


## Licensing, Authors, Acknowledgements<a name="licensing"></a>
Credit to Amazon for providing the data.

   
