# 用户活跃度

获取指定用户 `username` 的用户活跃度。不需要任何授权。
Request:
```
GET /api/user/activeness/data/:username
```

Response:
```json
{
    "code": 0,
    "data": {
        "daily_activeness": [
            {
                "date": "2020-04-07",
                "count": 1
            }
        ],
        "total": 76,
        "start_date": "2019.04.11",
        "end_date": "2020.04.11",
        "longest_active_duration": {
            "days": 7,
            "start_date": "2020.03.08",
            "end_date": "2020.03.14"
        },
        "current_active_duration": {
            "days": 0
        },
        "last_activity_at": 1586589956490,
        "total_with_seal_top_line": 76
    }
}
```

|键值|说明|
|--|--|
|daily_activeness|活跃度数据|
|- date|日期|
|- count|活跃计数|
|total|总活跃度|
|start_date|统计起始日|
|end_date|统计结束日|
|longest_active_duration|最长连续活跃天数|
|- days|天数|
|- start_date|起始日（若天数大于0）|
|- end_date|结束日（若天数大于0）|
|current_active_duration|当前连续活跃天数|
|- days|天数|
|- start_date|起始日（若天数大于0）|
|- end_date|结束日（若天数大于0）|
|last_activity_at|最后活跃时间|
|total_with_seal_top_line|#Unknown|