# FastText Word Embeddings for Spanish Language Variations

This repository contains word embeddings for several Spanish language variations created from Twitter data.
The data was collected from Twitter's public stream between the period Dec. 2015 to Dec. 2018 using the Twitter's API.
Each tweet in the collection is geolocalized and labeled as Spanish by Twitter (`lang="es"` in the API); it also contains at least one Spanish's _stop word_. The last condition is a consequence of the query used to capture tweets from the stream. For the interested reader, the stopword's list contains 400 common words, more precisely, articles, prepositions, interjections along other typical words.

Using this methodology, we collected close to 660 geolocalized million tweets from 185 countries.
We select 21 countries having Spanish as one of their official languages,[^1]. From the rest of the world, we select Brazil, Canada, Great Britain, France, and Uninated States of America due to the large number of collected tweets in our dataset corresponding to these countries, but also because these countries have a well known migration, business, and tourism activities of Spanish speakers. 
To ensure a minimum amount of information in each tweet of the collection, we discard those tweets with at less than five tokens; where each token correspond to some word or punctuation symbol. We also removed all retweets, since the original tweet may not be generated at the claimed country. After this filtering procedure, we retain more than 586 million tweets.

The next table describes our datasets.


| Country                  | Code | \#users  | \#tweets | \#tokens  |
|--------------------------|------|----------|----------|-----------|
| Argentina                |  AR  | 1,199.5K |  175.7M  | 2,325.0M  |
| Bolivia                  |  BO  | 28.4K    |    0.8M  |    14.1M  |
| Chile                    |  CL  | 358.0K   |   32.7M  |   543.3M  |
| Colombia                 |  CO  | 601.6K   |   44.7M  |   686.9M  |
| Costa Rica               |  CR  | 67.2K    |    5.8M  |    81.3M  |
| Cuba                     |  CU  | 24.8K    |    0.3M  |     4.1M  |
| Dominican Republic       |  DO  | 95.1K    |    5.5M  |    89.0M  |
| Ecuador                  |  EC  | 178.3K   |    9.8M  |   162.9M  |
| El Salvador              |  SV  | 37.4K    |    1.8M  |    29.5M  |
| Equatorial Guinea        |  GQ  | 0.6K     |    5.9K  |     0.1M  |
| Guatemala                |  GT  | 63.7K    |    3.8M  |    57.7M  |
| Honduras                 |  HN  | 28.4K    |    1.4M  |    21.5M  |
| Mexico                   |  MX  | 1,305.3K |   85.0M  | 1,247.3M  |
| Nicaragua                |  NI  | 29.5K    |    2.5M  |    33.7M  |
| Panama                   |  PA  | 69.2K    |    4.5M  |    75.9M  |
| Paraguay                 |  PY  | 88.9K    |    7.3M  |   105.2M  |
| Peru                     |  PE  | 232.5K   |   11.3M  |   181.0M  |
| Puerto Rico              |  PR  | 15.9K    |    0.5M  |     7.0M  |
| Spain                    |  ES  | 1,112.1K |   91.0M  | 1,496.6M  |
| Uruguay                  |  UY  | 135.4K   |   22.2M  |   276.8M  |
| Venezuela                |  VE  | 386.9K   |   29.3M  |   480.9M  |
|  -                       |  -   | -        |   -      | -         |
| Brazil                   |  BR  | 1,315.6K |    9,5M  |    85.8M  |
| Canada                   |  CA  | 122.2K   |    0.9M  |    14.5M  |
| France                   |  FR  | 244.0K   |    1.4M  |    20.4M  |
| Great Britain            |  GB  | 316.3K   |    1.7M  |    25.4M  |
| United States of America |  US  | 2,256.6K |   26.2M  |   366.1M  |

In addition to the country's population; the number of tweeters vary different due to social and economic conditions, internet access, and obviously, Twitter's permeation in that country.

....

# Download instructions

## Word Embeddings for Countries where Spanish is an official language

###  Argentina                (AR)
``` curl -o es-AR-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-AR-100d.zip" ```
###  Bolivia                  (BO)
``` curl -o es-BO-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-BO-100d.zip" ```
###  Chile                    (CL)
``` curl -o es-CL-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-CL-100d.zip" ```
###  Colombia                 (CO)
``` curl -o es-CO-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-CO-100d.zip" ```
###  Costa Rica               (CR)
``` curl -o es-CR-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-CR-100d.zip" ```
###  Cuba                     (CU)
``` curl -o es-CU-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-CU-100d.zip" ```
###  Dominican Republic       (DO)
``` curl -o es-DO-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-DO-100d.zip" ```
###  Ecuador                  (EC)
``` curl -o es-EC-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-EC-100d.zip" ```
###  El Salvador              (SV)
``` curl -o es-SV-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-SV-100d.zip" ```
###  Equatorial Guinea        (GQ)
``` curl -o es-GQ-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-GQ-100d.zip" ```
###  Guatemala                (GT)
``` curl -o es-GT-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-GT-100d.zip" ```
###  Honduras                 (HN)
``` curl -o es-HN-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-HN-100d.zip" ```
###  Mexico                   (MX)
``` curl -o es-MX-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-MX-100d.zip" ```
###  Nicaragua                (NI)
``` curl -o es-NI-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-NI-100d.zip" ```
###  Panama                   (PA)
``` curl -o es-PA-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-PA-100d.zip" ```
###  Paraguay                 (PY)
``` curl -o es-PY-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-PY-100d.zip" ```
###  Peru                     (PE)
``` curl -o es-PE-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-PE-100d.zip" ```
###  Puerto Rico              (PR)
``` curl -o es-PR-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-PR-100d.zip" ```
###  Spain                    (ES)
``` curl -o es-ES-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-ES-100d.zip" ```
###  Uruguay                  (UY)
``` curl -o es-UY-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-UY-100d.zip" ```
###  Venezuela                (VE)
``` curl -o es-VE-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-VE-100d.zip" ```

## Other countries with a significant number of tweets in Spanish
###  Brazil                   (BR)
``` curl -o es-BR-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-BR-100d.zip" ```
###  Canada                   (CA)
``` curl -o es-CA-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-CA-100d.zip" ```
###  France                   (FR)
``` curl -o es-FR-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-FR-100d.zip" ```
###  Great Britain            (GB)
``` curl -o es-GB-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-GB-100d.zip" ```
###  United States of America (US)
``` curl -o es-US-100d.zip "http://ingeotec.mx/~sadit/regional-embeddings/es-US-100d.zip" ```


[^1]: [List of countries where Spanish is an official language](https://en.wikipedia.org/wiki/List_of_countries_where_Spanish_is_an_official_language)