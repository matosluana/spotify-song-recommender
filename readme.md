![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Project: Song Recommender

### Goals

- Practice data extraction through web scrapping and APIs
- Create a MVP for a song recommender based on the business case described below

### Business goal: Gnod case study

#### Scenario

You have been hired as a Data Analyst for "Gnod".

"Gnod" is a site that provides recommendations for music, art, literature and products based on collaborative filtering algorithms. Their flagship product is the _music recommender_, which you can try at [www.gnoosic.com](www.gnoosic.com). The site asks users to input 3 bands they like, and computes similarity scores with the rest of the users. Then, they recommend to the user bands that users with similar tastes have picked.

"Gnod" is a small company, and its only revenue stream so far are adds in the site. In the future, they would like to explore partnership options with music apps (such as _Deezer_, _Soundcloud_ or even _Apple Music_ and _Spotify_). However, for that to be possible, they need to expand and improve their recommendations.

That's precisely where you come. They have hired you as a Data Analyst, and they expect you to bring a mix of technical expertise and business mindset to the table.

Jane, CTO of Gnod, has sent you an email assigning you with your first task.

#### Task(s)

> This is an e-mail Jane - CTO of Gnod - sent over your inbox in the first weeks working there.

_Dear xxxxxxxx,
We are thrilled to welcome you as a Data Analyst for *Gnoosic*!_

_As you know, we are trying to come up with ways to enhance our music recommendations. One of the new features we'd like to research is to recommend songs (not only bands). We're also aware of the limitations of our collaborative filtering algorithms, and would like to give users two new possibilities when searching for recommendations:_

- _Songs that are actually similar to the ones they picked from an acoustic point of view._
- _Songs that are popular around the world right now, independently from their tastes._

_Coming up with the perfect song recommender will take us months - no need to stress out too much. In this first week, we want you to explore new data sources for songs. The Internet is full of information and our first step is to acquire it do an initial exploration. Feel free to use APIs or directly scrape the web to collect as much information as possible from popular songs. Eventually, we'll need to collect data from millions of songs, but we can start with a few hundreds or thousands from each source and see if the collected features are useful._

_Once the data is collected, we want you to create clusters of songs that are similar to each other. The idea is that if a user inputs a song from one group, we'll prioritize giving them recommendations of songs from that same group._

_On Friday, you will present your work to me and Marek, the CEO and founder. Full disclosure: I need you to be very convincing about this whole song-recommender, as this has been my personal push and the main reason we hired you for!_

_Be open minded about this process: we are agile, and that means that we define our products and features on-the-go, while exploring the tools and the data that's available to us. We'd love you to provide your own vision of the product and the next steps to be taken._

_Lots of luck and strength for this first week with us!_

_-Jane_


### Content

#### Notebooks

**01_Getting hot songs and scraping first songs:**
In this notebook, I scraped multiple pages to get the 100 hot songs of the week and to get the most popular songs from the past 50 years.
A first version of the song recommender was developed. This is capable of making a recommendation only if the song entered by the user is in the hot 100 songs. As per requirement, if this is the case another song from the hot 100 will be suggested.
Finally, I have used the Spotify API to get audio features from the most popular songs of the last 50 years. These will be used later to build up the recommender.

**02_Scraping Playlists from Spotify:**
To expand the selection of songs that will be part of the recommender, I have used the Spotify API to collect several playlists and tracks and their respective audio features.

**03_Clustering**
The songs collected in steps 01 and 02 are put together and clustered usig KMeans.
As outcome, now I have:
A model to be used in the song recommender
A dataset with thousands of songs which have been clustered based on their audio features

**04_Song_recommender (MVP)**
This is the main file. There are a few lines that update the list of hot songs, so that the recommender is always working with the latest top songs. Then, one can run the song recommender and it will:
- Ask for confirmation that it got the right song based on the entry
- Suggest a song based either on the hot 100 or on the clustered songs. A direct link to spotify is provided.


#### CSV Files

CSV files of the scraped songs


### Technlogies used

Python
Web Scraping
Spotify API










