# 项目列表

获取授权用户所有能访问的项目信息。需要设置 `project` 的 scope 授权。

Request:

```
GET /api/user/projects
```

Response:

```json
{
    "code": 0,
    "data": {
        "list": [
            {
                "created_at": 1412009297000,
                "backend_project_path": "/team/team_name/project/project_name",
                "description": "Project Description",
                "git_url": "git@e.coding.net:team_name/project_name.git",
                "ssh_url": "git@e.coding.net:team_name/project_name.git",
                "svn_url": "svn+ssh://svn@svn.e.coding.net/team_name/project_name",
                "is_public": false,
                "https_url": "https://e.coding.net/team_name/project_name.git",
                "vcs_type": "git",
                "subversion_url": "svn.e.coding.net/team_name/project_name",
                "id": 2796962,
                "name": "project_name",
                "name_pinyin": "",
                "display_name": "project_name",
                "owner_id": 0,
                "owner_user_name": "team_name",
                "owner_user_picture": "https://dn-coding-net-production-static.codehub.cn/cc500da5-4b86-4cd2-8d6c-9d375a7ffcd8.jpg?imageMogr2/auto-orient/format/jpeg/crop/!458x458a0a0",
                "owner_user_home": "<a href=\"https://team_name.coding.net/u/user_name\">user_name</a>",
                "project_path": "/p/project_name",
                "status": 1,
                "type": 2,
                "updated_at": 1581083137000,
                "fork_count": 0,
                "star_count": 0,
                "watch_count": 0,
                "pin": false,
                "depot_path": "/p/project_name/d/depot_name/git",
                "forked": false,
                "un_read_activities_count": 0,
                "icon": "/static/project_icon/scenery-21.png",
                "current_user_role_id": 90,
                "current_user_role": "admin",
                "stared": false,
                "watched": false,
                "recommended": 0,
                "shared": false,
                "is_member": false,
                "max_member": 0,
                "groupId": 0,
                "plan": 1,
                "isTeam": true,
                "archived": false,
                "isDemo": false,
                "taskHide": true,
                "default_depot_name": "project_name",
                "agile_feature_initialized": false
            }
        ],
        "page": 1,
        "pageSize": 1,
        "totalPage": 111,
        "totalRow": 111
    }
}
```

|键值|说明|
|--|--|
|list|项目列表|
|- created_at|创建日期|
|- backend_project_path|API 地址路径|
|- description|项目描述|
|- git_url|Git 仓库地址|
|- ssh_url|SSH 仓库地址|
|- svn_url|SVN 仓库地址|
|- https_url| Https 仓库地址|
|- is_public|是否公共的项目，默认 false，目前没有发现使之变 true 的方法|
|- vcs_type|代码托管类型：git 或 svn|
|- subversion_url |SVN 地址|
|- id|项目 Id|
|- name|项目名|
|- name_pinyin|项目显示名拼音，英文项目名则为空|
|- display_name|项目显示名称|
|- owner_id|所有者 Id|
|- owner_user_name|所有者用户名|
|- owner_user_picture|所有者头像|
|- owner_user_home|所有者主页|
|- project_path|项目路径|
|- status| #Unknown|
|- type|#Unknown|
|- updated_at|最后更新日期|
|- fork_count|fork 数|
|- star_count|Star 数|
|- watch_count|Watch 数|
|- pin|#Unknown|
|- depot_path|默认仓库地址|
|- un_read_activities_count|未读活动|
|- icon|项目图标|
|- current_user_role_id|用户角色 Id|
|- current_user_role|用户角色|
|- shared|仓库是否开启开放源代码|
|- is_member|#Unknown|
|- max_member|#Unknown|
|- groupId|分组 Id|
|- plan|#Unknown|
|- isTeam|#Unknown|
|- archived|是否归档|
|- isDemo|是否示例项目|
|- taskHide|#Unknown|
|- default_depot_name|默认仓库名|
|page|页码|
|pageSize|每页个数|
|totalPage|页数总和|
|totalRow|总条目数|
