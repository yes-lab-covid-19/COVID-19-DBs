# COVID-19-DBs

## Database

|Name |        Description        |                       Dataset                       |          Num. Rows and Columns         |
|:---:|:-------------------------:|:---------------------------------------------------:|:--------------------------------------:|
| DB1 |   disease related data    |        *confirmed_case.xlsx*<br>*death.xlsx*        |          <1531, 27><br><229, 27>       |
| DB2 |demographic & mobility data|                 *demographics.xlsx*                 |               <28889, 6>               |
| DB3 |        Reddit data        |*post.csv*<br>*comment.csv*<br>*comment_location*.csv|<22992, 11><br><182554, 8><br><29165, 3>|
| DB4 |     constructed AHIN      |                     *AHIN.csv*                      |                <96459, 3>              |

## Column Details

- *confirmed_case.xlsx*, *death.xlsx*

```
["county", "02.28",...,"03.24"]
```


- *demographics.xlsx*

```
["county_name", "state_name", "lat", "lng", "population", "density"]
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
