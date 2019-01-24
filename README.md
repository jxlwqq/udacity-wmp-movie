# Udacity 微信小程序纳米学位实战项目2————看看侃侃电影影评小程序

## Schema 设计

### movie table

| field        | type  | comment             |
| ----------- | ----------- | ----------- |
| id          | int(11)      | 电影id，自增主键 |
| title       | varchar(255) | 电影名称          |
| image       | varchar(255) | 电影图片 url      |
| category    | varchar(255) | 电影分类         |
| description | text         | 电影简介        |
| create_time | datetime     | 创建时间     |




### movie_comment table

| field        | type  | comment             |
| ----------- | ----------- | ----------- |
| id           | int(11) | 影评id，自增主键  |
| movie_id     | int(11) | 电影id            |
| comment_type | int(1) | 影评类型 | 0:文字；1语音 |
| rating       | decimal(3,1) | 打分，最高5分     |
| user      | varchar(255) | 影评人微信open_id |
| username | varchar(255) | 影评人昵称      |
| avatar | varchar(255) | 影评人头像url   |
| content | varchar(1024) | 影评内容  |
| create_time | datetime | 创建时间  |

### comment_like table

| field        | type  | comment             |
| ----------- | ----------- | ----------- |
| id          | int(11)      | 自增主键          |
| comment_id  | int(11)      | 影评id            |
| movie_id    | int(11)      | 电影id            |
| open_id     | varchar(255) | open_id |
| create_time | datetime     | 创建时间          |



### comment_fave table

| field        | type  | comment             |
| ----------- | ----------- | ----------- |
| id          | int(11)      | 自增主键          |
| comment_id  | int(11)      | 影评id            |
| movie_id    | int(11)      | 电影id            |
| open_id     | varchar(255) | open_id |
| create_time | datetime     | 创建时间          |


