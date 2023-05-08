# spark_y_rock_anthem

## Introduction

This repository contains the final project of Big-Data CS-GY 6513 Spring 2023. The project is titled Spark-y Rock Anthem and contains the following:
1) EDA of songs, aritists and albums across all genres for the years 2020-2023.
2) Song Search using MinHashLSH to compare the user's search keywords to all the songs present in the data.
3) Song classification into genres using MinHashLSH.
4) Lyric generator to inspire the next generation of AI and Human combined music

### Contributers:
- Khalid Ansari
- Zaid Parvej Patel
- Mahasmtri Adhuri
- Prajna Ravindra Nayak
- Niegil Francis Muttath Joseph<br><br>

## Code Description

***Note: None of the codes will work unless the data folder is added to the repo. The folder can be found [here](https://drive.google.com/drive/folders/102J24s4C4UbUdeNW8NzfLwEh_J611ZG8?usp=share_link). This folder contains all the data scraped/pulled from different websites.***
- [rate-your-music-scraper.ipynb](rate-your-music-scraper.ipynb) <br>
Contains code that pulls data from [rateyourmusic.com](https://rateyourmusic.com/). The album and artist of the top, bottom, popular, esoteric and diverse charts for each year ranging from 2000-2023 are pulled.
- [spotify-scraper.ipynb](spotify-scraper.ipynb) <br>
Contains code that takes the data pulled from [rateyourmusic.com](https://rateyourmusic.com/) and uses the artist and album name to get all tracks of the album and other features of the artist, album and track using the [Spotify API](https://developer.spotify.com/documentation/web-api).
- [genius-scraper.ipynb](genius-scraper.ipynb) <br>
This code iterates through the data pulled from [rateyourmusic.com](https://rateyourmusic.com/) and the [Spotify API](https://developer.spotify.com/documentation/web-api) to get the lyrics for each track. The lyrics are then appended to the data.<br><br>

## Folder Stucture

- [data](data/) <br>
 Should be downloaded manually from this [link](https://drive.google.com/drive/folders/102J24s4C4UbUdeNW8NzfLwEh_J611ZG8?usp=share_link). Contains all the data pulled from each website.
- [drivers](drivers/) <br>
Contains chromium.exe drivers for scraping.
- [not_used](not_used/) <br>
Contains all the codes that work but are not used. There are different scrapers in the folder.
- [not_working](not_working/) <br>
Contains the code to pull data from [a-z lyrics](https://www.azlyrics.com/). The website has blockers and is not conducive for scraping.<br><br>

## References
- The code for rate your music scraper was modified from [here](https://github.com/MichaelAlexanderBryant/rate-your-music-scraper).
- The code for the vagalume scraper was adapted from [here](https://aneisse.com/post/20190210-music-data-scraping/20190210-music-data-scraping/).