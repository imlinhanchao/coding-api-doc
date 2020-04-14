# 上传文件

上传文件到仓库，不支持 SVN 仓库，无需 scope 授权。和创建文件一样，包含两个步骤。

## 获取最后的提交 Hash

见[创建文件](create.md)。

## 发送文件内容

Request:

```
POST /api/user/:team/project/:project/depot/:depot/git/upload/:branch/:folder

Content-Type: multipart/form-data; boundary=----WebKitFormBoundary:boundarykey

------WebKitFormBoundary:boundarykey
Content-Disposition: form-data; name="message"

:message
------WebKitFormBoundary:boundarykey
Content-Disposition: form-data; name="lastCommitSha"

:lastCommitSha
------WebKitFormBoundary:boundarykey
Content-Disposition: form-data; name="newRef"

:newRef
------WebKitFormBoundary:boundarykey
Content-Disposition: form-data; name="filename1.jpg"; filename="filename1.jpg"
Content-Type: image/jpeg

:file1_buffer
------WebKitFormBoundary:boundarykey
Content-Disposition: form-data; name="filename2.jpg"; filename="filename2.jpg"
Content-Type: image/jpeg

:file2_buffer
------WebKitFormBoundary:boundarykey--
```

|键|说明|
|--|--|
|team|团队名|
|project|项目名|
|depot|仓库名|
|branch|分支名|
|folder|保存文件夹，空为根目录。文件夹若不存在，则自动创建|
|message|提交说明|
|lastCommitSha|最后提交的 Hash|
|newRef|如果要以此提交创建新分支，则传递新分支名|
|boundarykey|form data 请求分隔唯一标识，需要确保不会在文件或表单项的内容中出现。|

提交请求类型为 `multipart/formdata`，前面包含表单说明，最后加上要上传的文件 buffer，文件名做为 key，多个文件就加多个。

Response:
```json
{
    "code": 0
}
```