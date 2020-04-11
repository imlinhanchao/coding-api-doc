# 用户通知

获取用户的通知列表，可以支持分页查询。需要设置 `notification` 的 scope 授权。

Request:

```
GET /api/notification?page=1&pageSize=10&order=1
```

|键|说明|
|--|--|
|page|第几页|
|pageSize|每页个数|
|order|应该是排序条件，但实际测试设置其他值没有差异|

Response:

```json
{
    "code": 0,
    "data": {
        "list": [
            {
                "reminded": false,
                "owner_id": "2492081",
                "target_type": "Project",
                "created_at": 1585551005000,
                "project": {
                    // 项目的详细信息，仅当 target_type 为 Project 时
                },
                "target_id": "8888888",
                "id": "99999999",
                "type": "4",
                "content": "内容",
                "status": "1"
            }
    }
}
```

|键|说明|
|--|--|
|reminded|是否提醒(目前没有发现为 true 的消息触发方式)|
|owner_id|消息所有者 Id|
|target_type|消息目标类型|
|created_at|创建时间|
|project|项目信息，若 target_type 为 `project` 时存在此字段|
|target_id|消息目标 ID。若是项目，则为项目 ID|
|id|消息 ID|
|type|消息类型，目前发现项目相关为 4， 公告更新为 0，更多待补充|
|content|消息内容|
|status|消息状态，0: 未读，1: 已读|