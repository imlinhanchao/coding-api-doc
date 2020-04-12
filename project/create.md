# 创建项目

创建一个新的项目，这需要 `all` 的 scope 授权，但个人令牌没有这样的设置项。所以只能通过应用来做了。（个人认为这是一个产品 Bug)

Request:
```
POST /api/team/:team_name/project

name=code&
displayName=code&
description=test&
vcsType=git&
createSvnLayout=no&
gitEnabled=true&
gitReadmeEnabled=true&
gitLicense=no&
gitIgnore=no&
shared=1&
type=2
```

|键值|说明|
|--|--|
|team_name|团队域名|
|name|项目名|
|displayName|项目显示名|
|description|描述|
|vscType|代码托管方式|
|createSvnLayout|是否创建 SVN 仓库推荐布局，yes=创建，no=不创建|
|gitEnabled|是否启用 Git 初始化，true=启用，false=不启用|
|gitReadmeEnabled|是否添加 Readme，若为 true，gitEnabled 必须为 true 才能生效|
|gitLicense|是否添加 License，若为 true，gitEnabled 必须为 true 才能生效|
|gitIgnore|是否添加 gitignore，若不为 no，true，gitEnabled 必须为 true 才能生效。若要添加，则写上对应 gitignore 文件名称即可|
|shared|是否共享源代码|
|type|写 2 就对了，不知道什么含义|

Response:
```json
{
    "code": 0,
    "data": "/p/code"
}
```

|键值|说明|
|--|--|
|data|项目地址|