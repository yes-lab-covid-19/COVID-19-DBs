# COVID-19-DBs

## Datasets

|Name |           Summary           |                       Dataset                       |          Num. Rows and Columns         |
|:---:|:---------------------------:|:---------------------------------------------------:|:--------------------------------------:|
| DB1 |    Disease Related Data     |        *confirmed_case.xlsx*<br>*death.xlsx*        |          <1531, 28><br><229, 28>       |
| DB2 |Demographic and Mobility data|                 *demographics.xlsx*                 |               <28889, 7>               |
| DB3 |         Reddit Data         |*post.csv*<br>*comment.csv*<br>*comment_location.csv*|<22992, 11><br><182554, 8><br><29165, 3>|
| DB4 |      Constructed Graph      |                     *AHIN.csv*                      |                <96459, 3>              |

## Detailed Descriptions of Datasets

|Name |                 Dataset                |
|:---:|:---------------------------------------|
| DB1 |According to simplemaps, the U.S. includes 50 states, Washington, D.C. and Puerto Rico as well as 3,203 counties and 28,889 cities. We have collected the up-to-date countybased coronavirus related data including the numbers of confirmed cases, new cases, deaths and the fatality rate, from official public health organizations and digital media with real-time updates of COVID-19. By the date, we have collected these data from 1,531 counties and 52 states (including Washington, D.C. and Puerto Rico) on a daily basis from Feb. 28, 2020 to date (i.e., March 25, 2020).|
| DB2 |We parse the demographic data collected from the the United States Census Bureau in a hierarchical manner: for each city, county or state in the U.S., the dataset includes its estimated population, population density (e.g., number of people per square mile), age and gender distributions. By the date, we make the demographic and mobility dataset available for public use including the information of estimated population, population density, and GPS coordinates for 28,889 cities, 3,203 counties and 52 states (including Washington, D.C. and Puerto Rico).|
| DB3 |In this work, we initialize our efforts on social media data with the focus of public perception analysis on Reddit, as it provides the platform for scientific discussion of dynamic policies, announcements, symptoms and events of COVID-19. In particular, we have collected and analyzed 48 statebased subreddits (i.e., Washington, D.C. and 47 states). By the date, we have crawled and automatically analyze 22,992 posts by 8,948 users on Reddit associated with 182,554 comments by 30,147 users on the discussion of COVID-19 from February 17, 2020 to date (i.e., March 25, 2020). Along with these data, this publicized dataset also includes the extracted locations of the posts using Stanford Named Entity Recognizer.|
| DB4 |Based on the designed network schema in our paper (see below in references), the constructed graph has 32,145 nodes (i.e., 1 node with type of nation, 52 nodes with type of state, 3,203 nodes with type of county, 28,889 nodes with type of city) and 96,459 edges.|


## Column Details

- *confirmed_case.xlsx*, *death.xlsx*

```
["county", "2020/2/28",...,"2020/3/25"]
```


- *demographics.xlsx*

```
["city", "county_name", "state_name", "lat", "lng", "population", "density"]
```


- *post.csv*

```
["id", "title", "author", "content", "post_type", "created_time", "num_of_comments", "attachment", "post_url", "subreddit", "state"]
```

- *comment.csv*

```
["comment_id", "post_id", "author", "content", "created_time", "comment_url", "subreddit", "state"]
```

- *comment_location.csv*

```
["content", "comment_url", "location"]
```

- *AHIN.xlsx*

```
["entity", "entity", "relation (0: include, 1: near)"]
```


## Reference

If you use our dataset(s), please cite our paper:

```
@article{Ye2020_Covid-19_Satellite,
  title={α-Satellite: An AI-driven System and Benchmark Datasets for Hierarchical Community-level Risk Assessment to Help Combat COVID-19},
  author={Ye, Yanfang and Hou, Shifu and Fan, Yujie and Qian, Yiyue and Zhang, Yiming and Sun, Shiyu and Peng, Qian and Laparo, Kenneth},
  journal={arXiv preprint arXiv:2003.12232},
  year={2020} 
} 
```
