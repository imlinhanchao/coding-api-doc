# 项目动态
获取项目活动记录，需要设置 `project` 的 scope 授权。

Request:
```
GET /api/project/:project_id/activities?last_id=999999999&type=all&user_filter=0
```

|键|说明|
|--|--|
|project_id|项目 Id|
|last_id|最后一比活动记录 Id，可用于做滚动下拉显示|
|type|动态类型，可选值有 iteration=迭代，epic=史诗，requirement=需求，mission=任务，defect=缺陷，code=代码，ci=持续集成，artifact=制品库，wiki=Wiki，file=文件，Other=设置|
|user_filter|用户 Id，过滤特定用户的活动记录|

Response:
```json
{
    "code": 0,
    "data": [
        // 根据不同动态，返回内容各不相同，以后再写
    ]
}
```