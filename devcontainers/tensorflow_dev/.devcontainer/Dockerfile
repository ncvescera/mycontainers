FROM tensorflow/tensorflow:latest-gpu

# update the systems
RUN apt-get update -y && apt-get upgrade -y
RUN apt-get install wget -y

# things for print and display keras models as imgs
RUN apt-get install graphviz -y
RUN pip install pydot pydotplus graphviz

# math and charts libs
RUN pip install matplotlib pandas seaborn 

# sklearn lib. Offers a LOT OF THINGS. Most used for splitting dataset into train set and test/validation set
RUN pip install sklearn

# Hagging Face Transformers lib. Offers a lot of pre-trained NLP models like BERT, AlBERT, ecc
RUN pip installtransformers 

# package for natural language toolkit. Offers things like known set of stopwords, ecc.
RUN pip install nltk