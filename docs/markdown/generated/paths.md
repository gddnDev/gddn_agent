
<a name="paths"></a>
## 资源

<a name="agent-company-controller_resource"></a>
### Agent-company-controller
代理商授权企业管理


<a name="creatnewcompanyusingpost"></a>
#### 新增企业
```
POST /addCompany
```


##### 参数

|类型|名称|说明|类型|
|---|---|---|---|
|**Query**|**address**  <br>*必填*|详细地址|string|
|**Query**|**cityName**  <br>*必填*|企业城市名称|string|
|**Query**|**companyType**  <br>*必填*|企业类型(1.专业分包2.设备分包3.材料分包4.后勤服务5.特殊设备6.劳务分包7.监理8.建设单位9.总承包单位10.勘察11.设计单位12.租赁13.其他)|string (byte)|
|**Query**|**coname**  <br>*必填*|企业名称|string|
|**Query**|**contactsMobile**  <br>*必填*|联系人手机号|string|
|**Query**|**contactsName**  <br>*必填*|联系人姓名|string|
|**Query**|**memId**  <br>*必填*|管理员用户id|string|


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[成功的请求](#e5ddf48022ae6d2b4c39915efc48e0f8)|
|**201**|Created|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `*/*`


##### HTTP请求示例

###### 请求 path
```
/addCompany
```


###### 请求 query
```
json :
{
  "address" : "string",
  "cityName" : "string",
  "companyType" : "string",
  "coname" : "string",
  "contactsMobile" : "string",
  "contactsName" : "string",
  "memId" : "string"
}
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "code" : "string",
  "data" : "object",
  "message" : "string",
  "success" : false
}
```


<a name="agentstatisticsusingpost"></a>
#### 代理商统计信息：授权企业总数，当年授权企业总数
```
POST /agentCompanyStatistics
```


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[成功的请求«AgentStatistics»](#ffe815d8bd31d2ab15eea9d2fa51e71c)|
|**201**|Created|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `*/*`


##### HTTP请求示例

###### 请求 path
```
/agentCompanyStatistics
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "code" : "string",
  "data" : {
    "authenticatedQuantity" : "认证的总数",
    "currentYearOfAuthenticatedQuantity" : "今年认证的总数"
  },
  "message" : "string",
  "success" : false
}
```


<a name="dissolutioncompanyusingpost"></a>
#### 解散企业
```
POST /dissolutionCompany
```


##### 参数

|类型|名称|说明|类型|
|---|---|---|---|
|**Body**|**coId**  <br>*可选*|企业id|integer (int32)|


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[成功的请求](#e5ddf48022ae6d2b4c39915efc48e0f8)|
|**201**|Created|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `*/*`


##### HTTP请求示例

###### 请求 path
```
/dissolutionCompany
```


###### 请求 body
```
json :
{ }
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "code" : "string",
  "data" : "object",
  "message" : "string",
  "success" : false
}
```


<a name="listagentcompanyusingpost"></a>
#### 获取代理商管理的企业
```
POST /listCompany
```


##### 参数

|类型|名称|说明|类型|
|---|---|---|---|
|**Query**|**bluredCompanyName**  <br>*可选*|模糊查找名称（仅右模糊）|string|
|**Query**|**coid**  <br>*必填*|企业id|integer (int32)|
|**Query**|**page**  <br>*可选*|页码：空值或不传，默认返回所有值|string|
|**Query**|**pjId**  <br>*必填*|项目id|integer (int32)|
|**Query**|**size**  <br>*可选*|每页行数：空值或不传，默认返回所有值|string|
|**Query**|**type**  <br>*必填*|代理商类型：0 全国代理商1 区域代理商|string|


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[成功的请求«Pagination«CompanyVo»»](#a69fad129a99ca29233d74c1293f9e76)|
|**201**|Created|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `*/*`


##### HTTP请求示例

###### 请求 path
```
/listCompany
```


###### 请求 query
```
json :
{
  "bluredCompanyName" : "string",
  "coid" : 0,
  "page" : "string",
  "pjId" : 0,
  "size" : "string",
  "type" : "string"
}
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "code" : "string",
  "data" : {
    "list" : "结果列表",
    "page" : "页码",
    "size" : "每页行数",
    "totalPage" : "总页数",
    "totalRows" : "总行数"
  },
  "message" : "string",
  "success" : false
}
```


<a name="updatenewcompanyusingpost"></a>
#### 更新企业
```
POST /updateCompany
```


##### 参数

|类型|名称|说明|类型|
|---|---|---|---|
|**Query**|**address**  <br>*必填*|详细地址|string|
|**Query**|**cityName**  <br>*必填*|企业城市名称|string|
|**Query**|**companyType**  <br>*必填*|企业类型(1.专业分包2.设备分包3.材料分包4.后勤服务5.特殊设备6.劳务分包7.监理8.建设单位9.总承包单位10.勘察11.设计单位12.租赁13.其他)|string (byte)|
|**Query**|**coname**  <br>*必填*|企业名称|string|
|**Query**|**contactsMobile**  <br>*必填*|联系人手机号|string|
|**Query**|**contactsName**  <br>*必填*|联系人姓名|string|
|**Query**|**memId**  <br>*必填*|管理员用户id|string|


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[成功的请求](#e5ddf48022ae6d2b4c39915efc48e0f8)|
|**201**|Created|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `*/*`


##### HTTP请求示例

###### 请求 path
```
/updateCompany
```


###### 请求 query
```
json :
{
  "address" : "string",
  "cityName" : "string",
  "companyType" : "string",
  "coname" : "string",
  "contactsMobile" : "string",
  "contactsName" : "string",
  "memId" : "string"
}
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "code" : "string",
  "data" : "object",
  "message" : "string",
  "success" : false
}
```


<a name="agent-project-controller_resource"></a>
### Agent-project-controller
代理商授权项目管理


<a name="creatnewprojectusingpost"></a>
#### 新增项目
```
POST /addProject
```


##### 参数

|类型|名称|说明|类型|
|---|---|---|---|
|**Query**|**aliasProjectTitle**  <br>*必填*|项目别名|string|
|**Query**|**investAmount**  <br>*必填*|投资总额（万元）|string|
|**Query**|**memberId**  <br>*必填*|项目负责人id|string|
|**Query**|**pointx**  <br>*必填*|项目定位x|number (double)|
|**Query**|**pointy**  <br>*必填*|项目定位y|number (double)|
|**Query**|**projectLogo**  <br>*必填*|项目logo|string|
|**Query**|**projectTitle**  <br>*必填*|项目标题|string|
|**Query**|**projectType**  <br>*必填*|项目类型 1-房建项目 2-市政项目 3-专业工程 4-其他|integer (int32)|
|**Query**|**scale**  <br>*必填*|建设规模 1 小型 2 中型 3 大型|string (byte)|
|**Query**|**status**  <br>*必填*|状态：1-在建 2-完成 3-删除|string (byte)|


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[成功的请求](#e5ddf48022ae6d2b4c39915efc48e0f8)|
|**201**|Created|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `*/*`


##### HTTP请求示例

###### 请求 path
```
/addProject
```


###### 请求 query
```
json :
{
  "aliasProjectTitle" : "string",
  "investAmount" : "string",
  "memberId" : "string",
  "pointx" : 0.0,
  "pointy" : 0.0,
  "projectLogo" : "string",
  "projectTitle" : "string",
  "projectType" : 0,
  "scale" : "string",
  "status" : "string"
}
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "code" : "string",
  "data" : "object",
  "message" : "string",
  "success" : false
}
```


<a name="agentstatisticsusingpost_1"></a>
#### 代理商统计信息：授权项目总数，当年授权项目总数
```
POST /agentProjectStatistics
```


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[成功的请求«AgentStatistics»](#ffe815d8bd31d2ab15eea9d2fa51e71c)|
|**201**|Created|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `*/*`


##### HTTP请求示例

###### 请求 path
```
/agentProjectStatistics
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "code" : "string",
  "data" : {
    "authenticatedQuantity" : "认证的总数",
    "currentYearOfAuthenticatedQuantity" : "今年认证的总数"
  },
  "message" : "string",
  "success" : false
}
```


<a name="authorizeprojectusingpost"></a>
#### 项目授权
```
POST /authorize
```


##### 参数

|类型|名称|说明|类型|
|---|---|---|---|
|**Query**|**products**  <br>*必填*|产品列表|< integer (int32) > array(multi)|
|**Query**|**projectId**  <br>*必填*|项目id|integer (int32)|


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[成功的请求](#e5ddf48022ae6d2b4c39915efc48e0f8)|
|**201**|Created|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `*/*`


##### HTTP请求示例

###### 请求 path
```
/authorize
```


###### 请求 query
```
json :
{
  "products" : 0,
  "projectId" : 0
}
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "code" : "string",
  "data" : "object",
  "message" : "string",
  "success" : false
}
```


<a name="dissolutionprojectusingpost"></a>
#### 删除项目
```
POST /dissolutionProject
```


##### 参数

|类型|名称|说明|类型|
|---|---|---|---|
|**Body**|**proId**  <br>*可选*|项目id|integer (int32)|


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[成功的请求](#e5ddf48022ae6d2b4c39915efc48e0f8)|
|**201**|Created|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `*/*`


##### HTTP请求示例

###### 请求 path
```
/dissolutionProject
```


###### 请求 body
```
json :
{ }
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "code" : "string",
  "data" : "object",
  "message" : "string",
  "success" : false
}
```


<a name="listagentprojectusingpost"></a>
#### 获取代理商管理的项目
```
POST /listProject
```


##### 参数

|类型|名称|说明|类型|
|---|---|---|---|
|**Query**|**bluredCompanyName**  <br>*可选*|模糊查找名称（仅右模糊）|string|
|**Query**|**coid**  <br>*必填*|企业id|integer (int32)|
|**Query**|**page**  <br>*可选*|页码：空值或不传，默认返回所有值|string|
|**Query**|**pjId**  <br>*必填*|项目id|integer (int32)|
|**Query**|**size**  <br>*可选*|每页行数：空值或不传，默认返回所有值|string|
|**Query**|**type**  <br>*必填*|代理商类型：0 全国代理商1 区域代理商|string|


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[成功的请求«Pagination«ProjectVo»»](#6b37d272121b46efe207fa6e17b2fb09)|
|**201**|Created|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `*/*`


##### HTTP请求示例

###### 请求 path
```
/listProject
```


###### 请求 query
```
json :
{
  "bluredCompanyName" : "string",
  "coid" : 0,
  "page" : "string",
  "pjId" : 0,
  "size" : "string",
  "type" : "string"
}
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "code" : "string",
  "data" : {
    "list" : "结果列表",
    "page" : "页码",
    "size" : "每页行数",
    "totalPage" : "总页数",
    "totalRows" : "总行数"
  },
  "message" : "string",
  "success" : false
}
```


<a name="updatenewprojectusingpost"></a>
#### 更新项目
```
POST /updateProject
```


##### 参数

|类型|名称|说明|类型|
|---|---|---|---|
|**Query**|**aliasProjectTitle**  <br>*必填*|项目别名|string|
|**Query**|**investAmount**  <br>*必填*|投资总额（万元）|string|
|**Query**|**memberId**  <br>*必填*|项目负责人id|string|
|**Query**|**pointx**  <br>*必填*|项目定位x|number (double)|
|**Query**|**pointy**  <br>*必填*|项目定位y|number (double)|
|**Query**|**projectLogo**  <br>*必填*|项目logo|string|
|**Query**|**projectTitle**  <br>*必填*|项目标题|string|
|**Query**|**projectType**  <br>*必填*|项目类型 1-房建项目 2-市政项目 3-专业工程 4-其他|integer (int32)|
|**Query**|**scale**  <br>*必填*|建设规模 1 小型 2 中型 3 大型|string (byte)|
|**Query**|**status**  <br>*必填*|状态：1-在建 2-完成 3-删除|string (byte)|


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[成功的请求](#e5ddf48022ae6d2b4c39915efc48e0f8)|
|**201**|Created|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `*/*`


##### HTTP请求示例

###### 请求 path
```
/updateProject
```


###### 请求 query
```
json :
{
  "aliasProjectTitle" : "string",
  "investAmount" : "string",
  "memberId" : "string",
  "pointx" : 0.0,
  "pointy" : 0.0,
  "projectLogo" : "string",
  "projectTitle" : "string",
  "projectType" : 0,
  "scale" : "string",
  "status" : "string"
}
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "code" : "string",
  "data" : "object",
  "message" : "string",
  "success" : false
}
```


<a name="basic-error-controller_resource"></a>
### Basic-error-controller
Basic Error Controller


<a name="errorhtmlusingpost"></a>
#### errorHtml
```
POST /error
```


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[ModelAndView](#modelandview)|
|**201**|Created|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `text/html`


##### HTTP请求示例

###### 请求 path
```
/error
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "empty" : true,
  "model" : "object",
  "modelMap" : {
    "string" : "object"
  },
  "reference" : true,
  "status" : "string",
  "view" : {
    "contentType" : "string"
  },
  "viewName" : "string"
}
```


<a name="errorhtmlusingget"></a>
#### errorHtml
```
GET /error
```


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[ModelAndView](#modelandview)|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `text/html`


##### HTTP请求示例

###### 请求 path
```
/error
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "empty" : true,
  "model" : "object",
  "modelMap" : {
    "string" : "object"
  },
  "reference" : true,
  "status" : "string",
  "view" : {
    "contentType" : "string"
  },
  "viewName" : "string"
}
```


<a name="errorhtmlusingput"></a>
#### errorHtml
```
PUT /error
```


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[ModelAndView](#modelandview)|
|**201**|Created|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `text/html`


##### HTTP请求示例

###### 请求 path
```
/error
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "empty" : true,
  "model" : "object",
  "modelMap" : {
    "string" : "object"
  },
  "reference" : true,
  "status" : "string",
  "view" : {
    "contentType" : "string"
  },
  "viewName" : "string"
}
```


<a name="errorhtmlusingdelete"></a>
#### errorHtml
```
DELETE /error
```


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[ModelAndView](#modelandview)|
|**204**|No Content|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|


##### 消耗

* `application/json`


##### 生成

* `text/html`


##### HTTP请求示例

###### 请求 path
```
/error
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "empty" : true,
  "model" : "object",
  "modelMap" : {
    "string" : "object"
  },
  "reference" : true,
  "status" : "string",
  "view" : {
    "contentType" : "string"
  },
  "viewName" : "string"
}
```


<a name="errorhtmlusingpatch"></a>
#### errorHtml
```
PATCH /error
```


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[ModelAndView](#modelandview)|
|**204**|No Content|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|


##### 消耗

* `application/json`


##### 生成

* `text/html`


##### HTTP请求示例

###### 请求 path
```
/error
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "empty" : true,
  "model" : "object",
  "modelMap" : {
    "string" : "object"
  },
  "reference" : true,
  "status" : "string",
  "view" : {
    "contentType" : "string"
  },
  "viewName" : "string"
}
```


<a name="errorhtmlusinghead"></a>
#### errorHtml
```
HEAD /error
```


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[ModelAndView](#modelandview)|
|**204**|No Content|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|


##### 消耗

* `application/json`


##### 生成

* `text/html`


##### HTTP请求示例

###### 请求 path
```
/error
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "empty" : true,
  "model" : "object",
  "modelMap" : {
    "string" : "object"
  },
  "reference" : true,
  "status" : "string",
  "view" : {
    "contentType" : "string"
  },
  "viewName" : "string"
}
```


<a name="errorhtmlusingoptions"></a>
#### errorHtml
```
OPTIONS /error
```


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[ModelAndView](#modelandview)|
|**204**|No Content|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|


##### 消耗

* `application/json`


##### 生成

* `text/html`


##### HTTP请求示例

###### 请求 path
```
/error
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "empty" : true,
  "model" : "object",
  "modelMap" : {
    "string" : "object"
  },
  "reference" : true,
  "status" : "string",
  "view" : {
    "contentType" : "string"
  },
  "viewName" : "string"
}
```


<a name="log-controller_resource"></a>
### Log-controller
日志接口


<a name="getlogusingpost"></a>
#### 获取日志内容
```
POST /logDetail
```


##### 参数

|类型|名称|说明|类型|
|---|---|---|---|
|**Query**|**agentId**  <br>*必填*|代理商id|integer (int32)|
|**Query**|**operationType**  <br>*必填*|操作类型：0 代理商管理 1 产品管理 2 代理商企业管理 3 代理商项目管理 4 产品授权|integer (int32)|
|**Query**|**operationTypeDetail**  <br>*可选*|操作详细类型：0 新增 1 更新 2 删除|integer (int32)|


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[成功的请求«List«日志信息»»](#602e8fea19a78acc968bf0cf3a308097)|
|**201**|Created|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `*/*`


##### HTTP请求示例

###### 请求 path
```
/logDetail
```


###### 请求 query
```
json :
{
  "agentId" : 0,
  "operationType" : 0,
  "operationTypeDetail" : 0
}
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "code" : "string",
  "data" : [ {
    "id" : "主键",
    "operateUserId" : "操作人",
    "operateUserName" : "操作人姓名",
    "operationCompanyId" : "被操作企业",
    "operationCompanyName" : "被操作企业名称",
    "operationProjectId" : "被操作项目id",
    "operationProjectName" : "被操作项目名称",
    "operationRemark" : "日志备注",
    "operationType" : "0 代理商管理 1 产品管理 2 代理商企业管理 3 代理商项目管理 4 产品授权",
    "operationTypeDetail" : "操作详细类型：0 新增 1 更新 2 删除",
    "timestampCreate" : "创建时间",
    "timestampModify" : "修改时间"
  } ],
  "message" : "string",
  "success" : false
}
```


<a name="product-authenticate-controller_resource"></a>
### Product-authenticate-controller
产品授权


<a name="listagentproductsusingpost"></a>
#### 获取代理商产品列表
```
POST /listAgentProducts
```


##### 参数

|类型|名称|说明|类型|
|---|---|---|---|
|**Body**|**agentId**  <br>*可选*|代理商id|integer (int32)|


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[成功的请求«List«产品类型»»](#a3590e4473e0c901c62cb639f4fba99d)|
|**201**|Created|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `*/*`


##### HTTP请求示例

###### 请求 path
```
/listAgentProducts
```


###### 请求 body
```
json :
{ }
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "code" : "string",
  "data" : [ {
    "authorizingQuantity" : "授权数量",
    "authorizingUnusedQuantity" : "未使用授权数量",
    "authorizingUsageQuantity" : "已使用授权数量",
    "productId" : "产品id",
    "productName" : "授权产品名称",
    "productType" : "产品类型：0 企业级 1 项目级"
  } ],
  "message" : "string",
  "success" : false
}
```


<a name="listproductsusingpost"></a>
#### 获取所有产品列表
```
POST /listProducts
```


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[成功的请求«List«产品类型»»](#a3590e4473e0c901c62cb639f4fba99d)|
|**201**|Created|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `*/*`


##### HTTP请求示例

###### 请求 path
```
/listProducts
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "code" : "string",
  "data" : [ {
    "authorizingQuantity" : "授权数量",
    "authorizingUnusedQuantity" : "未使用授权数量",
    "authorizingUsageQuantity" : "已使用授权数量",
    "productId" : "产品id",
    "productName" : "授权产品名称",
    "productType" : "产品类型：0 企业级 1 项目级"
  } ],
  "message" : "string",
  "success" : false
}
```


<a name="productdetailusingpost"></a>
#### 获取产品的详情内容
```
POST /productDetail
```


##### 参数

|类型|名称|说明|类型|
|---|---|---|---|
|**Body**|**productId**  <br>*可选*|产品id|integer (int32)|


##### 响应

|HTTP代码|说明|类型|
|---|---|---|
|**200**|OK|[成功的请求«产品详情»](#f1761d32df15a3f2447e460c01bbd6c0)|
|**201**|Created|无内容|
|**401**|Unauthorized|无内容|
|**403**|Forbidden|无内容|
|**404**|Not Found|无内容|


##### 消耗

* `application/json`


##### 生成

* `*/*`


##### HTTP请求示例

###### 请求 path
```
/productDetail
```


###### 请求 body
```
json :
{ }
```


##### HTTP响应示例

###### 响应 200
```
json :
{
  "code" : "string",
  "data" : {
    "applications" : "应用名称",
    "productName" : "产品名称"
  },
  "message" : "string",
  "success" : false
}
```



