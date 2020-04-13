# 创建文件

在仓库中创建新的文件，无需 scope 授权。一共分成两个步骤。

## 获取最后的提交 Hash

Request:
```
GET /api/user/:team/project/:project/depot/:depot/git/new/:branch
```

|键|说明|
|--|--|
|team|团队名|
|project|项目名|
|depot|仓库名|
|branch|分支名|

Response:
```json
{
    "code": 0,
    "data": {
        "path": "",
        "ref": "master",
        "can_edit": true,
        "lastCommit": "3a2cd6cfce73f97f128abad8bff4a0147df2072e"
    }
}
```

|键|说明|
|--|--|
|path|文件路径，一直为空|
|ref|分支名|
|can_edit|能否编辑，目前没有发现 false 的情况|
|lastCommit|最后提交的 Hash|

Request:
```
POST /api/user/:team/project/:project/depot/:depot/git/new/:branch

title:test/test.js
content:123
message:提交说明
lastCommitSha:3a2cd6cfce73f97f128abad8bff4a0147df2072e
newRef:
```

|键|说明|
|--|--|
|team|团队名|
|project|项目名|
|depot|仓库名|
|branch|分支名|
|folder|保存文件夹，空为根目录。文件夹若不存在，则自动创建|
|title|保存路径，包含文件名|
|content|文件内容|
|message|提交说明|
|lastCommitSha|最后提交的 Hash|
|newRef|如果要以此提交创建新分支，则传递新分支名|

Response:
```json
{
    "code": 0
}
```