# COVID-19-DBs

## Database

|Name |     Description    |                       Dataset                       |           Rows           |
|:---:|:------------------:|:---------------------------------------------------:|:------------------------:|
| DB1 |disease related data|       *confirmed_case.xlsx*, *death.xlsx*         |        1531, 229       |
| DB2 |  demographic data  |                 *demographics.xlsx*                 |           28889          |
| DB3 |  social media data |*post.csv*, *comment.csv*, *comment_location*.csv| 22992,182554,29165 |
| DB4 |  constructed AHIN  |                    *AHIN.csv*                       |           96459          |

### DB1

- *confirmed_case.xlsx*, *death.xlsx*

```
["county", "date: 02.28-03.24"]
```

### DB2

- *demographics.xlsx*

```
["county_name", "state_name", "lat", "lng", "population", "density"]
```

### DB3

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


### DB4

- *AHIN.xlsx*

```
["entity", "entity", "relation"]
```

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
