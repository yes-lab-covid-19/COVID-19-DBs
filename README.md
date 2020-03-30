# COVID-19-DBs

## Database

|Name |        Description        |                       Dataset                       |          Num. Rows and Columns         |
|:---:|:-------------------------:|:---------------------------------------------------:|:--------------------------------------:|
| DB1 |   Disease Related Data    |        *confirmed_case.xlsx*<br>*death.xlsx*        |          <1531, 28><br><229, 28>       |
| DB2 |Demographic and Mobility data|                 *demographics.xlsx*                 |               <28889, 7>               |
| DB3 |        Reddit Data        |*post.csv*<br>*comment.csv*<br>*comment_location.csv*|<22992, 11><br><182554, 8><br><29165, 3>|
| DB4 |     Constructed AHIN      |                     *AHIN.csv*                      |                <96459, 3>              |

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


## References

If you use our dataset(s), please cite our paper:

```
@article{Ye2020_Covid-19_Satellite,
  title={α-Satellite: An AI-driven System and Benchmark Datasets for Hierarchical Community-level Risk Assessment to Help Combat COVID-19},
  author={Ye, Yanfang and Hou, Shifu and Fan, Yujie and Qian, Yiyue and Zhang, Yiming and Sun, Shiyu and Peng, Qian and Laparo, Kenneth},
  journal={arXiv preprint arXiv:2003.12232},
  year={2020} 
} 
```
