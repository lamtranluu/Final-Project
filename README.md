![Header](https://github.com/lamtranluu/lam.labwork/blob/main/Final%20Project/Image/Modern%20Desktop%20Writing%20Workshop%20Google%20Classroom%20Header%20.png)


## 📖 Table of Contents:
* [Context](https://github.com/lamtranluu/lam.labwork/blob/main/Final%20Project/README.md#context)
* [Objectives](https://github.com/lamtranluu/lam.labwork/tree/main/Final%20Project/README.md#-objectives)
* [Tools Requirements](https://github.com/lamtranluu/lam.labwork/blob/main/Final%20Project/README.md#%EF%B8%8F-tools)
* [Method](https://github.com/lamtranluu/lam.labwork/blob/main/Final%20Project/README.md#%EF%B8%8F-method-)
* [Outcomes](https://github.com/lamtranluu/lam.labwork/tree/main/Final%20Project#-outcomes) 
* [Conclusions](https://github.com/lamtranluu/lam.labwork/tree/main/Final%20Project#%EF%B8%8F-conclusions) 

## Context 
Marvel and DC are two of the most popular film producers in the movie industry. Both brands have gained very high engagement from audiences, which can be proved by their success in box office revenue. 30% of the top 20 highest-grossing box office revenue belongs to Marvel & DC movies.
- However, let's explore a bit deeper their success per company. According to the top 10 successful movies in each brand, Marvel gained remarkable gross revenue of 1,5B (over 70%) compared to DC's revenue (850M) by using a slightly higher budget 20%  more than DC to produce movies.
- The winning of Marvel has inspired me to analyze which factors have contributed to their success in the movie industry, therefore I decided to take a look at 20,000 movie reviews to find my answers.
## 🎯 Objectives 
**1. Conduct sentiments analysis between Marvel & DC based on movies reviews.**

**2. Present the correlation between review rating & revenue.**
## ⚙️ Tools:
 ![](https://img.shields.io/badge/Tableau-Visualization-informational?style=flat&logo=tableau&logoColor=white&color=2bbc8a)
 ![](https://img.shields.io/badge/Python-Code-informational?style=flat&logo=python&logoColor=white&color=2dbc8a)
- Requirements :
- Web Scraping
- NLTK,sklearn, CountVectorizer, TfidfVectorizer,word_tokenize
- NRC Lexical, VADER...
 
## ⚙️ Method :
1. Write a Web Scraping function in Python to gather 20,000 reviews from 20 movies on the IMDB website.
2. Implement a Data Cleaning process to clean data:
- remove special characters & repeated sentences which are at the bottom of each review
- change words to lower case
- Implement Data Processing:
- tokenize reviews, stopwords removal 
3. Sentiment Analysis with VADER & AFINN: these lexicon sentiment analyses don't provide an appropriate result, as many positive sentiments still belongs to the low rating group (1-3) from audiences
4. Sentiment Analysis with Classified Modeling:
- Select another movie dataset (50,000 rows) from Kaggle with human labeled.
- Apply 2 different feature selections to compare the accuracy: BOW & TFIDF
- Train Logistic Regression Model with 90% accuracy
- Apply a better model on a data set from Marvel & DC. 
5. Define topic classification by using Bag of Words to extract keywords, which are relevant to certain topics
<img align="center" src="https://github.com/lamtranluu/lam.labwork/blob/main/Final%20Project/Image/Screenshot%202022-03-17%20at%2021.29.01.png " width="700px">
 
## 📌 Outcomes:
- [Tableau Visualization](https://public.tableau.com/app/profile/lamluu/viz/MarvelDC_16475584767410/Plot?publish=yes)

- Presentation [Click here!](https://docs.google.com/presentation/d/1YhR9P3Um8dC1JiCj-YhAKnE8qQ2iYOBxy8SBqLaViWo/edit#slide=id.p)

1.There is a correlation between higher rating and high revenue
<img align="center" src="https://github.com/lamtranluu/lam.labwork/blob/main/Final%20Project/Image/Plot.png" width="600px">

2. Marvel gained more positive reviews around 6% , compared to DC based on IMDB reviews
<img align="center" src="https://github.com/lamtranluu/lam.labwork/blob/main/Final%20Project/Image/Screenshot%202022-03-17%20at%2022.47.12.png" width="600px">

3. 8/12 of the movies with the positive sentiment from Marvel
<img align="center" src="https://github.com/lamtranluu/lam.labwork/blob/main/Final%20Project/Image/Screenshot%202022-03-18%20at%2000.12.54.png
" width="500px">

4. By using BOW features, we extracted the most common key words, which are mentioned in positive reviews from Marvel & DC
- We can see that Marvel audiences mentioned about name of favorite characters, showed their engagement with these adjectives (great, good, one of the best), also **1 interesting points** they tend to mention more about the fact : franchise sequence in Marvel, which is one of most points stimulate Marvel 's revenue  
<img align="center" src="https://github.com/lamtranluu/lam.labwork/blob/main/Final%20Project/Image/MV_wordcloud.png" width="500px">
In term of audience emotions ( using NRC Lexical to get the indicator), Marvel gained around 20% trust from audiencens
<img align="center" src="https://github.com/lamtranluu/lam.labwork/blob/main/Final%20Project/Image/Screenshot%202022-03-18%20at%2000.10.32.png" width="500px">

5. When look at positive word cloud of DC: user also mentioned about character but mainly around Batman, DC fan seems pay attention more about the actors who stared at the role in movies since most keywords appeared with real name of actors, these engageing keywords also be mentioned (great, good...)
<img align="center" src="https://github.com/lamtranluu/lam.labwork/blob/main/Final%20Project/Image/DC_wordcloud.png" width="500px">

6.Lastly, in order to understand which topic are releated to user review, i designed some list of words, use BOW feature to find downd the number of words in each reviews.
- For example, from word cloud Marvel, we obtained the point that audience love the action sequence from Marvel series, there for i create a list which indicated about the curiosity , such as: 'post credit','easter egg','curious','eager','wait' to know in which topic Marvel recieved more psotive feedbacks.
<img align="center" src="https://github.com/lamtranluu/lam.labwork/blob/main/Final%20Project/Image/Screenshot%202022-03-18%20at%2000.10.47.png" width="500px">

- Curiosity topic associated 4.5x more with positive than negative reviews for Marvel movies and double than DC movies

- By contrast, as DC's user wrote more reviews about name of actors, the chart showed: in positive reviews Acting topic associated 4x more with positive than negative reviews for DC movies. The appealing acting of actors is a reason which leaded DC 's revenue
<img align="center" src="https://github.com/lamtranluu/lam.labwork/blob/main/Final%20Project/Image/Screenshot%202022-03-18%20at%2000.10.54.png
" width="700px">
 
## ‼️ Conclusions:
- Sentiment analysis shows a higher customer satisfaction with Marvel´s top grossing movies than those of DC
- The high positive sentiment of the first Avengers movie might have led to the success of the Avengers movie sequence 
- Similar DC attempts such as Batman v Superman and Justice League have very low positive sentiment

- Marvel is successful in maintaining audience ‘s engagement and attention to movies sequence

- Marvel has used the element of curiosity (post-credit scenes, easter-eggs) to drive positive sentiment
- This helps in keeping the discussion alive and bringing customers back to the cinema

 
