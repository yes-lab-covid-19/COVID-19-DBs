# COVID-19-DBs

## Datasets

|Name |           Summary           |                       Dataset                       |          Num. Rows and Columns         |
|:---:|:---------------------------:|:---------------------------------------------------:|:--------------------------------------:|
| DB1 |    Disease Related Data     |        *confirmed_case.xlsx*<br>*death.xlsx*        |          <2724, 44><br><1021, 44>       |
| DB2 |Demographic and Mobility Data|                 *demographics.xlsx*                 |               <28889, 7>               |
| DB3 |         Reddit Data         |*post.csv*<br>*comment.csv*<br>*comment_location.csv*|<22992, 11><br><182554, 8><br><29165, 3>|
| DB4 |      Constructed Graph      |                     *graph.csv*                      |                <96459, 3>              |

## Detailed Descriptions of Datasets

|Name |                 Description                |
|:---:|--------------------------------------------|
| DB1 |Disease Related Data: We have collected the up-to-date county-based coronavirus related data (i.e., the number of confirmed cases and deaths) from official public health organizations and digital media with real-time updates of COVID-19. By the date, we have collected these data for *2,724* areas including *2,686* counties from *52* states (including Washington, D.C. and Puerto Rico), *2* correctional institution and *36* unassigned areas on a daily basis from February 28, 2020 to date (i.e., April 10, 2020).|
| DB2 |Demographic and Mobility Data: We parse the demographic data collected from the United States Census Bureau in a hierarchical manner: for each city, county or state in the U.S., the dataset includes its estimated population, population density (e.g., number of people per square mile), age and gender distributions. By the date, we have made the demographic and mobility dataset available for public use, including the information of estimated population, population density, and GPS coordinates for *28,889* cities, *3,203* counties and *52* states (including Washington, D.C. and Puerto Rico).|
| DB3 |Reddit Data: We initialize our efforts on social media data with the focus of public perception analysis on Reddit, as it provides the platform for scientific discussion of dynamic policies, announcements, symptoms and events of COVID-19. We have collected and analyzed the data from 48 state-based subreddits (i.e., Washington, D.C. and 47 states). By the date, we have crawled and automatically analyzed *22,992* posts by *8,948* users on Reddit associated with *182,554* comments by *30,147* users on the discussion of COVID-19 from February 17, 2020 to date (i.e., March 25, 2020). Along with these data, this publicized dataset also includes the extracted locations of the posts using Stanford Named Entity Recognizer.|
| DB4 |Constructed Graph: Based on the designed network schema in our paper (see below reference), the constructed graph has *32,145* nodes (i.e., 1 node with type of nation, 52 nodes with type of state, 3,203 nodes with type of county, 28,889 nodes with type of city) and *96,459* edges.|


## Column Details

- *confirmed_case.xlsx*, *death.xlsx*

```
["county", "2/28/2020",...,"4/10/2020"]
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
