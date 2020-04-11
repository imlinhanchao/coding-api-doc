# 项目信息
获取项目基本信息，需要设置 `project` 的 scope 授权。

Request:
```
GET /api/user/:team_name/project/:project_name
```

|键|说明|
|--|--|
|team_name|团队域名|
|project_name|项目名|

Response:

```json
{
    "code": 0,
    "data": {
        "created_at": 1586592635000,
        "backend_project_path": "/team/team_name/project/coding-demo",
        "description": "CODING 示例项目",
        "git_url": "git@e.coding.net:team_name/coding-demo.git",
        "ssh_url": "git@e.coding.net:team_name/coding-demo.git",
        "svn_url": "svn+ssh://svn@svn.e.coding.net/team_name/coding-demo",
        "is_public": false,
        "https_url": "https://e.coding.net/team_name/coding-demo.git",
        "vcs_type": "git",
        "subversion_url": "svn.e.coding.net/team_name/coding-demo",
        "id": 7763581,
        "name": "coding-demo",
        "name_pinyin": "slxm|shlxm|shilixiangmu",
        "display_name": "示例项目",
        "owner_id": 0,
        "owner_user_name": "team_name",
        "owner_user_picture": "https://dn-coding-net-production-static.codehub.cn/cc500da5-4b86-4cd2-8d6c-9d375a7ffcd8.jpg?imageMogr2/auto-orient/format/jpeg/crop/!458x458a0a0",
        "owner_user_home": "\u003ca href\u003d\"https://team_name.coding.net/u/SnlleiNbUS\"\u003eSnlleiNbUS\u003c/a\u003e",
        "project_path": "/p/coding-demo",
        "status": 1,
        "type": 2,
        "updated_at": 1586592635000,
        "last_updated": 1586592678000,
        "fork_count": 0,
        "star_count": 0,
        "watch_count": 0,
        "pin": false,
        "depot_path": "/p/coding-demo/d/coding-demo/git",
        "forked": false,
        "un_read_activities_count": 0,
        "icon": "https://dn-coding-net-production-pp.codehub.cn/79a8bcc4-d9cc-4061-940d-5b3bb31bf571.png",
        "current_user_role_id": 90,
        "current_user_role": "admin",
        "owner": {
            // 所有者用户信息
        },
        "stared": false,
        "watched": false,
        "recommended": 0,
        "shared": false,
        "is_member": true,
        "max_member": 0,
        "groupId": 0,
        "plan": 1,
        "isTeam": true,
        "archived": false,
        "isDemo": true,
        "taskHide": true,
        "default_depot_name": "coding-demo",
        "last_visit_depot_name": "coding-demo",
        "cooperate_settings": [],
        "agile_feature_initialized": true,
        "test": []
    }
}
```

|键值|说明|
|--|--|
|created_at|创建日期|
|backend_project_path|API 地址路径|
|description|项目描述|
|git_url|Git 仓库地址|
|ssh_url|SSH 仓库地址|
|svn_url|SVN 仓库地址|
|https_url| Https 仓库地址|
|is_public|是否公共的项目，默认 false，目前没有发现使之变 true 的方法|
|vcs_type|代码托管类型：git 或 svn|
|subversion_url |SVN 地址|
|id|项目 Id|
|name|项目名|
|name_pinyin|项目显示名拼音，英文项目名则为空|
|display_name|项目显示名称|
|owner_id|#似乎总是 0|
|owner_user_name|所有者用户名|
|owner_user_picture|所有者头像|
|owner_user_home|所有者主页|
|project_path|项目路径|
|status|#Unknown|
|type|#Unknown|
|updated_at|最后更新日期|
|fork_count|fork 数|
|star_count|Star 数|
|watch_count|Watch 数|
|pin|#Unknown|
|depot_path|默认仓库地址|
|un_read_activities_count|未读活动|
|icon|项目图标|
|current_user_role_id|用户角色 Id|
|current_user_role|用户角色|
|owner|所有者信息|
|shared|仓库是否开启开放源代码|
|is_member|#Unknown|
|max_member|#Unknown|
|groupId|分组 Id|
|plan|#Unknown|
|isTeam|#Unknown|
|archived|是否归档|
|isDemo|是否示例项目|
|taskHide|#Unknown|
|default_depot_name|默认仓库名|
|test|#Unknown|