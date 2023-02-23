-   <a
    href="#this-repo-only-contatins-the-data-and-statistics-for-2022.for-the-data-of"
    id="toc-this-repo-only-contatins-the-data-and-statistics-for-2022.for-the-data-of">This
    repo only contatins the data and statistics for 2022.For the data
    of:</a>
    -   <a
        href="#please-visithttpsgithub.comlopezbeccovid19_tweets_dataset_2020"
        id="toc-please-visithttpsgithub.comlopezbeccovid19_tweets_dataset_2020">-
        2020 please
        visit:<span>https://github.com/lopezbec/COVID19_Tweets_Dataset_2020</span></a>
    -   <a
        href="#please-visithttpsgithub.comlopezbeccovid19_tweets_dataset_2021"
        id="toc-please-visithttpsgithub.comlopezbeccovid19_tweets_dataset_2021">-
        2021 please
        visit:<span>https://github.com/lopezbec/COVID19_Tweets_Dataset_2021</span></a>
-   <a href="#data-organization" id="toc-data-organization">Data
    Organization</a>
-   <a href="#data-statistics" id="toc-data-statistics">Data Statistics</a>
    -   <a href="#general-statistics" id="toc-general-statistics">General
        Statistics</a>
    -   <a href="#language-statistics" id="toc-language-statistics">Language
        Statistics</a>
    -   <a href="#english-sentiment-analaysis"
        id="toc-english-sentiment-analaysis">English Sentiment Analaysis</a>
    -   <a href="#english-named-entity-recognition-mentions-and-hashtags"
        id="toc-english-named-entity-recognition-mentions-and-hashtags">English
        Named Entity Recognition, Mentions, and Hashtags</a>
    -   <a href="#spanish-sentiment-analaysis"
        id="toc-spanish-sentiment-analaysis">Spanish Sentiment Analaysis</a>
    -   <a href="#spanish-named-entity-recognition"
        id="toc-spanish-named-entity-recognition">Spanish Named Entity
        Recognition</a>
    -   <a href="#data-collection-process-inconsistencies"
        id="toc-data-collection-process-inconsistencies">Data Collection Process
        Inconsistencies</a>
-   <a href="#hydrating-tweets" id="toc-hydrating-tweets">Hydrating
    Tweets</a>
    -   <a href="#using-our-twarc-notebook"
        id="toc-using-our-twarc-notebook">Using our TWARC Notebook</a>
        -   <a href="#using-hydrator" id="toc-using-hydrator">Using Hydrator</a>
        -   <a href="#using-twarc" id="toc-using-twarc">Using Twarc</a>
-   <a href="#inquiries-requests" id="toc-inquiries-requests">Inquiries
    &amp; Requests</a>
-   <a href="#licensing" id="toc-licensing">Licensing</a>
-   <a href="#references" id="toc-references">References</a>

## This repo only contatins the data and statistics for 2022.For the data of:

### - 2020 please visit:<https://github.com/lopezbec/COVID19_Tweets_Dataset_2020>

### - 2021 please visit:<https://github.com/lopezbec/COVID19_Tweets_Dataset_2021>

------------------------------------------------------------------------

The repository contains an ongoing collection of tweets associated with
the novel coronavirus COVID-19 since January 22nd, 2020.

As of 12/31/2022 there were a total of **3,001,855,651** tweets
collected. The tweets are collected using Twitter’s trending topics and
selected keywords. Moreover, the tweets from [Chen et
al. (2020)](https://github.com/echen102/COVID-19-TweetIDs) was used to
supplement the dataset by hydrating non-duplicated tweets. These tweets
are just a sample of all the tweets generated that are provided by
Twitter, and it might not represent the whole population of tweets at
any given point.

**Citation**

Lopez, C. E., Gallemore, C., “An Augmented Multilingual Twitter dataset
for studying the COVID-19 infodemic” Soc. Netw. Anal. Min. 11, 102
(2021). DOI: s13278-021-00825-0
<https://pubmed.ncbi.nlm.nih.gov/34697560/>

## Data Organization

The dataset is organized by hour (UTC) , month, and by tables. The
description of all the features in all seven tables is provided below.
For example, the path
“./Summary_Details/2020_01/2020_01_22_00_Summary_Details.csv” contains
all the summary details of the tweets collection on January 22nd at
00:00 UTC time.

<table class="table table" style="margin-left: auto; margin-right: auto; font-size: 9px; margin-left: auto; margin-right: auto;">
<caption style="font-size: initial !important;">
Features Description
</caption>
<thead>
<tr>
<th style="text-align:left;font-weight: bold;">
Table
</th>
<th style="text-align:left;font-weight: bold;">
Feature Name
</th>
<th style="text-align:left;font-weight: bold;">
Description
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
Primary key
</td>
<td style="text-align:left;">
Tweet_ID
</td>
<td style="text-align:left;">
Integer representation of the tweets unique identifier
</td>
</tr>
<tr>
<td style="text-align:left;">
1.Summary_Details
</td>
<td style="text-align:left;">
Language
</td>
<td style="text-align:left;">
When present, indicates a BCP47 language identifier corresponding to the
machine-detected language of the Tweet text
</td>
</tr>
<tr>
<td style="text-align:left;">
</td>
<td style="text-align:left;">
Geolocation_cordinate
</td>
<td style="text-align:left;">
Indicates whether or not the geographic location of the tweet was
reported
</td>
</tr>
<tr>
<td style="text-align:left;">
</td>
<td style="text-align:left;">
RT
</td>
<td style="text-align:left;">
Indicates if the tweet is a retweet (YES) or original tweet (NO)
</td>
</tr>
<tr>
<td style="text-align:left;">
</td>
<td style="text-align:left;">
Likes
</td>
<td style="text-align:left;">
Number of likes for the tweet
</td>
</tr>
<tr>
<td style="text-align:left;">
</td>
<td style="text-align:left;">
Retweets
</td>
<td style="text-align:left;">
Number of times the tweet was retweeted
</td>
</tr>
<tr>
<td style="text-align:left;">
</td>
<td style="text-align:left;">
Country
</td>
<td style="text-align:left;">
When present, indicates a list of uppercase two-letter country
codes from which the tweet comes
</td>
</tr>
<tr>
<td style="text-align:left;">
</td>
<td style="text-align:left;">
Date_Created
</td>
<td style="text-align:left;">
UTC date and time the tweet was created
</td>
</tr>
<tr>
<td style="text-align:left;">
2.Summary_Hastag
</td>
<td style="text-align:left;">
Hashtag
</td>
<td style="text-align:left;">
Hashtag (#) present in the tweet
</td>
</tr>
<tr>
<td style="text-align:left;">
3.Summary_Mentions
</td>
<td style="text-align:left;">
Mentions
</td>
<td style="text-align:left;">
Mention (@) present in the tweet
</td>
</tr>
<tr>
<td style="text-align:left;">
4.Summary_Sentiment
</td>
<td style="text-align:left;">
Sentiment_Label
</td>
<td style="text-align:left;">
Most probable tweet sentiment (neutral, positive, negative)
</td>
</tr>
<tr>
<td style="text-align:left;">
</td>
<td style="text-align:left;">
Logits_Neutral
</td>
<td style="text-align:left;">
Non-normalized prediction for neutral sentiment
</td>
</tr>
<tr>
<td style="text-align:left;">
</td>
<td style="text-align:left;">
Logits_Positive
</td>
<td style="text-align:left;">
Non-normalized prediction for positive sentiment
</td>
</tr>
<tr>
<td style="text-align:left;">
</td>
<td style="text-align:left;">
Logits_Negative
</td>
<td style="text-align:left;">
Non-normalized prediction for negative sentiment
</td>
</tr>
<tr>
<td style="text-align:left;">
5.Summary_NER
</td>
<td style="text-align:left;">
NER_text
</td>
<td style="text-align:left;">
Text stating a named entity recognized by the NER algorithm
</td>
</tr>
<tr>
<td style="text-align:left;">
</td>
<td style="text-align:left;">
Start_Pos
</td>
<td style="text-align:left;">
Initial character position within the tweet of the NER_text
</td>
</tr>
<tr>
<td style="text-align:left;">
</td>
<td style="text-align:left;">
End_Pos
</td>
<td style="text-align:left;">
End character position within the tweet of the NER_text
</td>
</tr>
<tr>
<td style="text-align:left;">
</td>
<td style="text-align:left;">
NER_Label Prob
</td>
<td style="text-align:left;">
Label and probability of the named entity recognized by the NER
algorithm
</td>
</tr>
<tr>
<td style="text-align:left;">
6.Summary_Sentiment_ES
</td>
<td style="text-align:left;">
Sentiment_Label
</td>
<td style="text-align:left;">
Most probable tweet sentiment (neutral, positive, negative)
</td>
</tr>
<tr>
<td style="text-align:left;">
</td>
<td style="text-align:left;">
Probability_pos
</td>
<td style="text-align:left;">
Probability of the tweets sentiment being positive (\<=0.33 is negative,
\>0.33 OR \<0.66 is neutral, else positve)
</td>
</tr>
<tr>
<td style="text-align:left;">
7.Summary_NER_ES
</td>
<td style="text-align:left;">
NER_text
</td>
<td style="text-align:left;">
Text stating a named entity recognized by the NER algorithm
</td>
</tr>
<tr>
<td style="text-align:left;">
</td>
<td style="text-align:left;">
Start_Pos
</td>
<td style="text-align:left;">
Initial character position within the tweet of the NER_text
</td>
</tr>
<tr>
<td style="text-align:left;">
</td>
<td style="text-align:left;">
End_Pos
</td>
<td style="text-align:left;">
End character position within the tweet of the NER_text
</td>
</tr>
<tr>
<td style="text-align:left;">
</td>
<td style="text-align:left;">
NER_Label Prob
</td>
<td style="text-align:left;">
Label and probability of the named entity recognized by the NER
algorithm
</td>
</tr>
</tbody>
</table>

For more information visit: [Twitter
API](https://developer.twitter.com/en/docs) and the [Documentation for
API
Tweet-object](https://developer.twitter.com/en/docs/twitter-api/v1/data-dictionary/overview/tweet-object)

# Data Statistics

## General Statistics

As of 12/31/2022:

Total Number of tweets: **3,001,855,651**

Average daily number of tweets: **115,932**

<table class="table table" style="margin-left: auto; margin-right: auto; font-size: 12px; margin-left: auto; margin-right: auto;">
<caption style="font-size: initial !important;">
Summary Statistics per Month
</caption>
<thead>
<tr>
<th style="text-align:right;font-weight: bold;">
Year
</th>
<th style="text-align:left;font-weight: bold;">
Month
</th>
<th style="text-align:left;font-weight: bold;">
Daily Avg. Original
</th>
<th style="text-align:left;font-weight: bold;">
Daily Avg. Retweets
</th>
<th style="text-align:left;font-weight: bold;">
Daily Avg. Tweets
</th>
<th style="text-align:left;font-weight: bold;">
Total of Orignal
</th>
<th style="text-align:left;font-weight: bold;">
Total of Retweets
</th>
<th style="text-align:left;font-weight: bold;">
Total of Tweets
</th>
<th style="text-align:left;font-weight: bold;">
Total with Geolocation
</th>
<th style="text-align:left;font-weight: bold;">
Max No. Retweets
</th>
<th style="text-align:left;font-weight: bold;">
Max No. Likes
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:right;">
2020
</td>
<td style="text-align:left;">
1
</td>
<td style="text-align:left;">
5,947
</td>
<td style="text-align:left;">
30,576
</td>
<td style="text-align:left;">
35,501
</td>
<td style="text-align:left;">
1,958,346
</td>
<td style="text-align:left;">
7,852,504
</td>
<td style="text-align:left;">
9,810,850
</td>
<td style="text-align:left;">
1,773
</td>
<td style="text-align:left;">
674,151
</td>
<td style="text-align:left;">
334,802
</td>
</tr>
<tr>
<td style="text-align:right;">
2020
</td>
<td style="text-align:left;">
2
</td>
<td style="text-align:left;">
10,978
</td>
<td style="text-align:left;">
29,918
</td>
<td style="text-align:left;">
40,604
</td>
<td style="text-align:left;">
7,624,648
</td>
<td style="text-align:left;">
21,944,443
</td>
<td style="text-align:left;">
29,568,948
</td>
<td style="text-align:left;">
8,103
</td>
<td style="text-align:left;">
469,739
</td>
<td style="text-align:left;">
637,589
</td>
</tr>
<tr>
<td style="text-align:right;">
2020
</td>
<td style="text-align:left;">
3
</td>
<td style="text-align:left;">
13,095
</td>
<td style="text-align:left;">
44,714
</td>
<td style="text-align:left;">
56,283
</td>
<td style="text-align:left;">
12,610,824
</td>
<td style="text-align:left;">
46,659,589
</td>
<td style="text-align:left;">
59,270,412
</td>
<td style="text-align:left;">
19,952
</td>
<td style="text-align:left;">
1,064,693
</td>
<td style="text-align:left;">
1,255,858
</td>
</tr>
<tr>
<td style="text-align:right;">
2020
</td>
<td style="text-align:left;">
4
</td>
<td style="text-align:left;">
30,091
</td>
<td style="text-align:left;">
89,513
</td>
<td style="text-align:left;">
119,859
</td>
<td style="text-align:left;">
20,594,379
</td>
<td style="text-align:left;">
60,311,559
</td>
<td style="text-align:left;">
80,905,936
</td>
<td style="text-align:left;">
38,220
</td>
<td style="text-align:left;">
649,823
</td>
<td style="text-align:left;">
662,005
</td>
</tr>
<tr>
<td style="text-align:right;">
2020
</td>
<td style="text-align:left;">
5
</td>
<td style="text-align:left;">
35,163
</td>
<td style="text-align:left;">
100,022
</td>
<td style="text-align:left;">
135,709
</td>
<td style="text-align:left;">
26,307,406
</td>
<td style="text-align:left;">
73,792,461
</td>
<td style="text-align:left;">
100,099,863
</td>
<td style="text-align:left;">
47,777
</td>
<td style="text-align:left;">
1,007,616
</td>
<td style="text-align:left;">
929,811
</td>
</tr>
<tr>
<td style="text-align:right;">
2020
</td>
<td style="text-align:left;">
6
</td>
<td style="text-align:left;">
51,033
</td>
<td style="text-align:left;">
142,569
</td>
<td style="text-align:left;">
193,096
</td>
<td style="text-align:left;">
34,786,076
</td>
<td style="text-align:left;">
95,171,388
</td>
<td style="text-align:left;">
129,957,461
</td>
<td style="text-align:left;">
58,138
</td>
<td style="text-align:left;">
790,652
</td>
<td style="text-align:left;">
882,693
</td>
</tr>
<tr>
<td style="text-align:right;">
2020
</td>
<td style="text-align:left;">
7
</td>
<td style="text-align:left;">
53,720
</td>
<td style="text-align:left;">
155,042
</td>
<td style="text-align:left;">
209,738
</td>
<td style="text-align:left;">
39,611,015
</td>
<td style="text-align:left;">
111,876,344
</td>
<td style="text-align:left;">
151,487,359
</td>
<td style="text-align:left;">
56,808
</td>
<td style="text-align:left;">
9,998
</td>
<td style="text-align:left;">
99,846
</td>
</tr>
<tr>
<td style="text-align:right;">
2020
</td>
<td style="text-align:left;">
8
</td>
<td style="text-align:left;">
51,330
</td>
<td style="text-align:left;">
143,551
</td>
<td style="text-align:left;">
195,142
</td>
<td style="text-align:left;">
37,596,182
</td>
<td style="text-align:left;">
103,098,588
</td>
<td style="text-align:left;">
140,694,770
</td>
<td style="text-align:left;">
55,837
</td>
<td style="text-align:left;">
2,183,434
</td>
<td style="text-align:left;">
860,162
</td>
</tr>
<tr>
<td style="text-align:right;">
2020
</td>
<td style="text-align:left;">
9
</td>
<td style="text-align:left;">
50,068
</td>
<td style="text-align:left;">
132,040
</td>
<td style="text-align:left;">
182,947
</td>
<td style="text-align:left;">
35,861,979
</td>
<td style="text-align:left;">
92,957,247
</td>
<td style="text-align:left;">
128,819,226
</td>
<td style="text-align:left;">
32,381
</td>
<td style="text-align:left;">
1,925,489
</td>
<td style="text-align:left;">
839,689
</td>
</tr>
<tr>
<td style="text-align:right;">
2020
</td>
<td style="text-align:left;">
10
</td>
<td style="text-align:left;">
54,489
</td>
<td style="text-align:left;">
137,225
</td>
<td style="text-align:left;">
198,708
</td>
<td style="text-align:left;">
41,062,885
</td>
<td style="text-align:left;">
104,195,279
</td>
<td style="text-align:left;">
144,962,625
</td>
<td style="text-align:left;">
319,101
</td>
<td style="text-align:left;">
946,810
</td>
<td style="text-align:left;">
785,385
</td>
</tr>
<tr>
<td style="text-align:right;">
2020
</td>
<td style="text-align:left;">
11
</td>
<td style="text-align:left;">
64,125
</td>
<td style="text-align:left;">
111,686
</td>
<td style="text-align:left;">
177,062
</td>
<td style="text-align:left;">
45,096,171
</td>
<td style="text-align:left;">
77,885,575
</td>
<td style="text-align:left;">
122,981,746
</td>
<td style="text-align:left;">
26,488
</td>
<td style="text-align:left;">
1,187,438
</td>
<td style="text-align:left;">
619,643
</td>
</tr>
<tr>
<td style="text-align:right;">
2020
</td>
<td style="text-align:left;">
12
</td>
<td style="text-align:left;">
64,840
</td>
<td style="text-align:left;">
121,149
</td>
<td style="text-align:left;">
186,852
</td>
<td style="text-align:left;">
49,065,436
</td>
<td style="text-align:left;">
87,366,002
</td>
<td style="text-align:left;">
133,179,589
</td>
<td style="text-align:left;">
3,277,244
</td>
<td style="text-align:left;">
1,402,911
</td>
<td style="text-align:left;">
1,038,164
</td>
</tr>
<tr>
<td style="text-align:right;">
2021
</td>
<td style="text-align:left;">
1
</td>
<td style="text-align:left;">
58,064
</td>
<td style="text-align:left;">
134,346
</td>
<td style="text-align:left;">
191,962
</td>
<td style="text-align:left;">
42,074,164
</td>
<td style="text-align:left;">
95,252,118
</td>
<td style="text-align:left;">
137,326,282
</td>
<td style="text-align:left;">
25,273
</td>
<td style="text-align:left;">
1,437,164
</td>
<td style="text-align:left;">
867,275
</td>
</tr>
<tr>
<td style="text-align:right;">
2021
</td>
<td style="text-align:left;">
2
</td>
<td style="text-align:left;">
47,789
</td>
<td style="text-align:left;">
104,467
</td>
<td style="text-align:left;">
152,780
</td>
<td style="text-align:left;">
30,916,912
</td>
<td style="text-align:left;">
65,130,838
</td>
<td style="text-align:left;">
96,047,732
</td>
<td style="text-align:left;">
23,977
</td>
<td style="text-align:left;">
971,119
</td>
<td style="text-align:left;">
644,697
</td>
</tr>
<tr>
<td style="text-align:right;">
2021
</td>
<td style="text-align:left;">
3
</td>
<td style="text-align:left;">
51,889
</td>
<td style="text-align:left;">
117,776
</td>
<td style="text-align:left;">
168,768
</td>
<td style="text-align:left;">
37,803,773
</td>
<td style="text-align:left;">
83,103,448
</td>
<td style="text-align:left;">
120,907,221
</td>
<td style="text-align:left;">
28,788
</td>
<td style="text-align:left;">
1,083,628
</td>
<td style="text-align:left;">
599,385
</td>
</tr>
<tr>
<td style="text-align:right;">
2021
</td>
<td style="text-align:left;">
4
</td>
<td style="text-align:left;">
47,350
</td>
<td style="text-align:left;">
128,902
</td>
<td style="text-align:left;">
176,534
</td>
<td style="text-align:left;">
34,252,762
</td>
<td style="text-align:left;">
90,730,535
</td>
<td style="text-align:left;">
124,983,296
</td>
<td style="text-align:left;">
24,117
</td>
<td style="text-align:left;">
1,111,306
</td>
<td style="text-align:left;">
653,537
</td>
</tr>
<tr>
<td style="text-align:right;">
2021
</td>
<td style="text-align:left;">
5
</td>
<td style="text-align:left;">
45,779
</td>
<td style="text-align:left;">
120,864
</td>
<td style="text-align:left;">
166,235
</td>
<td style="text-align:left;">
34,427,222
</td>
<td style="text-align:left;">
89,269,622
</td>
<td style="text-align:left;">
123,696,843
</td>
<td style="text-align:left;">
22,669
</td>
<td style="text-align:left;">
3,194,460
</td>
<td style="text-align:left;">
697,980
</td>
</tr>
<tr>
<td style="text-align:right;">
2021
</td>
<td style="text-align:left;">
6
</td>
<td style="text-align:left;">
37,931
</td>
<td style="text-align:left;">
84,426
</td>
<td style="text-align:left;">
122,204
</td>
<td style="text-align:left;">
28,310,536
</td>
<td style="text-align:left;">
63,462,978
</td>
<td style="text-align:left;">
91,773,014
</td>
<td style="text-align:left;">
17,693
</td>
<td style="text-align:left;">
824,584
</td>
<td style="text-align:left;">
413,875
</td>
</tr>
<tr>
<td style="text-align:right;">
2021
</td>
<td style="text-align:left;">
7
</td>
<td style="text-align:left;">
47,221
</td>
<td style="text-align:left;">
107,089
</td>
<td style="text-align:left;">
155,522
</td>
<td style="text-align:left;">
35,904,375
</td>
<td style="text-align:left;">
79,718,595
</td>
<td style="text-align:left;">
115,621,765
</td>
<td style="text-align:left;">
16,713
</td>
<td style="text-align:left;">
1,108,703
</td>
<td style="text-align:left;">
633,347
</td>
</tr>
<tr>
<td style="text-align:right;">
2021
</td>
<td style="text-align:left;">
8
</td>
<td style="text-align:left;">
47,626
</td>
<td style="text-align:left;">
109,563
</td>
<td style="text-align:left;">
157,721
</td>
<td style="text-align:left;">
35,681,168
</td>
<td style="text-align:left;">
81,535,924
</td>
<td style="text-align:left;">
117,217,091
</td>
<td style="text-align:left;">
13,943
</td>
<td style="text-align:left;">
1,271,696
</td>
<td style="text-align:left;">
732,266
</td>
</tr>
<tr>
<td style="text-align:right;">
2021
</td>
<td style="text-align:left;">
9
</td>
<td style="text-align:left;">
39,218
</td>
<td style="text-align:left;">
87,191
</td>
<td style="text-align:left;">
126,668
</td>
<td style="text-align:left;">
29,197,317
</td>
<td style="text-align:left;">
63,649,539
</td>
<td style="text-align:left;">
92,846,856
</td>
<td style="text-align:left;">
11,824
</td>
<td style="text-align:left;">
1,107,188
</td>
<td style="text-align:left;">
378,328
</td>
</tr>
<tr>
<td style="text-align:right;">
2021
</td>
<td style="text-align:left;">
10
</td>
<td style="text-align:left;">
26,441
</td>
<td style="text-align:left;">
56,615
</td>
<td style="text-align:left;">
82,723
</td>
<td style="text-align:left;">
19,589,093
</td>
<td style="text-align:left;">
41,041,351
</td>
<td style="text-align:left;">
60,630,444
</td>
<td style="text-align:left;">
9,172
</td>
<td style="text-align:left;">
785,621
</td>
<td style="text-align:left;">
611,358
</td>
</tr>
<tr>
<td style="text-align:right;">
2021
</td>
<td style="text-align:left;">
11
</td>
<td style="text-align:left;">
34,121
</td>
<td style="text-align:left;">
71,347
</td>
<td style="text-align:left;">
105,270
</td>
<td style="text-align:left;">
25,501,791
</td>
<td style="text-align:left;">
52,456,045
</td>
<td style="text-align:left;">
77,957,836
</td>
<td style="text-align:left;">
12,826
</td>
<td style="text-align:left;">
922,430
</td>
<td style="text-align:left;">
493,516
</td>
</tr>
<tr>
<td style="text-align:right;">
2021
</td>
<td style="text-align:left;">
12
</td>
<td style="text-align:left;">
51,161
</td>
<td style="text-align:left;">
112,414
</td>
<td style="text-align:left;">
161,728
</td>
<td style="text-align:left;">
38,142,486
</td>
<td style="text-align:left;">
81,079,736
</td>
<td style="text-align:left;">
116,751,096
</td>
<td style="text-align:left;">
2,500,334
</td>
<td style="text-align:left;">
2,120,230
</td>
<td style="text-align:left;">
708,690
</td>
</tr>
<tr>
<td style="text-align:right;">
2022
</td>
<td style="text-align:left;">
1
</td>
<td style="text-align:left;">
53,236
</td>
<td style="text-align:left;">
116,837
</td>
<td style="text-align:left;">
170,493
</td>
<td style="text-align:left;">
38,881,931
</td>
<td style="text-align:left;">
83,764,485
</td>
<td style="text-align:left;">
122,646,416
</td>
<td style="text-align:left;">
19,991
</td>
<td style="text-align:left;">
1,131,399
</td>
<td style="text-align:left;">
500,716
</td>
</tr>
<tr>
<td style="text-align:right;">
2022
</td>
<td style="text-align:left;">
2
</td>
<td style="text-align:left;">
32,931
</td>
<td style="text-align:left;">
66,068
</td>
<td style="text-align:left;">
98,593
</td>
<td style="text-align:left;">
23,216,374
</td>
<td style="text-align:left;">
46,385,889
</td>
<td style="text-align:left;">
69,602,263
</td>
<td style="text-align:left;">
14,346
</td>
<td style="text-align:left;">
1,386,245
</td>
<td style="text-align:left;">
1,175,841
</td>
</tr>
<tr>
<td style="text-align:right;">
2022
</td>
<td style="text-align:left;">
3
</td>
<td style="text-align:left;">
24,469
</td>
<td style="text-align:left;">
45,660
</td>
<td style="text-align:left;">
70,685
</td>
<td style="text-align:left;">
18,827,670
</td>
<td style="text-align:left;">
34,717,172
</td>
<td style="text-align:left;">
53,544,842
</td>
<td style="text-align:left;">
9,695
</td>
<td style="text-align:left;">
1,898,582
</td>
<td style="text-align:left;">
191,644
</td>
</tr>
<tr>
<td style="text-align:right;">
2022
</td>
<td style="text-align:left;">
4
</td>
<td style="text-align:left;">
20,565
</td>
<td style="text-align:left;">
40,382
</td>
<td style="text-align:left;">
60,409
</td>
<td style="text-align:left;">
15,705,817
</td>
<td style="text-align:left;">
30,888,937
</td>
<td style="text-align:left;">
46,594,754
</td>
<td style="text-align:left;">
9,121
</td>
<td style="text-align:left;">
645,485
</td>
<td style="text-align:left;">
442,909
</td>
</tr>
<tr>
<td style="text-align:right;">
2022
</td>
<td style="text-align:left;">
5
</td>
<td style="text-align:left;">
19,188
</td>
<td style="text-align:left;">
36,913
</td>
<td style="text-align:left;">
56,270
</td>
<td style="text-align:left;">
14,903,482
</td>
<td style="text-align:left;">
28,969,107
</td>
<td style="text-align:left;">
43,872,589
</td>
<td style="text-align:left;">
7,542
</td>
<td style="text-align:left;">
705,210
</td>
<td style="text-align:left;">
1,136,957
</td>
</tr>
<tr>
<td style="text-align:right;">
2022
</td>
<td style="text-align:left;">
6
</td>
<td style="text-align:left;">
17,302
</td>
<td style="text-align:left;">
32,965
</td>
<td style="text-align:left;">
50,543
</td>
<td style="text-align:left;">
12,877,249
</td>
<td style="text-align:left;">
23,906,820
</td>
<td style="text-align:left;">
36,784,069
</td>
<td style="text-align:left;">
6,260
</td>
<td style="text-align:left;">
723,960
</td>
<td style="text-align:left;">
327,944
</td>
</tr>
<tr>
<td style="text-align:right;">
2022
</td>
<td style="text-align:left;">
7
</td>
<td style="text-align:left;">
7,158
</td>
<td style="text-align:left;">
14,199
</td>
<td style="text-align:left;">
21,228
</td>
<td style="text-align:left;">
5,559,033
</td>
<td style="text-align:left;">
10,814,253
</td>
<td style="text-align:left;">
16,373,286
</td>
<td style="text-align:left;">
2,251
</td>
<td style="text-align:left;">
3,086,697
</td>
<td style="text-align:left;">
9,963
</td>
</tr>
<tr>
<td style="text-align:right;">
2022
</td>
<td style="text-align:left;">
8
</td>
<td style="text-align:left;">
6,982
</td>
<td style="text-align:left;">
13,300
</td>
<td style="text-align:left;">
20,317
</td>
<td style="text-align:left;">
5,170,130
</td>
<td style="text-align:left;">
9,884,397
</td>
<td style="text-align:left;">
15,054,527
</td>
<td style="text-align:left;">
2,283
</td>
<td style="text-align:left;">
2,657,359
</td>
<td style="text-align:left;">
6,701
</td>
</tr>
<tr>
<td style="text-align:right;">
2022
</td>
<td style="text-align:left;">
9
</td>
<td style="text-align:left;">
13,467
</td>
<td style="text-align:left;">
28,631
</td>
<td style="text-align:left;">
42,119
</td>
<td style="text-align:left;">
10,061,763
</td>
<td style="text-align:left;">
21,223,630
</td>
<td style="text-align:left;">
31,285,393
</td>
<td style="text-align:left;">
3,702
</td>
<td style="text-align:left;">
1,506,870
</td>
<td style="text-align:left;">
187,492
</td>
</tr>
<tr>
<td style="text-align:right;">
2022
</td>
<td style="text-align:left;">
10
</td>
<td style="text-align:left;">
11,966
</td>
<td style="text-align:left;">
25,720
</td>
<td style="text-align:left;">
37,289
</td>
<td style="text-align:left;">
9,105,739
</td>
<td style="text-align:left;">
19,625,222
</td>
<td style="text-align:left;">
28,730,961
</td>
<td style="text-align:left;">
2,418
</td>
<td style="text-align:left;">
2,654,137
</td>
<td style="text-align:left;">
272,724
</td>
</tr>
<tr>
<td style="text-align:right;">
2022
</td>
<td style="text-align:left;">
11
</td>
<td style="text-align:left;">
10,692
</td>
<td style="text-align:left;">
21,852
</td>
<td style="text-align:left;">
32,450
</td>
<td style="text-align:left;">
8,724,117
</td>
<td style="text-align:left;">
16,938,680
</td>
<td style="text-align:left;">
25,662,797
</td>
<td style="text-align:left;">
2,178
</td>
<td style="text-align:left;">
1,196,001
</td>
<td style="text-align:left;">
194,306
</td>
</tr>
<tr>
<td style="text-align:right;">
2022
</td>
<td style="text-align:left;">
12
</td>
<td style="text-align:left;">
4,838
</td>
<td style="text-align:left;">
8,690
</td>
<td style="text-align:left;">
13,561
</td>
<td style="text-align:left;">
1,448,238
</td>
<td style="text-align:left;">
2,757,255
</td>
<td style="text-align:left;">
4,205,493
</td>
<td style="text-align:left;">
385
</td>
<td style="text-align:left;">
671,917
</td>
<td style="text-align:left;">
15,357
</td>
</tr>
</tbody>
</table>

![](https://github.com/lopezbec/COVID19_Tweets_Dataset/blob/main/Summary_Details/Tweets%20per%20Day.png)

There is a total of 6,729,323 tweets with geolocation information, which
are shown on a map below:

![](https://github.com/lopezbec/COVID19_Tweets_Dataset/blob/main/Summary_Details/GeoTweets.png)

## Language Statistics

<table class="table table" style="margin-left: auto; margin-right: auto; font-size: 12px; margin-left: auto; margin-right: auto;">
<caption style="font-size: initial !important;">
Tweets Language Summary
</caption>
<thead>
<tr>
<th style="text-align:left;font-weight: bold;">
Languages
</th>
<th style="text-align:left;font-weight: bold;">
Total No. Tweets
</th>
<th style="text-align:right;font-weight: bold;">
Percentage of Tweets
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
English
</td>
<td style="text-align:left;">
1,950,942,733
</td>
<td style="text-align:right;">
65.12
</td>
</tr>
<tr>
<td style="text-align:left;">
Spanish; Castilian
</td>
<td style="text-align:left;">
340,863,804
</td>
<td style="text-align:right;">
11.38
</td>
</tr>
<tr>
<td style="text-align:left;">
Portuguese
</td>
<td style="text-align:left;">
120,396,199
</td>
<td style="text-align:right;">
4.02
</td>
</tr>
<tr>
<td style="text-align:left;">
French
</td>
<td style="text-align:left;">
108,450,005
</td>
<td style="text-align:right;">
3.62
</td>
</tr>
<tr>
<td style="text-align:left;">
Bahasa
</td>
<td style="text-align:left;">
81,852,108
</td>
<td style="text-align:right;">
2.73
</td>
</tr>
<tr>
<td style="text-align:left;">
Others
</td>
<td style="text-align:left;">
393,330,409
</td>
<td style="text-align:right;">
13.13
</td>
</tr>
</tbody>
</table>

![](https://github.com/lopezbec/COVID19_Tweets_Dataset/blob/main/Summary_Details/Tweets%20by%20Language%20Line%20plot.png)

## English Sentiment Analaysis

The sentiment of all the English tweets was estimated using a
state-or-the-art Twitter Sentiment algorithm
[BB_twtr](https://arxiv.org/abs/1704.06125). [(See code
here)](https://github.com/leelaylay/TweetSemEval) .

![](https://github.com/lopezbec/COVID19_Tweets_Dataset/blob/main/Summary_Sentiment/Tweets%20Sentiment.png)

![](https://github.com/lopezbec/COVID19_Tweets_Dataset/blob/main/Summary_Sentiment/Tweets%20Sentiment%20Percentage.png)

## English Named Entity Recognition, Mentions, and Hashtags

The Named Entity Recognition algorithm of
[flairNLP](https://github.com/flairNLP/flair) was used to extract topics
of conversation about PERSON, LOCATION, ORGANIZATION, and others. Below
are the top 5 NER, Mentions (@) and Hastags (#)

<table class="table table" style="margin-left: auto; margin-right: auto; font-size: 12px; margin-left: auto; margin-right: auto;">
<caption style="font-size: initial !important;">
Top 5 Mentions, Hashtags, and NER
</caption>
<thead>
<tr>
<th style="text-align:left;font-weight: bold;">
Mentions
</th>
<th style="text-align:left;font-weight: bold;">
Hashtags
</th>
<th style="text-align:left;font-weight: bold;">
NER Person
</th>
<th style="text-align:left;font-weight: bold;">
NER Location
</th>
<th style="text-align:left;font-weight: bold;">
NER Organization
</th>
<th style="text-align:left;font-weight: bold;">
NER Miscellaneous
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
@realDonaldTrump
</td>
<td style="text-align:left;">
#covid19
</td>
<td style="text-align:left;">
covid
</td>
<td style="text-align:left;">
us
</td>
<td style="text-align:left;">
cdc
</td>
<td style="text-align:left;">
covid
</td>
</tr>
<tr>
<td style="text-align:left;">
14,106,218
</td>
<td style="text-align:left;">
141,043,789
</td>
<td style="text-align:left;">
11,693,277
</td>
<td style="text-align:left;">
8,142,966
</td>
<td style="text-align:left;">
9,216,737
</td>
<td style="text-align:left;">
15,419,522
</td>
</tr>
<tr>
<td style="text-align:left;">
@realdonaldtrump
</td>
<td style="text-align:left;">
#coronavirus
</td>
<td style="text-align:left;">
biden
</td>
<td style="text-align:left;">
covid
</td>
<td style="text-align:left;">
covid
</td>
<td style="text-align:left;">
covid-19
</td>
</tr>
<tr>
<td style="text-align:left;">
7,159,966
</td>
<td style="text-align:left;">
45,238,657
</td>
<td style="text-align:left;">
6,326,792
</td>
<td style="text-align:left;">
4,735,316
</td>
<td style="text-align:left;">
8,720,711
</td>
<td style="text-align:left;">
8,559,377
</td>
</tr>
<tr>
<td style="text-align:left;">
@mippcivzla
</td>
<td style="text-align:left;">
#covid
</td>
<td style="text-align:left;">
trump
</td>
<td style="text-align:left;">
uk
</td>
<td style="text-align:left;">
omicron
</td>
<td style="text-align:left;">
americans
</td>
</tr>
<tr>
<td style="text-align:left;">
4,235,021
</td>
<td style="text-align:left;">
20,606,091
</td>
<td style="text-align:left;">
1,699,680
</td>
<td style="text-align:left;">
4,669,747
</td>
<td style="text-align:left;">
3,957,665
</td>
<td style="text-align:left;">
2,787,506
</td>
</tr>
<tr>
<td style="text-align:left;">
@joebiden
</td>
<td style="text-align:left;">
#whatshappeninginmyanmar
</td>
<td style="text-align:left;">
fauci
</td>
<td style="text-align:left;">
china
</td>
<td style="text-align:left;">
pfizer
</td>
<td style="text-align:left;">
covid19
</td>
</tr>
<tr>
<td style="text-align:left;">
3,497,929
</td>
<td style="text-align:left;">
3,552,497
</td>
<td style="text-align:left;">
1,453,920
</td>
<td style="text-align:left;">
3,138,509
</td>
<td style="text-align:left;">
3,897,905
</td>
<td style="text-align:left;">
1,727,581
</td>
</tr>
<tr>
<td style="text-align:left;">
@narendramodi
</td>
<td style="text-align:left;">
#omicron
</td>
<td style="text-align:left;">
boris johnson
</td>
<td style="text-align:left;">
florida
</td>
<td style="text-align:left;">
fda
</td>
<td style="text-align:left;">
omicron
</td>
</tr>
<tr>
<td style="text-align:left;">
3,303,595
</td>
<td style="text-align:left;">
2,965,321
</td>
<td style="text-align:left;">
1,291,299
</td>
<td style="text-align:left;">
1,994,113
</td>
<td style="text-align:left;">
1,195,600
</td>
<td style="text-align:left;">
1,544,210
</td>
</tr>
</tbody>
</table>

## Spanish Sentiment Analaysis

The sentiment of all the Spanish tweets was estimated using sentiment
analysis in spanish based on neural networks model of the the python
library [sentiment-analysis-spanish
0.0.25](https://pypi.org/project/sentiment-analysis-spanish/).

![](https://github.com/lopezbec/COVID19_Tweets_Dataset/blob/main/Summary_Sentiment_ES/Tweets%20Sentiment%20ES.png)

![](https://github.com/lopezbec/COVID19_Tweets_Dataset/blob/main/Summary_Sentiment_ES/Tweets%20Sentiment%20Percentage%20ES.png)

## Spanish Named Entity Recognition

The Spanish Named Entity Recognition algorithm of
[flairNLP](https://github.com/flairNLP/flair) was used to extract topics
of conversation about PERSON, LOCATION, ORGANIZATION, and others. Below
are the top 5 NER of all the Spanish tweets (\* some special character
in Spanish are not correctly represented in the readme file, like
character with accent mark)

<table class="table table" style="margin-left: auto; margin-right: auto; font-size: 12px; margin-left: auto; margin-right: auto;">
<caption style="font-size: initial !important;">
Top 5 Mentions, Hashtags, and NER
</caption>
<thead>
<tr>
<th style="text-align:left;font-weight: bold;">
NER Person
</th>
<th style="text-align:left;font-weight: bold;">
NER Location
</th>
<th style="text-align:left;font-weight: bold;">
NER Organization
</th>
<th style="text-align:left;font-weight: bold;">
NER Miscellaneous
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
covid
</td>
<td style="text-align:left;">
venezuela
</td>
<td style="text-align:left;">
vtvcanal8
</td>
<td style="text-align:left;">
covid-19
</td>
</tr>
<tr>
<td style="text-align:left;">
2,318,555
</td>
<td style="text-align:left;">
1,404,020
</td>
<td style="text-align:left;">
1,199,534
</td>
<td style="text-align:left;">
11,621,329
</td>
</tr>
<tr>
<td style="text-align:left;">
nicolasmaduro
</td>
<td style="text-align:left;">
méxico
</td>
<td style="text-align:left;">
gobierno ayuso
</td>
<td style="text-align:left;">
covid
</td>
</tr>
<tr>
<td style="text-align:left;">
704,953
</td>
<td style="text-align:left;">
1,332,602
</td>
<td style="text-align:left;">
1,179,893
</td>
<td style="text-align:left;">
10,097,351
</td>
</tr>
<tr>
<td style="text-align:left;">
mippcivzla
</td>
<td style="text-align:left;">
españa
</td>
<td style="text-align:left;">
mippcivzla
</td>
<td style="text-align:left;">
covid19
</td>
</tr>
<tr>
<td style="text-align:left;">
371,134
</td>
<td style="text-align:left;">
863,340
</td>
<td style="text-align:left;">
1,055,669
</td>
<td style="text-align:left;">
7,236,615
</td>
</tr>
<tr>
<td style="text-align:left;">
lopezobrador
</td>
<td style="text-align:left;">
cuba
</td>
<td style="text-align:left;">
covid
</td>
<td style="text-align:left;">
coronavirus
</td>
</tr>
<tr>
<td style="text-align:left;">
221,730
</td>
<td style="text-align:left;">
507,911
</td>
<td style="text-align:left;">
970,094
</td>
<td style="text-align:left;">
1,295,666
</td>
</tr>
<tr>
<td style="text-align:left;">
drpacomoreno1
</td>
<td style="text-align:left;">
madrid
</td>
<td style="text-align:left;">
oms
</td>
<td style="text-align:left;">
protocolo
</td>
</tr>
<tr>
<td style="text-align:left;">
132,677
</td>
<td style="text-align:left;">
231,933
</td>
<td style="text-align:left;">
355,599
</td>
<td style="text-align:left;">
954,161
</td>
</tr>
</tbody>
</table>

## Data Collection Process Inconsistencies

Only tweets in English were collected from 22 January to 31 January
2020, after this time the algorithm collected tweets in all languages.
There are also some known gaps of data shown below:

<table class="table table" style="margin-left: auto; margin-right: auto; font-size: 12px; margin-left: auto; margin-right: auto;">
<caption style="font-size: initial !important;">
Known gaps
</caption>
<thead>
<tr>
<th style="text-align:left;font-weight: bold;">
Date
</th>
<th style="text-align:left;font-weight: bold;">
Time
</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left;">
2020-08-06
</td>
<td style="text-align:left;">
07:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2020-08-08
</td>
<td style="text-align:left;">
07:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2020-08-09
</td>
<td style="text-align:left;">
07:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2020-08-14
</td>
<td style="text-align:left;">
07:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2021-05-06
</td>
<td style="text-align:left;">
16:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
00:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
01:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
02:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
03:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
04:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
05:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
06:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
07:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
08:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
09:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
11:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
12:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
14:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
15:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
16:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
17:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
18:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
19:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
21:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-13
</td>
<td style="text-align:left;">
22:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-14
</td>
<td style="text-align:left;">
00:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-14
</td>
<td style="text-align:left;">
02:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-14
</td>
<td style="text-align:left;">
04:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-14
</td>
<td style="text-align:left;">
05:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-14
</td>
<td style="text-align:left;">
09:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-14
</td>
<td style="text-align:left;">
11:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-14
</td>
<td style="text-align:left;">
12:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-14
</td>
<td style="text-align:left;">
13:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-14
</td>
<td style="text-align:left;">
15:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-14
</td>
<td style="text-align:left;">
17:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-14
</td>
<td style="text-align:left;">
18:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-14
</td>
<td style="text-align:left;">
19:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-14
</td>
<td style="text-align:left;">
23:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
00:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
01:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
02:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
04:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
05:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
06:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
07:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
08:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
09:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
11:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
12:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
13:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
18:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
19:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
20:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
21:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
22:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-15
</td>
<td style="text-align:left;">
23:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-16
</td>
<td style="text-align:left;">
01:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-16
</td>
<td style="text-align:left;">
03:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-16
</td>
<td style="text-align:left;">
04:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-16
</td>
<td style="text-align:left;">
05:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-17
</td>
<td style="text-align:left;">
15:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-18
</td>
<td style="text-align:left;">
05:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-18
</td>
<td style="text-align:left;">
22:00 UTC
</td>
</tr>
<tr>
<td style="text-align:left;">
2022-12-20
</td>
<td style="text-align:left;">
01:00 UTC
</td>
</tr>
</tbody>
</table>

# Hydrating Tweets

## Using our TWARC Notebook

The notebook
[Automatically_Hydrate_TweetsIDs_COVID190_v2.ipynb](https://github.com/lopezbec/COVID19_Tweets_Dataset/blob/main/Automatically_Hydrate_TweetsIDs_COVID19_v2.ipynb)
will allow you to automatically hydrate the tweets-ID from our
[COVID19_Tweets_dataset GitHub
repository](https://github.com/lopezbec/COVID19_Tweets_Dataset).

You can run this notebook directly on the cloud using Google Colab [(see
how to
tutorials)](https://colab.research.google.com/notebooks/welcome.ipynb#scrollTo=xitplqMNk_Hc)
and Google Drive.

In order to hydrate the tweet-IDs using
[TWARC](https://github.com/DocNow/twarc) you need to create a [Twitter
Developer Account](https://developer.twitter.com/en/apply-for-access).

The Twitter API’s rate limits pose an issue to fetch data from
tweed-IDs. So, we recommended using Hydrator to convert the list of
tweed-IDs, into a CSV file containing all data and meta-data relating to
the tweets. Hydrator also manages Twitter API Rate Limits for you.

For those who prefer a command-line interface over a GUI, we recommend
using Twarc.

### Using Hydrator

Follow the instructions on the [Hydrator github
repository](https://github.com/DocNow/hydrator).

### Using Twarc

Follow the instructions on the [Twarc github
repository](https://github.com/DocNow/twarc).

# Inquiries & Requests

If you would like to filter the tweets’ ID based on some metadata not
provided on the repo (e.g., geolocation), if you would like to run some
additional analyses on the full tweet text data (e.g., sentiment
analysis using another language model, topic modeling, etc.), or if you
have any questions about the dataset, please contact Dr. Christian Lopez
at **<lopezbec@lafayette.edu>**

Existing filters performed are located in ‘Tweets_ID_Filter_requests’
directory

# Licensing

This dataset is licensed under the Creative Commons
Attribution-NonCommercial-ShareAlike 4.0 International Public License
([CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)).
By using this dataset, you agree to abide by the stipulations in the
license, remain in compliance with Twitter’s [Terms of
Service](https://developer.twitter.com/en/developer-terms/agreement-and-policy),
and cite the following manuscript:

Christian Lopez, and Caleb Gallemore (2020) An Augmented Multilingual
Twitter Dataset for Studying the COVID-19 Infodemic. DOI:
10.21203/rs.3.rs-95721/v1
<https://www.researchsquare.com/article/rs-95721/v1>

# References

Lopez, C. E., Gallemore, C., “An Augmented Multilingual Twitter dataset
for studying the COVID-19 infodemic” Soc. Netw. Anal. Min. 11, 102
(2021). DOI: s13278-021-00825-0
<https://pubmed.ncbi.nlm.nih.gov/34697560/>

<a name="chen"></a> Emily Chen, Kristina Lerman, and Emilio Ferrara.
2020. #COVID-19: The First Public Coronavirus Twitter Dataset.
arXiv:cs.SI/2003.07372, 2020

<https://github.com/echen102/COVID-19-TweetIDs>
