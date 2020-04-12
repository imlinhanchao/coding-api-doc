# 仓库信息

获取仓库基本信息。这不需要任何授权。

```Request
GET /api/user/:team_name/project/:project_name/depot/:depot_name/[git/svn]
```

|键|说明|
|--|--|
|team_name|团队域名|
|project_name|项目名|
|depot_name|仓库名|
|git/svn|根据仓库类型选择|

不同类型(Git/SVN)仓库 Response 内容是不同的：

Response(Git):
```json
{
    "code": 0,
    "data": {
        "depot": {
            "id": 7796833,
            "depot_type": "CODING",
            "parent_id": 0,
            "project_id": 7763581,
            "root_id": 7796833,
            "path": "imlinhanchao/coding-demo",
            "origin_url": "",
            "created_at": 1586592635000,
            "default_branch": "master",
            "depot_path": "/p/coding-demo/d/coding-demo/git",
            "name": "coding-demo",
            "actual_depot_name": "coding-demo",
            "status": 1,
            "owner": {
                // 所有者信息
            },
            "parent": {
                "depot_type": "CODING",
                "hasCommits": false,
                "svn_enabled": false,
                "releaseCount": 0,
                "branchCount": 0,
                "tagCount": 0,
                "size": 0,
                "shared": false
            },
            "hasCommits": true,
            "svn_enabled": false,
            "lastCommitSha": "89f53a77e90c4a920b3e1a4d79f58cacc0378091",
            "releaseCount": 1,
            "branchCount": 2,
            "tagCount": 1,
            "size": 240,
            "gitHttpsUrl": "https://e.coding.net/imlinhanchao/coding-demo.git",
            "gitWebUrl": "https://imlinhanchao.coding.net/p/coding-demo/d/coding-demo",
            "gitSshUrl": "git@e.coding.net:imlinhanchao/coding-demo.git",
            "shared": false,
            "gitHttpsHost": "https://e.coding.net",
            "gitSshHost": "git@e.coding.net"
        }
    }
}
```

|键|说明|
|--|--|
|id|仓库 Id|
|depot_type|仓库类型，目前只有 `CODING`|
|parent_id|#Unknown|
|project_id|项目 Id|
|root_id|#Unknown|
|path|仓库所在路径|
|origin_url|#Unknown|
|created_at|创建时间|
|default_branch|默认分支|
|depot_path|仓库地址|
|name|仓库名|
|actual_depot_name|目前看与仓库名值一致|
|status|#Unknown|
|owner|所有者信息|
|parent|#Unknown|
|hasCommits|是否有提交代码|
|svn_enabled|SVN 是否开启|
|releaseCount|Release 个数|
|branchCount|分支个数|
|tagCount|分支个数|
|size|仓库大小，单位为 KB|
|gitHttpsUrl|仓库 HTTPS 地址|
|gitWebUrl|仓库网页地址|
|gitSshUrl|仓库 SSH 地址|
|shared|是否开放源代码|
|gitHttpsHost|HTTPS 域|
|gitSshHost|SSH 域|

Response(Svn):
```json
{
    "code": 0,
    "data": {
        "depot": {
            "id": 7796842,
            "name": "svn_demo",
            "size": 0,
            "actual_depot_name": "svn_demo",
            "path": "imlinhanchao/svn_demo",
            "origin_url": "",
            "created_at": 1586592861000,
            "depot_path": "/p/svn_demo/d/svn_demo/svn",
            "vcs_type": "svn",
            "status": 1,
            "isSvnHttp": false,
            "shared": false,
            "svn_enabled": true,
            "svnHttpsUrl": "https://e-svn.coding.net/imlinhanchao/svn_demo/svn_demo",
            "svnWebUrl": "https://imlinhanchao.coding.net/p/svn_demo/d/svn_demo",
            "svnSshUrl": "svn+ssh://subversion.e.coding.net/imlinhanchao/svn_demo",
            "svnUrl": "svn://subversion.e.coding.net/imlinhanchao/svn_demo",
            "svnHost": "svn://subversion.e.coding.net",
            "svnSshHost": "svn+ssh://subversion.e.coding.net"
        }
    }
}
```

|键|说明|
|--|--|
|id|仓库 Id|
|name|仓库名|
|actual_depot_name|目前看与仓库名值一致|
|origin_url|#Unknown|
|created_at|创建时间|
|depot_path|仓库地址|
|vcs_type|版本管理类型|
|status|#Unknown|
|isSvnHttp|是否开启 HTTP|
|shared|是否开放源代码|
|svn_enabled|Svn 是否启用|
|svnHttpsUrl|SVN HTTPS 地址|
|svnWebUrl|网页地址|
|svnSshUrl|SSH 地址|
|svnUrl|SVN 协议地址|
|svnHost|SVN 协议域|
|svnSshHost|SSH 域|

