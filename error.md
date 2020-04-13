# 错误代码

基于实验，不保证覆盖所有错误代码。

|Error Code|Message Code|Description|复现方式|
|--|--|--|--|
|905|network_connection_error|网络连接异常，请重试||
|1100|project_not_exists|项目不存在|传递了错误的项目 Id 进行项目的修改|
|1161|project_display_name_exists|项目名称已经存在，请重新填写项目名称|创建同名项目|
|1217|file_exists|文件已存在|在仓库新建已经存在的文件|
|1400|permission_denied|无权访问，请联系团队管理员为您设置权限|没有传递 Token|
|3007|tean_not_exist|团队不存在|团队域名写错了|
|3015|oauth_user_scope_error|当前的 scope 不支持访问此 API|Token 没有开启对应权限|
