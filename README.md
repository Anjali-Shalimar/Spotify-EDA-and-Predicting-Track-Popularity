## **1. Introduction** {.tabset}
Spotify is a digital podcast and music streaming service with over 248 million monthly active users across the globe. The paid service of the company known as 'Spotify Premium', currently has its user base growing at a staggering rate of +31% (year on year growth). While its keen features make an average user spend 25 hours per month on the service, the data behind the scenes is equally interesting to dive in and learn from. This 'king of music streaming' is widely recognized for its personalized music recommendations for its users, and the following analyses look into the key determinants that influence track popularity on Spotify. **The analyses is primarily designed to aid firms and music distributors that operate within the digital streaming services domain.**

```{r pressure, echo=FALSE,fig.width= 200 , fig.height=20,fig.align="center",out.width = '100%'}
# company logo 

knitr::include_graphics("logo.jpg")
```

### 1.1 Problem Statement
There are two main objectives for this analysis.

a. Identify the general trends in music affinity of Spotify users

b. Determine the key influencers of track popularity on Spotify and predict popularity class ( 'high' , 'medium' , 'low' )

### 1.2 Implementation and Techniques

The dataset contains information on the artist, genre, characteristics, and popularity of various tracks on Spotify. The cleaned data would be analyzed using EDA techniques and data mining techniques (such as regression, word tokenization and clustering) in order to implement the objectives(mentioned in 1.1). 

A regression approach such as Random Forest / Multiple Linear Regression would help identify the variable importance in determining track popularity. Tokenization and NLP techniques would help to identify if there is a set of words (in the titles) that come together for more popular tracks. 

### 1.3 Key Consumers of the Analysis

The analyses are primarily designed to aid firms and music distributors that operate within the digital streaming services domain. Identifying user trends would help digital music distributors to better streamline their music offerings. The analysis would also help artists to understand their target consumers better (as the analysis is split by music genre).

***

## **2. Packages Required** {.tabset}

Following are the packages required with their uses:

**tidytext** = To convert text to and from tidy formats

**DT** = HTML display of the data

**tidyverse** = Allows data manipulation 

**stringr** = Allows string operations

**magrittr** = Pipe operator in r programming

**ggplot2** = For graphical representation in r

**dplyr** = For data manipulation in r

**gridExtra** = Allows grod formating of ggplot figures

**pracma** = Allows advanced numerical analyses

**treemap** = Allows treemap visualizations 

**tm** = For text mining

**GGally** = Allows in-depth EDA , works in synchrony with ggplot

**randomForest** = Creates random forest models 

**wordcloud** = For word cloud generator

**plotly** = For creating interactive web-based graphs
## **3.  Summary of the Analysis**{.tabset}

### **3.1 Summarizing the Problem Statement** 

Tha analysis mainly focuses on giving key trends and insights to music artists and music distributors that operate within the digital streaming services domain. The general trends in popularity of tracks were identified for different genres of music and different album release eras. The key elements of similarity in terms of "title words" of highly popular tracks were compared against the less popular ones. Additionally the popularity class of a track was predicted and the key influencers of populairty were determined.

### **3.2 Summarizing the Implementation** 

- Packages such as Plotly was used to represent key trends in an interactive fashion

- Text mininng techniques were used to generate word clouds of track titles (for various popularity classes)

- Random Forest Classifier was used to predict the popularity class of a track 

### **3.3 Summary of Insights and its Implications (to the consumers of this analysis)**

- While 'pop' genre has lower number of total tracks on spotify, it has the highest average popularity score amongst users

- 'edm' and 'rap' have higher number of tracks on spotify, hence new artists of these genres on spotify face a stiffer 
  competition in terms of track visibility
  
- Track popularity slightly decreases with higher song duration and with high instrumentalness of the track

- Tracks with higher danceability index tends to have higher valence ( positivity) scores

- Rock music of the early release eras are more popular than the newly released tracks amongst users

- The popularity of the genre "R&B" is improving amongst the spotify user base, with newly released tracks of the 2010's having   higher popularity than the tracks released in 2000's , 90's and 80's. Artists of this genre, would hence have a 
  higher scope and visibility amongst spotify users. Music distributors could hence focus more on this genre
  
- Tracks with the titles **'dance' , 'hits' , 'hip' , 'hop'** are more frequent in highly popular tracks than in less popular 
  ones
   
- "song_duration" , "instrumentalness" , "loudness" are three key attributes that determine the popularity of a track in 
  spotify
  
### **3.4 Limitations of the analysis**

- The analysis is on a static data set. This could be further improved by having data scraped dynamically through a web API

- User Reviews if available could be used to further understand the key aspects that increase the affinity of 
  user to a music/podcast track

- While Random Forest Classifier gives a satusfactory prediction performance, we could also look into neural networks to improve   the prediction performance

***
### *References*

[*https://www.statista.com/statistics/813876/spotify-monthly-active-users-time-spent-listening/*](https://www.statista.com/statistics/813876/spotify-monthly-active-users-time-spent-listening/)

[*https://qz.com/1736762/spotify-grows-monthly-active-users-and-turns-profit-shares-jump-15-percent/ *](https://qz.com/1736762/spotify-grows-monthly-active-users-and-turns-profit-shares-jump-15-percent/)

[*https://www.tunefab.com/spotify/spotify-bluetooth.html*](https://www.tunefab.com/spotify/spotify-bluetooth.html)

  



