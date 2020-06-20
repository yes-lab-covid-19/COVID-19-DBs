# COVID-19-DBs

## Datasets

|Name |           Summary           |               Dataset             |   Num. Rows and Columns  |
|:---:|:---------------------------:|:---------------------------------:|:------------------------:|
| DB1 |    Disease Related Data     |*confirmed_case.csv*<br>*death.csv*| <3208, 113><br><3208, 113> |
| DB2 |Demographic and Mobility Data|         *demographics.xlsx*       |        <28889, 7>        |
| DB3 |         Reddit Data         |    *post.csv*<br>*comment.csv*    |<58294, 12><br><561080, 9>|
| DB4 |      Constructed Graph      |            *graph.csv*            |         <103243, 3>       |

## Detailed Descriptions of Datasets

|Name |                 Description                |
|:---:|--------------------------------------------|
| DB1 |Disease Related Data: We have collected the up-to-date county-based coronavirus related data (i.e., the number of confirmed cases and deaths) from official public health organizations and digital media with real-time updates of COVID-19. By the date, we have collected these data for *3,208* counties from *52* states (including Washington, D.C. and Puerto Rico) on a daily basis from February 28, 2020 to date (i.e., June 18, 2020).|
| DB2 |Demographic and Mobility Data: We parse the demographic data collected from the United States Census Bureau in a hierarchical manner: for each city, county or state in the U.S., the dataset includes its estimated population, population density (e.g., number of people per square mile), age and gender distributions. By the date, we have made the demographic and mobility dataset available for public use, including the information of estimated population, population density, and GPS coordinates for *28,889* cities, *3,208* counties and *52* states (including Washington, D.C. and Puerto Rico).|
| DB3 |Reddit Data: We initialize our efforts on social media data with the focus of public perception analysis on Reddit, as it provides the platform for scientific discussion of dynamic policies, announcements, symptoms and events of COVID-19. We have collected and analyzed the data from 48 state-based subreddits (i.e., Washington, D.C. and 47 states). By the date, we have crawled and automatically analyzed *58,294* posts by *16,939* users on Reddit associated with *561,080* comments by *62,194* users on the discussion of COVID-19 from February 17, 2020 to date (i.e., June 03, 2020). Along with these data, this publicized dataset also includes the sentiment (0: negative, 1: positive) of each post and comment.|
| DB4 |Constructed Graph: Based on the designed network schema in our paper (see below reference), the constructed graph has *34,401* nodes (i.e., 1 node with type of nation, 52 nodes with type of state, 3,208 nodes with type of county, 31,140 nodes with type of city) and *103,243* edges.|


## Column Details

- *confirmed_case.csv*, *death.csv*

```
["county name", "2/28/2020",...,"6/18/2020"]
```


- *demographics.xlsx*

```
["city", "county_name", "state_name", "lat", "lng", "population", "density"]
```


- *post.csv*

```
["id", "title", "author", "content", "post_type", "created_time", "num_of_comments", "attachment", "post_url", "subreddit", "state", "sentiment (0: negative, 1: positive)"]
```

- *comment.csv*

```
["comment_id", "post_id", "author", "content", "created_time", "comment_url", "subreddit", "state", "sentiment (0: negative, 1: positive)"]
```


- *graph.csv*

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
