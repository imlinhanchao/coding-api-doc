# 新建合并请求

在仓库种新建合并请求，无需 scope 授权。

Request:
```
POST /api/user/:team/project/:project/depot/:depot/git/merge

srcBranch=develop&
desBranch=master&
title=Merge Title&
content=Merge Description&
reviewers=SnlleiNbUS,HHEqJATZdd&
labels=12770695&
watchers=SnlleiNbUS,HHEqJATZdd&
```

|键|说明|
|--|--|
|team|团队名|
|project|项目名|
|depot|仓库名|
|srcBranch|来源分支名|
|desBranch|目标分支名|
|title|合并请求标题|
|content|合并请求说明|
|reviewers|评审者用户名，多个用逗号隔开|
|labels|标签 Id，多个用逗号隔开|
|watchers|关注者用户名，多个用逗号隔开|

Response:
```json
{
    "code": 0,
    "data": {
        "can_edit": true,
        "can_edit_src_branch": true,
        "merge_request": {
            "merged_sha": "1233f19cc199fb539490eb86e61045d5461e8883",
            "diffStat": {
                "paths": [
                    {
                        "changeType": "MODIFY",
                        "insertions": 51,
                        "deletions": 86,
                        "name": "README.md",
                        "path": "README.md",
                        "size": 4184,
                        "mode": 33188,
                        "objectId": "f9f7614095cec6a01620d9bed7fac3b040b98937",
                        "commitId": "c70c0bb84dd32a653c7029741c52757faacbcd85"
                    }
                ],
                "commitId": "c70c0bb84dd32a653c7029741c52757faacbcd85",
                "oldSha": "c70db37c4d694a536d086da737c58caa56112434",
                "newSha": "c70c0bb84dd32a653c7029741c52757faacbcd85",
                "insertions": 51,
                "deletions": 86
            },
            "commits": [
                {
                    "fullMessage": "新增 new feature",
                    "shortMessage": "新增 new feature\n",
                    "allMessage": "",
                    "commitId": "c70c0bb84dd32a653c7029741c52757faacbcd85",
                    "commitTime": 1586855626000,
                    "committer": {
                        "name": "跳跳",
                        "email": "imlinhanchao@gmail.com",
                        "avatar": "https://dn-coding-net-production-static.codehub.cn/cc500da5-4b86-4cd2-8d6c-9d375a7ffcd8.jpg?imageMogr2/auto-orient/format/jpeg/crop/!458x458a0a0",
                        "link": "/u/SnlleiNbUS"
                    },
                    "notesCount": 0,
                    "rawMessage": "新增 new feature"
                }
            ],
            "body": "<p>xxx</p>",
            "body_plan": "xxx",
            "source_sha": "c70c0bb84dd32a653c7029741c52757faacbcd85",
            "target_sha": "c70db37c4d694a536d086da737c58caa56112434",
            "base_sha": "c70db37c4d694a536d086da737c58caa56112434",
            "conflicts": [],
            "srcBranchDeleted": false,
            "canDeleteSrcBranch": true,
            "id": 6347209,
            "srcBranch": "new-feature",
            "desBranch": "master",
            "title": "xxxx",
            "iid": 16,
            "merge_status": "CANMERGE",
            "path": "/p/coding-demo/d/coding-demo/git/merge/16",
            "created_at": 1586855695610,
            "updated_at": 1586855695610,
            "author": {
               // 创建者信息
            },
            "action_author": {
                // 创建者其他信息
            },
            "action_at": 1586855695610,
            "granted": 0,
            "comment_count": 0,
            "reminded": false
        }
    }
}
```
