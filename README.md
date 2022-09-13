# Topic-Modelling-on-BBC-News-Articles-using-LDA

This is the fourth capstone project I've done in my [Almabetter](https://almabetter.com) Data science curriculam. In this project I've implemented LDA (Latent Dirichlet Allocation) algorithm for modelling the topics on the BBC news articles.

## **Abstract**
[BBC](https://www.bbc.com/) stands for British Broadcasting Corporation.

It is an operational business division of the British Broadcasting Corporation (BBC) responsible for the gathering and broadcasting of news and current affairs in the UK and around the world. The department is the world's largest broadcast news organisation and generates about 120 hours of radio and television output each day, as well as online news coverage. The service maintains 50 foreign news bureaus with more than 250 correspondents around the world.

BBC News Online is the BBC's news website. It is one of the most popular news websites in the UK, reaching over a quarter of the UK's internet users, and worldwide, with around 14 million global readers every month. 

The website contains international news coverage as well as articles based on *entertainment*, *sports*, *science*, and *political* news.


## **Objective**

In this project, the task is to identify major themes/topics across a collection of BBC news articles.


## **Data Gathering and description**

The Data provided is divided into 5 categories, that are, Sports, Tech, Business, 
Entertainment and Politics. Across these 
folders the data is stored in form of text files 
such that each text file contains the complete 
transcript of the article.

The dataset in this 
case isn't collective, it has been stored in 
form of numerous text files sub-categorized 
in 5 different domains. First I 
segregated the data by 
traversing all these folders and storing the 
data present in the files to a data-frame.
 
**Following are the attributes of the dataset:**

* **Index**: Entry index.
* **Filename**: Destination File 
name/number.
* **Contents**: Complete transcript of a
article, this contains all the textual 
data present in the destination file for 
a particular entry.
* **Category**: Theme/domain of a 
article

The dataset is available at [kaggle](https://www.kaggle.com/).

## **Python Libraries used**

**Datawrangling and manipulation:** 
* Numpy
* Pandas

**Visualization:** 
* Matplotib
* Seaborn 
* Wordcloud
* TQDM
* IPython

**Machine learning Models:**
* Scikit-Learn (LDA)

**Others:**
* warnings
* collections
* NLTK
* ast

## **Model Development**

Here I've used the LDA (Latent Dirichlet Allocation) algorithm for modelling the topics on the BBC news articles.

These are the optimal LDA metrics that I got after implementing GridSearchCV:

    Best LDA model's params: {'n_components': 5}

    Best log likelihood Score for the LDA model: -643494.9704171557

    LDA model Perplexity on train data: 1696.6352006244963


## **Notable Findings**

* While reading the text files, I noticed that the file encoding was different in a few off-cases. Considering such factors, and engineering based on such knowledge, is very important while handling such data, in order to perform tasks efficiently.

* Upon experimenting with stemming and lemmatization on our dataset, I found that although it saves space and perhaps time, in our case, it's better to focus on quality, and avoid nuances. In my own 'cost-benefit' analysis, the difference weren't all that significant. Perhaps at a massive scale, the former approach would be ideal.

* Noticed that its more optimal to tokenize with no factual differences, hence lowercased the contents to unify tokens that may have just case-differences.

* Upon looking at the top n topics generated, I was able to correlate it with relevance to what was expected at a significant degree, whilst also shedding light on some unseen aspects. Hence, I see that the model effectively beared fruits.
