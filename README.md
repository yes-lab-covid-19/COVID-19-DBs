# COVID-19-DBs

## Database

|          Name         |                     Dataset                     |           Rows           |    Columns   |
|:---------------------:|:-----------------------------------------------:|:------------------------:|:------------:|
| DB1: Disease data     |       confirmed_case.xlsx<br>death.xlsx         |        1531<br>229       | ```["county", "date: 02.28-03.24"]```<br>```["county", "date: 02.28-03.24"]``` |
| DB2: Demographic data |                demographics.xlsx                |           28889          | ```["county_name", "state_name", "lat", "lng", "population", "density"]```  |
| DB3: Reddit data      | post.csv<br>comment.csv<br>comment_location.csv | 22992<br>182554<br>29165 | ```["id", "title", "author", "content", "post_type", "created_time", "num_of_comments", "attachment", "post_url", "subreddit", "state"]```<br>```["comment_id", "post_id", "author", "content", "created_time", "comment_url", "subreddit", "state"]``` <br>```["content", "comment_url", "location"]``` |
| DB4: AHIN             |                     AHIN.csv                    |           96459          | ```["entity", "entity", "relation"]```  |

## References

If you use our dataset or code, please cite our paper:

```
@article{ye2020satellite,
  title={α-Satellite: An AI-driven System and Benchmark Datasets for Hierarchical Community-level Risk Assessment to Help Combat COVID-19},
  author={Ye, Yanfang and Hou, Shifu and Fan, Yujie and Qian, Yiyue and Zhang, Yiming and Sun, Shiyu and Peng, Qian and Laparo, Kenneth},
  journal={arXiv preprint arXiv:xxxx.xxxxx},
  year={2020}
}
```
