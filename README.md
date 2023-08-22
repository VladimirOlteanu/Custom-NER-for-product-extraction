# Custom NER (Named Entity Recognition) application for product extraction

This was my first attempt at training a custom Spacy NER model used to detect products in product description. 

This repository contains the following:

* the Jupyter Notebooks used to web-crawl the data, annotate the products and train the model
* the files related to the application and the deployment to Cloud Run (Google Cloud Services)

First I web-crawled product descriptions 
from several websites (multiple categories of products), annotated the products and stored the annotations in a dictionary. Afterwards, 
I trained custom Spacy NER models using the Roberta transformer architecture. Stored the best model (with an F1-score of 81% on test data) 
and used it to develop a Flask application. I wrote the Python Flask script, encompassed the templates (HTML and CSS for the website), 
wrote a Dockerfile and a .dockerignore file and saved the requirements.txt file from the application. Finally, I deployed the application 
to Cloud Run via the docker image created (built in Docker beforehand). 

In order to test the application you can write "The Texawood Adirondack Lounge Rocker combines classic comfort and innovative manufacturer. 
Guests will love its durable design and relaxing rocking motion and you’ll love that it doesn’t require any waterproofing or painting" 
in the application window (Home tab). This is how the output should look like:

![image](https://github.com/VladimirOlteanu/Custom-NER-for-product-extraction/assets/62969646/ebf0da16-819e-402f-b003-d30f2cae3095)




