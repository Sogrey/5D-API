## 施工日志提交

> 用于提交施工日志

### 1. 请求说明

> 请求方式：POST
>
> 请求URL ：`/api/AppApi/submitConstructMonthLog `

### 2. 请求参数

> 请求参数按照示例传入一个json字符串，其格式为[查询施工日志详情](GetConstructMonthLogInfo.md)接口的返回格式。

body:

| **参数**   |  **数据类型** | 是否必须 | 描述           |
| ---------- |  :----------: | :------: | -------------- |
| **Pmodel** | String | Y | 传入json字符串 |

json传中的各字段：

| **参数**                               | 子字段               | **数据类型** | 是否必须 | 描述                                                   |
| -------------------------------------- | -------------------- | ------------ | :------: | ------------------------------------------------------ |
| **R_Construction_logModel**            |                      |              |          | 日志详情内容                                           |
|                                        | **AddDate**          | **String**   |    Y     | 提报日期                                               |
|                                        | **Adder**            | **String**   |    Y     | 提报人                                                 |
|                                        | **ConstructionUnit** | **String**   |    Y     | 施工单位                                               |
|                                        | **PostName**         | String       |          | 施工专业名称                                           |
|                                        | **Postid**           | String       |          | 施工专业ID                                             |
|                                        | **Projectid**        | String       |          | 项目ID                                                 |
|                                        | **SafetyShow**       | String       |          | 安全质量问题                                           |
|                                        | **Situation**        | String       |          | 施工情况                                               |
|                                        | **SituationShow**    | String       |          | 施工工作总结                                           |
|                                        | **UserName**         | String       |          | 提报人名字                                             |
|                                        | **UserNum**          | String       |          | 人员数目                                               |
|                                        | **WeatherName**      | String       |          | 天气名称                                               |
|                                        | **equipmentNum**     | String       |          | 施工机具数目                                           |
|                                        | **equipmentShwo**    | String       |          | 设备使用情况                                           |
|                                        | **problem**          | String       |          | 存在问题                                               |
|                                        | **rq**               | String       |          | 填报日志日期                                           |
|                                        | **weatherID**        | **String**   |    Y     | 天气ID                                                 |
| **R_Construction_logDetailsModelList** |                      | Array        |    Y     | 施工部位列表                                           |
|                                        | **CompletePercent**  | String       |          | 完成百分比                                             |
|                                        | **IsDelete**         | String       |          | true 自定义任务，false计划任务                         |
|                                        | **PEndDate**         | String       |          | 计划截止时间                                           |
|                                        | **PStartDate**       | String       |          | 计划开始时间                                           |
|                                        | **PUserNum**         | String       |          | 计划人数                                               |
|                                        | **PEquipMent**       | String       |          | 计划设备                                               |
|                                        | **REquipMent**       | String       |          | 实际设备                                               |
|                                        | **RUserNum**         | String       |          | 实际人数                                               |
|                                        | **TaskID**           | String       |          | 计划ID，自定义任务没有                                 |
|                                        | **Type**             | String       |          | 1计划内任务，2自定义任务                               |
|                                        | **id**               | String       |          | 自定义任务id为 `tmp_`开头,提交后服务器处理数据时id自增 |
|                                        | **site**             | String       |          | 施工部位                                               |
| **R_Construction_logFileModelList**    |                      | Array        |          | 附件列表                                               |
|                                        | **filepath**         | String       |          | 上传文件路径                                           |
|                                        | **filetype**         | String       |          | 文件类型，后缀名                                       |
|                                        | **filename**         | String       |          | 文件名，描述                                           |

示例:

``` json
{
    "ConstructionUnitName": null, 
    "FilePathAndName": null, 
    "IsCanEdit": true, 
    "LogDetails": null, 
    "PlanTaskList": null, 
    "R_Construction_logDetailsModelList": [
        {
            "CompletePercent": "50.00", 
            "IsDelete": false, 
            "Lid": "", 
            "PEndDate": "2018/12/19", 
            "PEquipMent": "0", 
            "PStartDate": "2018/12/7", 
            "PUserNum": "0", 
            "REquipMent": "14", 
            "RUserNum": "12", 
            "TaskID": "fb155485-b7fd-4cbf-a84a-0d742f189c78", 
            "Type": "1", 
            "id": "tmp_1545105171305", 
            "site": "z16-2#桩基_桩基_桩基"
        }, 
        {
            "CompletePercent": "13", 
            "IsDelete": true, 
            "Lid": "", 
            "PEndDate": "2018-12-31", 
            "PEquipMent": "12", 
            "PStartDate": "2018-12-01", 
            "PUserNum": "15", 
            "REquipMent": "12", 
            "RUserNum": "14", 
            "TaskID": "", 
            "Type": "", 
            "id": "tmp_1545105234793", 
            "site": "自定义任务"
        }
    ], 
    "R_Construction_logFileModelList": [
        {
            "Lid": "", 
            "filename": "图片1", 
            "filepath": "/uploadFile/attachment/EF_20181218_115343393.jpg", 
            "filetype": ".jpg", 
            "id": ""
        }, 
        {
            "Lid": "", 
            "filename": "附件2", 
            "filepath": "/uploadFile/attachment/EF_20181218_115343395.jpg", 
            "filetype": ".jpg", 
            "id": ""
        }
    ], 
    "R_Construction_logModel": {
        "AddDate": "2018-12-18", 
        "Adder": "496", 
        "ConstructionUnit": "418", 
        "Lid": "0",  //不能为空，没有可传0
        "PostName": "土建", 
        "Postid": "1", 
        "Projectid": "61", 
        "SafetyShow": "安全质量问题", 
        "Situation": "施工情况", 
        "SituationShow": "工作总结", 
        "UserName": "wang2", 
        "UserNum": "15", 
        "WeatherName": "晴天", 
        "equipmentNum": "12", 
        "equipmentShwo": "设备使用情况", 
        "problem": "存在问题", 
        "rq": "2018-12-18", 
        "weatherID": "1"
    }, 
    "jsonYMD": null, 
    "userType": "2" //不能为空
}
```
### 3. 返回参数

| 字段        | 字段类型 | 字段说明               |
| ----------- | :------: | ---------------------- |
| **Code**    |  string  | 0：成功 ；其他：失败   |
| **CodeMsg** |  String  | 失败时原因信息         |

返回示例：

```json
{
  "Code": 0,
  "CodeMsg": "OK",
  "Datas": null
}
```