# Geosearch using Twitter API

This project uses Twitter API to collect Geo-tagged text chuncks from Twitter and visualized them as dots on the map. I'm focusing on two main locations to explore how location or language might contribute to form different patterns. For the first half of the project I'm going to collect tweets from the US and for the later part, I'm focusing on tweets from Korea and Japan.

## Maps

```python
# geosearch.ipynb

# Coordinate points for US territories
LOCATIONS = [-124.7771694, 24.520833, -66.947028, 49.384472,  # Contiguous US
             -164.639405, 58.806859, -144.152365, 71.76871,  # Alaska
             -160.161542, 18.776344, -154.641396, 22.878623]  # Hawaii

# Define boundaries for South Korea and Japan
LOCATIONS_KR_JP = [124.961954, 32.942967, 129.473591, 38.710363, # KR
                 130.029922, 31.018095, 146.996222, 45.997520] # JP
```

Here is how you would declare an array for bounding boxes. The first two coordinates are longitude and latitude for the southwest corner and the last two are for the northeast corner of the box.

![tweet-us](/assets/image/tweet-us.png)
![tweet-kr-jp](/assets/image/tweet-kr-jp.png)

These are the two different results from the different locations. It seems like the number of Geo-tagged tweets from the US is larger than that of from South Korea and Japan. One interesting pattern from the KR-JP map is that the number of Geo-tagged tweets collected in areas near the capital cities, Seoul and Tokyo, is larger compared to the other cities in the country. This pattern was not noticeable from the US version.

## Word Cloud

![us-words](/assets/image/us-words.png)

Here is a word cloud image that allows us to spot the high-frequency terms from the US based tweets. I see some common words in English including job, out, love, time, etc.

However, it was not possible to render for KR-JP based tweets because the website does not support fonts for CJK characters.

![kr-jp-words](/assets/image/kr-jp-words.png)

---

<sub>Please note that you need your own Twitter API keys to run the code. The secret keys I used for this project was removed before publishing it.</sub>
