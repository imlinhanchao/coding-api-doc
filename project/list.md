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
                "depot_path": "/p/project_name/d/project_name/git",
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