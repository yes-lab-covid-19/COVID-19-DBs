# COVID-19-DBs

## Database

|          Name         |                     Dataset                     |           Rows           |    Columns   |
|:---------------------:|:-----------------------------------------------:|:------------------------:|:------------:|
| DB1: Disease data     |       confirmed_case.xlsx<br>death.xlsx         |        1531<br>229       | `["county", "date: 02.28-03.24"]`<br>`["county", "date: 02.28-03.24"]` |
| DB2: Demographic data |                demographics.xlsx                |           28889          | `["county_name", "state_name", "lat", "lng", "population", "density"]`  |
| DB3: Reddit data      | post.csv<br>comment.csv<br>comment_location.csv | 22992<br>182554<br>29165 | `["id", "title", "author", "content", "post_type", "created_time", "num_of_comments", "attachment", "post_url", "subreddit", "state"]`<br>`["comment_id", "post_id", "author", "content", "created_time", "comment_url", "subreddit", "state"]` <br>`["content", "comment_url", "location"]` |
| DB4: AHIN             |                     AHIN.csv                    |           96459          | `["entity", "entity", "relation"]`  |

## References

If you use our dataset or code, please cite [our paper](https://arxiv.org/abs/1711.07846):

```
@inproceedings{fmow2018,
  title={Functional Map of the World},
  author={Christie, Gordon and Fendley, Neil and Wilson, James and Mukherjee, Ryan},
  booktitle={CVPR},
  year={2018}
}
```
