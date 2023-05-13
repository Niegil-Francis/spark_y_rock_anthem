# spark_y_rock_anthem

## Introduction

This repository contains the final project of Big-Data CS-GY 6513 Spring 2023. The project is titled Spark-y Rock Anthem and contains the following:
1) EDA of songs, aritists and albums across all genres for the years 2020-2023.
2) Song Search using MinHashLSH to compare the user's search keywords to all the songs present in the data.
3) Lyric generator to inspire the next generation of music that combines AI with human creativity

### Contributers:
- Khalid Ansari
- Zaid Parvej Patel
- Mahasmtri Adhuri
- Prajna Ravindra Nayak
- Niegil Francis Muttath Joseph<br><br>

## File Description

***Note: None of the codes will work unless the data folder is added to the repo. The folder can be found [here](https://drive.google.com/drive/folders/102J24s4C4UbUdeNW8NzfLwEh_J611ZG8?usp=share_link). This folder contains all the data scraped/pulled from different websites.***
- [rate-your-music-scraper.ipynb](rate-your-music-scraper.ipynb) <br>
Contains code that pulls data from [rateyourmusic.com](https://rateyourmusic.com/). The album and artist of the top, bottom, popular, esoteric and diverse charts for each year ranging from 2000-2023 are pulled.
- [spotify-scraper.ipynb](spotify-scraper.ipynb) <br>
Contains code that takes the data pulled from [rateyourmusic.com](https://rateyourmusic.com/) and uses the artist and album name to get all tracks of the album and other features of the artist, album and track using the [Spotify API](https://developer.spotify.com/documentation/web-api).
- [genius-scraper.ipynb](genius-scraper.ipynb) <br>
This code iterates through the data pulled from [rateyourmusic.com](https://rateyourmusic.com/) and the [Spotify API](https://developer.spotify.com/documentation/web-api) to get the lyrics for each track. The lyrics are then appended to the data.
- [lyric-gen.ipynb](lyric-gen.ipynb) <br>
Contains code that generates lyrics using gpt-2. The user can enter either album, artist or song name to generate lyrics of the song. This code loads the model from the folder models that needs to be downloaded from [here](https://drive.google.com/drive/folders/1_Xmrl37ft80cT5gZb2MTrwLuWE1DXgnO?usp=sharing). This code uses colab-pro and if you would like to run the gpt-2-medium model you would need colab-pro+.
- [song-search.ipynb](song-search.ipynb) <br>
Contains code that searches for a song based on the lyrics. This code uses colab-pro with high ram. We have limited the search to 10 entries to make the code run quicker. This can be changed by changing the limit value while assigning raw_features within the code. The entire dataset can be included by commenting out the year condition and condition on the order while loading the data into spark.
- [vagalume-scraper](vagalume-scraper.ipynb) <br>
Contains code that scrapes lyrics of all artists and their albums from the [vagalume.br](https://www.vagalume.com.br/) website.
- [song-list-scraper](song-list-scraper.ipynb) <br>
Contains code that scrapes artist and their album names from the [song-list](https://www.song-list.net/) website.
- [Presentation-Spark-y-Rock-Anthem.pdf](Presentation-Spark-y-Rock-Anthem.pdf) <br>
Contains the final presentation as a pdf
- [Project-Report-Spark-y-Rock-Anthem.pdf](Project-Report-Spark-y-Rock-Anthem.pdf) <br>
Contains the final project report as a pdf <br><br>

## Folder Stucture

- [data](data/) <br>
 Should be downloaded manually from this [link](https://drive.google.com/drive/folders/102J24s4C4UbUdeNW8NzfLwEh_J611ZG8?usp=share_link). Contains all the data pulled from each website.
- [models](models/) <br>
Should be downloaded manually from this [link](https://drive.google.com/drive/folders/1_Xmrl37ft80cT5gZb2MTrwLuWE1DXgnO?usp=sharing). Contains all the models used for lyric generation.
- [results](results/) <br>
Folder that contains some of the results that were added into the presentation.
- [drivers](drivers/) <br>
Contains chromium.exe drivers for scraping.
- [not_used](not_used/) <br>
Contains all the codes that work but are not used. There are different scrapers in the folder.
- [not_working](not_working/) <br>
Contains the code to pull data from [a-z lyrics](https://www.azlyrics.com/). The website has blockers and is not conducive for scraping.<br><br>

## References
- The code for rate your music scraper was modified from [here](https://github.com/MichaelAlexanderBryant/rate-your-music-scraper).
- The code for the vagalume scraper was adapted from [here](https://aneisse.com/post/20190210-music-data-scraping/20190210-music-data-scraping/).