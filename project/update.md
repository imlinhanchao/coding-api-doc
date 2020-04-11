# 更新项目

更新项目基本信息，这个不需要任何 scope 授权。

Request:
```
PUT /api/project

id=7763347&
name=new_name&
description=新的描述&
startDate=2020-04-01&
endDate=2020-04-02&
displayName=新的名词&
```

|键值|说明|
|--|--|
|id|项目 Id|
|name|项目名|
|description|描述|
|startDate|项目时间始|
|endDate|项目时间终|
|displayName|项目显示名|

Response:
```json
{
    "code": 0,
    "data": {
        "created_at": 1586586477000,
        "backend_project_path": "/team/imlinhanchao/project/test",
        "description": "",
        "git_url": "git@e.coding.net:imlinhanchao/test.git",
        "ssh_url": "git@e.coding.net:imlinhanchao/test.git",
        "svn_url": "svn+ssh://svn@svn.e.coding.net/imlinhanchao/test",
        "is_public": false,
        "https_url": "https://e.coding.net/imlinhanchao/test.git",
        "vcs_type": "git",
        "subversion_url": "svn.e.coding.net/imlinhanchao/test",
        "id": 7763347,
        "name": "test",
        "name_pinyin": "cs|csh|ceshi",
        "display_name": "测试",
        "owner_id": 0,
        "owner_user_name": "imlinhanchao",
        "owner_user_picture": "https://dn-coding-net-production-static.codehub.cn/cc500da5-4b86-4cd2-8d6c-9d375a7ffcd8.jpg?imageMogr2/auto-orient/format/jpeg/crop/!458x458a0a0",
        "owner_user_home": "<a href=\"https://imlinhanchao.coding.net/u/SnlleiNbUS\">SnlleiNbUS</a>",
        "project_path": "/p/test",
        "status": 1,
        "type": 2,
        "updated_at": 1586620794000,
        "last_updated": 1586620794000,
        "fork_count": 0,
        "star_count": 0,
        "watch_count": 0,
        "pin": false,
        "depot_path": "/p/test/d/test/git",
        "forked": false,
        "un_read_activities_count": 0,
        "icon": "/static/project_icon/scenery-version-2-10.svg",
        "current_user_role_id": 90,
        "current_user_role": "admin",
        "stared": false,
        "watched": false,
        "recommended": 0,
        "shared": true,
        "is_member": true,
        "max_member": 0,
        "groupId": 0,
        "plan": 1,
        "isTeam": true,
        "archived": false,
        "taskHide": true,
        "default_depot_name": "test",
        "agile_feature_initialized": true
    }
}
```

字段描述见[项目信息](info.md)