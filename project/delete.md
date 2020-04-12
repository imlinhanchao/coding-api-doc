# 删除项目

删除指定项目，这需要 `all` 的 scope 授权，但个人令牌没有这样的设置项。所以只能通过应用来做了。（个人认为这是一个产品 Bug)

Request:
```
POST /api/team/:team_name/project/:project_id/delete
```

|键值|说明|
|--|--|
|team_name|团队域名|
|project_id|项目 Id|

Response:
```json
{
    "code": 0
}
```
