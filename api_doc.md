# 接口文档 V1

以下接口HOST： `www.9coin.com`

访问地址为：https://{host}/{url}

例：https://www.9coin.com/home/api/currency

# 1 - 可用货币

**请求URL：** 
- ` /api/currency `
  
**请求方式：**
- GET 

 **返回示例**

``` 
{
    "code": 200,
    "data": [
        {
            "currency_id": "37",
            "currency_mark": "ETH"
        },
        {
            "currency_id": "39",
            "currency_mark": "ETC"
        },
    ]
}
```

 **返回参数说明** 

|参数名|类型|说明|
|:-----  |:-----|-----                           |
|currency_id |int   |货币ID  |
|currency_mark |int   |货币名称  |


    

# 2 - 可用交易对

**请求URL：** 
- ` /api/cy_mark_list `
  
**请求方式：**
- GET 

 **返回示例**

``` 
{
    "code": 200,
    "data": [
        {
            "cy_id": "60",
            "cy_mark": "SKY_BTC"
        },
        {
            "cy_id": "61",
            "cy_mark": "SKY_EHT"
        },
        {
            "cy_id": "27",
            "cy_mark": "ETH_BTC"
        }
    ]
}
```

 **返回参数说明** 

|参数名|类型|说明|
|:-----  |:-----|-----                           |
|cy_id |int   |交易对ID  |
|cy_mark |int   |交易对名称  |



    
# 3 - 最新行情

**请求URL：** 
- ` /api/tickers `
  
**请求方式：**
- GET
 
 **返回示例**

``` 
{
    "code": 200,
    "data": [
        {
            "cy_mark": "SKY_BTC",
            "buy_one_price": "0.02650000",
            "sell_one_price": "0.02650000",
            "new_price": "0.00223100",
            "24H_max_price": "0.002879",
            "24H_min_price": "0.002879",
            "24H_done_money": "2415.12"
        }
    ]
}
```

 **返回参数说明** 

|参数名|类型|说明|
|:-----  |:-----|-----                           |
|cy_mark |int   |交易对名称  |
|buy_one_price |int   |买一价格  |
|sell_one_price |int   |卖一价格  |
|new_price |int   |最新价格  |
|24H_max_price |int   |24小时最高价  |
|24H_min_price |int   |24小时最低价  |
|24H_done_money |int   |24小时交易量  |


