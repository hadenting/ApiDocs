
## 1 - 查询账户所有资产

**请求URL：** 
- ` /api/asset `
  
**请求方式：**
- POST 

**参数：** 

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|access_key |是  |string |   |
|nonce |是  |string |     |
|signature     |是  |string |     |

 **返回示例**

``` 
  {
    "code": 200,
    "data": [
        {
            "currency_mark": "BTC",
            "count": "0.00000000",
            "num": "0.00000000",
            "forzen_num": "0.00000000"
        },
        {
            "currency_mark": "BCC",
            "count": "0.00000000",
            "num": "0.00000000",
            "forzen_num": "0.00000000"
        }
    ]
}
```

 **返回参数说明** 

|参数名|类型|说明|
|:-----  |:-----|-----                           |
|currency_mark |string   |币名称  |
|count |string   |总余额  |
|num |string   |可用余额  |
|forzen_num |string   |冻结余额  |



## 2 - 查询挂单

**请求URL：** 
- ` /api/trade_list `
  
**请求方式：**
- POST 

**参数：** 

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|access_key |是  |string |   |
|nonce |是  |string |     |
|signature     |是  |string |     |
|start_time |否  |time |开始时间 时间戳   |
|end_time |否  |time | 结束时间 时间戳    |
|currency_id     |否  |string | 币种ID   |
|trade_currency_id    |否  |string | 锚定币种ID   |
|type     |否  |string | 买入/卖出 值为：sell/buy    |
|page_index     |否  |int | 页码，默认为1，每页20条固定数据    |

 **返回示例**

``` 
{
    "code": 200,
    "data": [
        {
            "orders_id": "1241",
            "cy_mark": "EOS_BTC",
            "price": "0.02400000",
            "num": "9.00000000",
            "type": "buy",
            "add_time": "1526016306",
            "trade_num": "0.00000000",
            "status": "0"
        }
    ]
}
```

 **返回参数说明** 

|参数名|类型|说明|
|:-----  |:-----|-----                           |
|orders_id |int   |订单ID  |
|cy_mark |string   |名称  |
|price |float   |价格  |
|trade_num |float   |成交数量  |
|num |float   |数量  |
|type |string   |买/卖  |
|add_time |time   |时间  |
|status |int   |状态 0 挂单中 1 部分成交 2 完全成交 -1 已撤销  |


## 3 - 撤销挂单

**请求URL：** 
- ` /api/cancel_trade `
  
**请求方式：**
- POST 

**参数：** 

|参数名|必选|类型|说明|
|:----    |:---|:----- |-----   |
|access_key |是  |string |   |
|nonce |是  |string |     |
|signature     |是  |string |     |
|orders_id |是  |int |订单ID   |


 **返回示例**

``` 
  {
    "code": 200,
    "message": "撤销成功"
}
```
