###### 签名规则事例
> 例：key=3 secret=5 storeid=4 timestamp=1606457285    
> signature = md5('3+4+5+1606457285')     
> 备注：无

###### 请求HOST
> http://yw.xiangzhuzhihui.com.cn

**1\. 查询房间内音箱状态**

###### 接口功能

> 查询房间内音箱状态

###### path

> /api/v1/robots/audio/checks

###### HTTP 请求方式

> post

###### 请求参数

> | 参数      | 必选 | 类型   | 说明                    |
> | :-------- | :--- | :----- | ----------------------- |
> | signature | ture | string | 签名。                  |
> | timestamp | true | int    | 时间戳。例：1606457285  |
> | hotelId   | true | string | 酒店 ID。例：1002 |
> | roomName  | true | string | 房间号。例：8501  |

###### 返回字段

> | 返回字段 | 字段类型 | 说明                             |
> | :------- | :------- | :------------------------------- |
> | code   | int      | 返回结果状态。  0  正常         |
> | msg  | string     | 返回信息                       |
> | data | bool      |   true:存在设备  false: 不存在设备 |

###### 接口示例


```javascript
{
    "code": 0,
    "msg": "success",
    "data": true
}
```

**2\. 查询房间内音箱状态并发送消息**

###### 接口功能

> 查询房间内音箱状态并发送消息

###### path

> /api/v1/robots/audio/sendmsg

###### HTTP 请求方式

> post

###### 请求参数

> | 参数      | 必选 | 类型   | 说明                    |
> | :-------- | :--- | :----- | ----------------------- |
> | signature | ture | string | 签名。                  |
> | timestamp | true | int    | 时间戳。例：1606457285  |
> | hotelId   | true | string | 酒店 ID。例：1002 |
> | roomName  | true | string | 房间号。例：8501  |
> | content   | false | string| 语音提示语。例：机器人已到房门外  |

###### 返回字段

> | 返回字段 | 字段类型 | 说明                             |
> | :------- | :------- | :------------------------------- |
> | code   | int      | 返回结果状态。  0  正常         |
> | msg  | string     | 返回信息                       |
> | data | bool      |   true:发送成功  false: 发送失败 |

###### 接口示例


```javascript
{
    "code": 0,
    "msg": "success",
    "data": true
}
```
