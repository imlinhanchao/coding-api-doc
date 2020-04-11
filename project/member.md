# 项目成员
项目成员相关接口，需要设置 `project` 的 scope 授权。

## 获取项目成员
获取项目的参与成员列表，需要项目 Id `project_id`。

Request:
```
GET /api/project/:project_id/members?page=1&pageSize=200
```

|键|说明|
|--|--|
|project_id|项目 Id|
|page|第几页|
|pageSize|每页个数|

Response:
```json
{
    "code": 0,
    "data": {
        "list": [{
            "id": 10929327,
            "project_id": 7763347,
            "user_id": 2492081,
            "type": 90,
            "alias": "",
            "team_alias": "",
            "created_at": 1586586477000,
            "last_visit_at": 1586592518000,
            "user": {
                // 用户个人信息
            },
            "roles": [{
                "roleId": 57806545,
                "name": "项目管理员",
                "description": "",
                "roleType": "ProjectAdmin",
                "isRoleCanEdit": false,
                "isRoleCanDelete": false,
                "isPermissionCanEdit": false,
                "createdAt": 1586586477000
            }]
        }],
        "page": 1,
        "pageSize": 200,
        "totalPage": 1,
        "totalRow": 1
    }
}
```

|键值|说明|
|--|--|
|list|项目列表|
|- id|成员 Id|
|- project_id|项目 Id|
|- type|#Unknown|
|- alias|别名|
|- team_alias|团队别名|
|- created_at|添加日期|
|- last_visit_at|最后访问日期|
|- user|用户信息|
|- roles|用户角色|
|- - roleId| 角色 Id|
|- - name|角色名称|
|- - description|角色描述|
|- - roleType|角色类型|
|- - isRoleCanEdit|角色是否可编辑|
|- - isRoleCanDelete|角色是否可删除|
|- - isPermissionCanEdit|权限是否可编辑|
|- - createdAt|创建时间|
|page|页码|
|pageSize|每页个数|
|totalPage|页数总和|
|totalRow|总条目数|

## 添加成员

添加项目成员，你需要成员的用户名。添加后默认为**开发**角色。需要设置 `project:members` 的 scope 授权。

Request:

```
POST /api/project/:project_id/members/gk/add

users=username
```

|键|说明|
|--|--|
|project_id|项目 Id|
|users|用户名|

Response:
```json
{
    "code": 0,
    "data": 1
}
```

## 移除成员

将成员从项目移除，需要设置 `project:members` 的 scope 授权。

Request:

```
POST /api/project/:project_id/kickout/:member_id

users=username
```

|键|说明|
|--|--|
|project_id|项目 Id|
|member_id|成员 Id，也就是成员列表中获得的 Id|

Response:
```json
{
    "code": 0
}
```