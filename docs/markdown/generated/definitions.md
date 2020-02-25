
<a name="definitions"></a>
## 定义

<a name="agentstatistics"></a>
### AgentStatistics
代理商统计数据


|名称|说明|类型|
|---|---|---|
|**authenticatedQuantity**  <br>*可选*|认证的总数  <br>**样例** : `"认证的总数"`|integer (int32)|
|**currentYearOfAuthenticatedQuantity**  <br>*可选*|今年认证的总数  <br>**样例** : `"今年认证的总数"`|integer (int32)|


<a name="companyvo"></a>
### CompanyVo
企业信息


|名称|说明|类型|
|---|---|---|
|**address**  <br>*可选*|详细地址  <br>**样例** : `"详细地址"`|string|
|**administrator**  <br>*可选*|超级管理员姓名（通信证号）  <br>**样例** : `"超级管理员姓名（通信证号）"`|string|
|**companyId**  <br>*可选*|企业ID  <br>**样例** : `0`|integer (int32)|
|**companyName**  <br>*可选*|企业详细地址  <br>**样例** : `"企业详细地址"`|string|
|**companyType**  <br>*可选*|企业类型(1.专业分包2.设备分包3.材料分包4.后勤服务5.特殊设备6.劳务分包7.监理8.建设单位9.总承包单位10.勘察11.设计单位12.租赁13.其他)  <br>**模式** : `"^(?:[A-Za-z0-9+/]{4})*(?:[A-Za-z0-9+/]{2}==\|[A-Za-z0-9+/]{3}=)?$"`  <br>**样例** : `"企业类型(1.专业分包2.设备分包3.材料分包4.后勤服务5.特殊设备6.劳务分包7.监理8.建设单位9.总承包单位10.勘察11.设计单位12.租赁13.其他)"`|string (byte)|
|**contactsMobile**  <br>*可选*|联系人手机号  <br>**样例** : `"联系人手机号"`|string|
|**contactsName**  <br>*可选*|联系人姓名  <br>**样例** : `"联系人姓名"`|string|
|**createTime**  <br>*可选*|创建时间时间戳  <br>**样例** : `"创建时间时间戳"`|integer (int64)|
|**creater**  <br>*可选*|创建人  <br>**样例** : `"创建人"`|string|


<a name="modelandview"></a>
### ModelAndView

|名称|说明|类型|
|---|---|---|
|**empty**  <br>*可选*|**样例** : `true`|boolean|
|**model**  <br>*可选*|**样例** : `"object"`|object|
|**modelMap**  <br>*可选*|**样例** : `{<br>  "string" : "object"<br>}`|< string, object > map|
|**reference**  <br>*可选*|**样例** : `true`|boolean|
|**status**  <br>*可选*|**样例** : `"string"`|enum (100 CONTINUE, 101 SWITCHING_PROTOCOLS, 102 PROCESSING, 103 CHECKPOINT, 200 OK, 201 CREATED, 202 ACCEPTED, 203 NON_AUTHORITATIVE_INFORMATION, 204 NO_CONTENT, 205 RESET_CONTENT, 206 PARTIAL_CONTENT, 207 MULTI_STATUS, 208 ALREADY_REPORTED, 226 IM_USED, 300 MULTIPLE_CHOICES, 301 MOVED_PERMANENTLY, 302 FOUND, 302 MOVED_TEMPORARILY, 303 SEE_OTHER, 304 NOT_MODIFIED, 305 USE_PROXY, 307 TEMPORARY_REDIRECT, 308 PERMANENT_REDIRECT, 400 BAD_REQUEST, 401 UNAUTHORIZED, 402 PAYMENT_REQUIRED, 403 FORBIDDEN, 404 NOT_FOUND, 405 METHOD_NOT_ALLOWED, 406 NOT_ACCEPTABLE, 407 PROXY_AUTHENTICATION_REQUIRED, 408 REQUEST_TIMEOUT, 409 CONFLICT, 410 GONE, 411 LENGTH_REQUIRED, 412 PRECONDITION_FAILED, 413 PAYLOAD_TOO_LARGE, 413 REQUEST_ENTITY_TOO_LARGE, 414 URI_TOO_LONG, 414 REQUEST_URI_TOO_LONG, 415 UNSUPPORTED_MEDIA_TYPE, 416 REQUESTED_RANGE_NOT_SATISFIABLE, 417 EXPECTATION_FAILED, 418 I_AM_A_TEAPOT, 419 INSUFFICIENT_SPACE_ON_RESOURCE, 420 METHOD_FAILURE, 421 DESTINATION_LOCKED, 422 UNPROCESSABLE_ENTITY, 423 LOCKED, 424 FAILED_DEPENDENCY, 425 TOO_EARLY, 426 UPGRADE_REQUIRED, 428 PRECONDITION_REQUIRED, 429 TOO_MANY_REQUESTS, 431 REQUEST_HEADER_FIELDS_TOO_LARGE, 451 UNAVAILABLE_FOR_LEGAL_REASONS, 500 INTERNAL_SERVER_ERROR, 501 NOT_IMPLEMENTED, 502 BAD_GATEWAY, 503 SERVICE_UNAVAILABLE, 504 GATEWAY_TIMEOUT, 505 HTTP_VERSION_NOT_SUPPORTED, 506 VARIANT_ALSO_NEGOTIATES, 507 INSUFFICIENT_STORAGE, 508 LOOP_DETECTED, 509 BANDWIDTH_LIMIT_EXCEEDED, 510 NOT_EXTENDED, 511 NETWORK_AUTHENTICATION_REQUIRED)|
|**view**  <br>*可选*|**样例** : `"[view](#view)"`|[View](#view)|
|**viewName**  <br>*可选*|**样例** : `"string"`|string|


<a name="cf83d861019e9004281516764e8d49f3"></a>
### Pagination«CompanyVo»

|名称|说明|类型|
|---|---|---|
|**list**  <br>*可选*|结果列表  <br>**样例** : `"结果列表"`|< [CompanyVo](#companyvo) > array|
|**page**  <br>*可选*|页码  <br>**样例** : `"页码"`|integer (int32)|
|**size**  <br>*可选*|每页行数  <br>**样例** : `"每页行数"`|integer (int32)|
|**totalPage**  <br>*可选*|总页数  <br>**样例** : `"总页数"`|integer (int32)|
|**totalRows**  <br>*可选*|总行数  <br>**样例** : `"总行数"`|integer (int32)|


<a name="aa9228011fca81a766e8f09d3c41a6d9"></a>
### Pagination«ProjectVo»

|名称|说明|类型|
|---|---|---|
|**list**  <br>*可选*|结果列表  <br>**样例** : `"结果列表"`|< [ProjectVo](#projectvo) > array|
|**page**  <br>*可选*|页码  <br>**样例** : `"页码"`|integer (int32)|
|**size**  <br>*可选*|每页行数  <br>**样例** : `"每页行数"`|integer (int32)|
|**totalPage**  <br>*可选*|总页数  <br>**样例** : `"总页数"`|integer (int32)|
|**totalRows**  <br>*可选*|总行数  <br>**样例** : `"总行数"`|integer (int32)|


<a name="projectvo"></a>
### ProjectVo
项目信息


|名称|说明|类型|
|---|---|---|
|**address**  <br>*可选*|详细地址  <br>**样例** : `"详细地址"`|string|
|**company**  <br>*可选*|所属企业（企业id）  <br>**样例** : `"所属企业（企业id）"`|string|
|**createTime**  <br>*可选*|创建时间时间戳  <br>**样例** : `"创建时间时间戳"`|integer (int64)|
|**creater**  <br>*可选*|创建人  <br>**样例** : `"创建人"`|string|
|**manager**  <br>*可选*|项目负责人  <br>**样例** : `"项目负责人"`|string|
|**projectId**  <br>*可选*|项目ID  <br>**样例** : `"项目ID"`|integer (int32)|
|**projectName**  <br>*可选*|项目名称  <br>**样例** : `"项目名称"`|string|
|**projectType**  <br>*可选*|项目类型  <br>**样例** : `"项目类型"`|integer (int32)|


<a name="view"></a>
### View

|名称|说明|类型|
|---|---|---|
|**contentType**  <br>*可选*|**样例** : `"string"`|string|


<a name="2db97cae51db93261c6e984fac8cdb10"></a>
### 产品类型

|名称|说明|类型|
|---|---|---|
|**authorizingQuantity**  <br>*可选*|授权数量  <br>**样例** : `"授权数量"`|integer (int32)|
|**authorizingUnusedQuantity**  <br>*可选*|未使用授权数量  <br>**样例** : `"未使用授权数量"`|integer (int32)|
|**authorizingUsageQuantity**  <br>*可选*|已使用授权数量  <br>**样例** : `"已使用授权数量"`|integer (int32)|
|**productId**  <br>*可选*|产品id  <br>**样例** : `"产品id"`|integer (int32)|
|**productName**  <br>*可选*|授权产品名称  <br>**样例** : `"授权产品名称"`|string|
|**productType**  <br>*可选*|产品类型：0 企业级 1 项目级  <br>**样例** : `"产品类型：0 企业级 1 项目级"`|integer (int32)|


<a name="61644d1f73db59ff2efdbc0bf7bafb2e"></a>
### 产品详情

|名称|说明|类型|
|---|---|---|
|**applications**  <br>*可选*|应用名称  <br>**样例** : `"应用名称"`|< [应用](#5b0520a9bf5e8d87c0b8c6e58766e184) > array|
|**productName**  <br>*可选*|产品名称  <br>**样例** : `"产品名称"`|string|


<a name="5b0520a9bf5e8d87c0b8c6e58766e184"></a>
### 应用

|名称|说明|类型|
|---|---|---|
|**applicationId**  <br>*可选*|应用id  <br>**样例** : `"应用id"`|integer (int32)|
|**applicationName**  <br>*可选*|应用名称  <br>**样例** : `"应用名称"`|string|


<a name="e5ddf48022ae6d2b4c39915efc48e0f8"></a>
### 成功的请求

|名称|说明|类型|
|---|---|---|
|**code**  <br>*可选*|请求的状态码  <br>**样例** : `"string"`|string|
|**data**  <br>*可选*|请求返回的内容  <br>**样例** : `"object"`|object|
|**message**  <br>*可选*|请求的结果信息  <br>**样例** : `"string"`|string|
|**success**  <br>*可选*|请求是否成功  <br>**样例** : `false`|boolean|


<a name="ffe815d8bd31d2ab15eea9d2fa51e71c"></a>
### 成功的请求«AgentStatistics»

|名称|说明|类型|
|---|---|---|
|**code**  <br>*可选*|请求的状态码  <br>**样例** : `"string"`|string|
|**data**  <br>*可选*|请求返回的内容  <br>**样例** : `"[agentstatistics](#agentstatistics)"`|[AgentStatistics](#agentstatistics)|
|**message**  <br>*可选*|请求的结果信息  <br>**样例** : `"string"`|string|
|**success**  <br>*可选*|请求是否成功  <br>**样例** : `false`|boolean|


<a name="a3590e4473e0c901c62cb639f4fba99d"></a>
### 成功的请求«List«产品类型»»

|名称|说明|类型|
|---|---|---|
|**code**  <br>*可选*|请求的状态码  <br>**样例** : `"string"`|string|
|**data**  <br>*可选*|请求返回的内容  <br>**样例** : `[ "[2db97cae51db93261c6e984fac8cdb10](#2db97cae51db93261c6e984fac8cdb10)" ]`|< [产品类型](#2db97cae51db93261c6e984fac8cdb10) > array|
|**message**  <br>*可选*|请求的结果信息  <br>**样例** : `"string"`|string|
|**success**  <br>*可选*|请求是否成功  <br>**样例** : `false`|boolean|


<a name="602e8fea19a78acc968bf0cf3a308097"></a>
### 成功的请求«List«日志信息»»

|名称|说明|类型|
|---|---|---|
|**code**  <br>*可选*|请求的状态码  <br>**样例** : `"string"`|string|
|**data**  <br>*可选*|请求返回的内容  <br>**样例** : `[ "[b27fb728413ba88b74d026f485b39d5f](#b27fb728413ba88b74d026f485b39d5f)" ]`|< [日志信息](#b27fb728413ba88b74d026f485b39d5f) > array|
|**message**  <br>*可选*|请求的结果信息  <br>**样例** : `"string"`|string|
|**success**  <br>*可选*|请求是否成功  <br>**样例** : `false`|boolean|


<a name="a69fad129a99ca29233d74c1293f9e76"></a>
### 成功的请求«Pagination«CompanyVo»»

|名称|说明|类型|
|---|---|---|
|**code**  <br>*可选*|请求的状态码  <br>**样例** : `"string"`|string|
|**data**  <br>*可选*|请求返回的内容  <br>**样例** : `"[cf83d861019e9004281516764e8d49f3](#cf83d861019e9004281516764e8d49f3)"`|[Pagination«CompanyVo»](#cf83d861019e9004281516764e8d49f3)|
|**message**  <br>*可选*|请求的结果信息  <br>**样例** : `"string"`|string|
|**success**  <br>*可选*|请求是否成功  <br>**样例** : `false`|boolean|


<a name="6b37d272121b46efe207fa6e17b2fb09"></a>
### 成功的请求«Pagination«ProjectVo»»

|名称|说明|类型|
|---|---|---|
|**code**  <br>*可选*|请求的状态码  <br>**样例** : `"string"`|string|
|**data**  <br>*可选*|请求返回的内容  <br>**样例** : `"[aa9228011fca81a766e8f09d3c41a6d9](#aa9228011fca81a766e8f09d3c41a6d9)"`|[Pagination«ProjectVo»](#aa9228011fca81a766e8f09d3c41a6d9)|
|**message**  <br>*可选*|请求的结果信息  <br>**样例** : `"string"`|string|
|**success**  <br>*可选*|请求是否成功  <br>**样例** : `false`|boolean|


<a name="f1761d32df15a3f2447e460c01bbd6c0"></a>
### 成功的请求«产品详情»

|名称|说明|类型|
|---|---|---|
|**code**  <br>*可选*|请求的状态码  <br>**样例** : `"string"`|string|
|**data**  <br>*可选*|请求返回的内容  <br>**样例** : `"[61644d1f73db59ff2efdbc0bf7bafb2e](#61644d1f73db59ff2efdbc0bf7bafb2e)"`|[产品详情](#61644d1f73db59ff2efdbc0bf7bafb2e)|
|**message**  <br>*可选*|请求的结果信息  <br>**样例** : `"string"`|string|
|**success**  <br>*可选*|请求是否成功  <br>**样例** : `false`|boolean|


<a name="b27fb728413ba88b74d026f485b39d5f"></a>
### 日志信息

|名称|说明|类型|
|---|---|---|
|**id**  <br>*可选*|主键  <br>**样例** : `"主键"`|integer (int32)|
|**operateUserId**  <br>*可选*|操作人  <br>**样例** : `"操作人"`|string|
|**operateUserName**  <br>*可选*|操作人姓名  <br>**样例** : `"操作人姓名"`|string|
|**operationCompanyId**  <br>*可选*|被操作企业  <br>**样例** : `"被操作企业"`|integer (int32)|
|**operationCompanyName**  <br>*可选*|被操作企业名称  <br>**样例** : `"被操作企业名称"`|string|
|**operationProjectId**  <br>*可选*|被操作项目id  <br>**样例** : `"被操作项目id"`|integer (int32)|
|**operationProjectName**  <br>*可选*|被操作项目名称  <br>**样例** : `"被操作项目名称"`|string|
|**operationRemark**  <br>*可选*|日志备注  <br>**样例** : `"日志备注"`|string|
|**operationType**  <br>*可选*|0 代理商管理 1 产品管理 2 代理商企业管理 3 代理商项目管理 4 产品授权  <br>**模式** : `"^(?:[A-Za-z0-9+/]{4})*(?:[A-Za-z0-9+/]{2}==\|[A-Za-z0-9+/]{3}=)?$"`  <br>**样例** : `"0 代理商管理 1 产品管理 2 代理商企业管理 3 代理商项目管理 4 产品授权"`|string (byte)|
|**operationTypeDetail**  <br>*可选*|操作详细类型：0 新增 1 更新 2 删除  <br>**模式** : `"^(?:[A-Za-z0-9+/]{4})*(?:[A-Za-z0-9+/]{2}==\|[A-Za-z0-9+/]{3}=)?$"`  <br>**样例** : `"操作详细类型：0 新增 1 更新 2 删除"`|string (byte)|
|**timestampCreate**  <br>*可选*|创建时间  <br>**样例** : `"创建时间"`|integer (int64)|
|**timestampModify**  <br>*可选*|修改时间  <br>**样例** : `"修改时间"`|integer (int64)|



