# 仓库列表

获取项目内的仓库列表，此功能不需要任何授权。

Request:
```
GET /api/user/:team_name/project/:project_name/depots
```

|键|说明|
|--|--|
|team_name|团队域名|
|project_name|项目名|

Response:
```json
{
    "code": 0,
    "data": [
        {
            "id": 7796833,
            "name": "coding-demo",
            "isDefault": true,
            "vcsType": "git",
            "svnEnabled": false,
            "shared": false,
            "depotPath": "/p/coding-demo/d/coding-demo/git",
            "size": 240,
            "gitHttpsUrl": "https://e.coding.net/team_name/coding-demo.git",
            "gitSshUrl": "git@e.coding.net:team_name/coding-demo.git",
            "gitHttpsHost": "https://e.coding.net",
            "gitSshHost": "git@e.coding.net",
            "isSvnHttp": false
        },
        {
            "id": 7796842,
            "name": "svn_demo",
            "isDefault": true,
            "vcsType": "svn",
            "svnEnabled": false,
            "shared": false,
            "depotPath": "/p/coding-demo/d/svn_demo/svn",
            "size": 0,
            "svnHttpUrl": "https://e-svn.coding.net/team_name/svn_demo/svn_demo",
            "svnUrl": "svn://subversion.e.coding.net/team_name/svn_demo",
            "svnSshUrl": "svn+ssh://subversion.e.coding.net/team_name/svn_demo",
            "isSvnHttp": false
        }
    ]
}
```

|键|说明|
|--|--|
|id|仓库 Id|
|name|仓库名|
|isDefault|是否默认仓库|
|vcsType|仓库类型|
|svnEnabled|是否启用了 SVN|
|shared|是否开放源代码|
|depotPath|仓库路径|
|size|仓库大小，单位为 KB|
|gitHttpsUrl/svnHttpUrl|仓库 HTTP 地址|
|gitSshUrl/svnSshUrl|仓库 SSH 地址|
|svnUrl|SVN 地址|
|gitHttpsHost|Git HTTP 域|
|gitSshHost|Git SSH 域|
|isSvnHttp|是否启用 SVN HTTP|