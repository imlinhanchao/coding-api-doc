# 用户通知

获取用户的通知列表，可以支持分页查询。需要设置 `notification` 的 scope 授权。

Request:

```
GET /api/notification?page=1&pageSize=10&order=1
```

|Key|Description|
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
