# 用户信息

获取当前用户，这是当前 token 的授权用户。你需要设置 `user` 的 scope。

Request:

```
GET /api/account/current_user
```

我们也可以获取团队成员的个人信息，但是很神奇的是，这个你不需要开启任何权限。你只需要知道他们的 `username` ，需要注意的是，团队内的用户名是随机生成的。唯一可以获取团队成员用户名的接口，是[获取项目成员](../project/member.md)。

Request:

```
GET /api/account/key/:username
```

这两个接口 Response 的内容都是一样的。

Response:

```json
{
    "code": 0,
    "data": {
        "tags_str": "XX, XXX, XXXX",
        "tags": "1,3,4",
        "job_str": "开发",
        "job": 1,
        "sex": 0,
        "location": "XXXXXX",
        "company": "XXXXXX",
        "slogan": "XXXXXXXXXXX",
        "website": "",
        "introduction": "",
        "avatar": "https://dn-coding-net-production-static.codehub.cn/cc500da5-4b86-4cd2-8d6c-9d375a7ffcd8.jpg?imageMogr2/auto-orient/format/jpeg/crop/!458x458a0a0",
        "gravatar": "",
        "lavatar": "https://dn-coding-net-production-static.codehub.cn/cc500da5-4b86-4cd2-8d6c-9d375a7ffcd8.jpg?imageMogr2/auto-orient/format/jpeg/crop/!458x458a0a0",
        "created_at": 1412260520000,
        "last_logined_at": 1586365724000,
        "last_activity_at": 1586436154484,
        "global_key": "UserName",
        "name": "昵称",
        "name_pinyin": "|nc|nichen",
        "updated_at": 1586365726000,
        "path": "/u/UserName",
        "status": 1,
        "is_member": 0,
        "id": 999999,
        "team": "team_name",
        "follows_count": 0,
        "fans_count": 0,
        "tweets_count": 0,
        "followed": false,
        "follow": false,
        "email_validation": 1,
        "regist_channel_id": 0,
        "account_type": 3
    }
}
```

|键值|说明|
|--|--|
|tags_str|用户标签列表，逗号分隔|
|tags|标签 ID 列表|
|job_str|工作|
|job|工作 ID|
|sex|性别，0 = 男，1 = 女，2 = 未知|
|location|地区|
|company|部门|
|slogan|座右铭|
|website|#Unknown|
|introduction|#Unknown|
|avatar|头像|
|gravatar|#Unknown|
|lavatar|头像|
|created_at|加入时间|
|last_logined_at|最后登录时间|
|last_activity_at|最后活动时间|
|global_key|团队内唯一用户 ID|
|name|姓名，昵称|
|name_pinyin|姓名配音|
|updated_at|最后更新时间|
|path|个人首页地址|
|status|#Unknown|
|is_member|#Unknown|
|id|用户 ID|
|team|团队域名|
|email_validation|邮箱是否验证|
|account_type|#Unknown|

另外，还有一个专门只获取用户邮箱的 API，你需要设置 `user:email` 的 scope 授权。

Request:

```
GET /api/account/email
```

Response:

```json
{
    "code": 0,
    "data": "email@example.com"
}
```