# Amazon-apparel-recommendation-engine

### Table of Content:

1. [Project Motivation](#motivation)
2. [Descriptions](#file)
3. [Installation](#installation) 
4. [Results and Improvements](#results)
   
## Project Motivation : <a name="motivation"></a>
Building an unsupervised content based recommendation engine. We want to build a recommendation engine that recommends users of Amazon similar products to one they are currently browsing using text description of all the products. 

What are we intereseted in answering the following question:
1. Which Amazon products are similar to current product being browsed by the user?

## Descriptions : <a name="file"></a>
The dataset `topfashions.json` used in this notebook is a simplified version of the real Amazon app with limited number of products.

Here is the explanation of each pertinent feature in the file :

   `topfashions.json`
   - asin : Amazon Id of the product
   - medium_image_url : Image of the product
   - product_type_name : Type of apparel
   - title : Text description of the products 
   - formatted_price : Price of the products in $

The three notebooks we see perform the follwong functions:
   - ETL Notebook : This notebook contains the implemented Extract, Transform and load pipline (ETL pipeline).
   - Modelling Notebook : This notebook contains the Machine learning pipeline developed with NLTK and Scikit-Learn.
   - Amazon recommendation engine : Run this notebook to see the results.


The description of various .npz files and pickle file saved in the 'Pickle' folder is as follows:
   - Word2Vec_aveg.npz : Saved Avg Word2Vec vectorized matrix using machine learning pipeline to avoid computationally expensive vectorization before each product recommendation.
   - Word2Vec_weighted.npz : Saved weighted Word2Vec vectorized matrix using machine learning pipeline to avoid computationally expensive vectorization before each product     recommendation.
   - idf_title_features.npz : Saved idf vectorized matrix using machine learning pipeline to avoid computationally expensive vectorization before each product recommendation.
   - preprocessed_data : Saved usable data after ETL pipleline implementation.

## Installation : <a name="installation"></a>
  - Gensim 4.0.1 for using pretrained word2vec library by Google.
  - Cython 0.29.21 for using pretrained word2vec library by Google.
  - Matplotlib version 3.2.0 for heatmaps.
  - Python version  3.*.




## Results and Improvements: <a name="results"></a>

Seeing our results we cannot determine which vectorization model is giving us better results. To find out which model is better we would have to first live test our recommendation models. We would divide our customers into random test groups of equal sizes and live test a model on each group. Second step would be to collect various response parameters or business parameters such as purchase conversion percentage of recommendations, recommendation opening percentage etc. Third step would be to perform multivariate A/B testing using these parameters after collecting sufficiently large data to select the best performing model.


## Licensing, Authors, Acknowledgements<a name="licensing"></a>
Credit to Amazon for providing the data.

   
