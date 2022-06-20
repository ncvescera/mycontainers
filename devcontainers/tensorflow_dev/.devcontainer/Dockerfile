FROM tensorflow/tensorflow:latest-gpu

RUN apt-get update -y && apt-get upgrade -y
RUN apt-get install wget graphviz -y
RUN pip install matplotlib pandas sklearn transformers seaborn 
RUN pip install pydot pydotplus graphviz
