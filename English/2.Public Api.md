# Interface documentation V1

Following interface HOST： `www.9coin.com`

Access address is：https://{host}/{url}

Example：https://www.9coin.com/home/api/currency

# 1 - Query all coins

**Request URL：** 
- ` /api/currency `
  
**Request Way：**
- GET 

 **Example**

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

 **Parameter Instructions** 

|Parameter Name |Type|Instructions|
|:-----  |:-----|-----                           |
|currency_id |string   |currency ID  |
|currency_mark |string   |currency Name  |


    

# 2 - Query all exchange pairs

**Request URL：** 
- ` /api/cy_mark_list `
  
**Request Way：**
- GET 

 **Example**

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
 **Parameter Instructions** 

|Parameter Name |Type|Instructions|
|:-----  |:-----|-----                           |
|cy_id |string   |unique identification of each exchange pair |
|cy_mark |string   |unique identification of each exchange pair  |



    
# 3 - Query real time quotes

**Request URL：** 
- ` /api/tickers `
  
**Request Way：**
- GET
 
 **Example**

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

 **Parameter Instructions** 

|Parameter Name |Type|Instructions|
|:-----  |:-----|-----|
|cy_mark |string   |Name  |
|buy_one_price |string   |Buy One Price  |
|sell_one_price |string   |Sell One Price   |
|new_price |string   |New Price  |
|24H_max_price |string   |highest price (24h)  |
|24H_min_price |string   |lowest price (24h)  |
|24H_done_money |string   |total exchange amount (24h)  |


 

# 4 - Query buy orders quotes（40 Number）

**Request URL：** 
- ` /api/buy `
  
**Request Way：**
- POST 

 **Parameter** 

|Parameter Name |Required|Type|Instructions|
|:----    |:---|:----- |-----   |
|cy_id |yes  |string |   |


 **Example** 

``` 
  {
    "code": 200,
    "data": [
        {
            "wtlnum": "2497496.0104",
            "price": "1.00000000"
        },
        {
            "wtlnum": "36.0000",
            "price": "0.02650000"
        },
        {
            "wtlnum": "42.0000",
            "price": "0.02600000"
        },
        {
            "wtlnum": "95093097.3119",
            "price": "0.02000000"
        }
    ]
}
```

 **Parameter Instructions** 

|Parameter Name |Type|Instructions|
|:-----  |:-----|-----                           |
|wtlnum |float   | number |
|price |float   |price  |


# 5 - Query sell orders quotes（40 Number）

**Request URL：** 
- ` /api/sell `
  
**Request Way：**
- POST 

 **Parameter ** 

|Parameter Name |Required|Type|Instructions|
|:----    |:---|:----- |-----   |
|cy_id |yes  |string |   |


 **Example**

``` 
  {
    "code": 200,
    "data": [
        {
            "wtlnum": "2497496.0104",
            "price": "1.00000000"
        },
        {
            "wtlnum": "36.0000",
            "price": "0.02650000"
        },
        {
            "wtlnum": "42.0000",
            "price": "0.02600000"
        },
        {
            "wtlnum": "95093097.3119",
            "price": "0.02000000"
        }
    ]
}
```

 **Parameter Instructions** 

|Parameter Name |Type|Instructions|
|:-----  |:-----|-----                           |
|wtlnum |float   | number |
|price |float   |price  |


# 6 - Query near orders quotes（80 Number）

**Request URL：** 
- ` /api/orders `
  
**Request Way：**
- POST 

 **Parameter** 

|Parameter Name |Required|Type|Instructions|
|:----    |:---|:----- |-----   |
|cy_id |是  |string |交易对ID   |

 **Example** 

``` 
{
    "code": 200,
    "data": [
        {
            "trade_no": "T1525656643",
            "num": "1.8950",
            "price": "0.026576",
            "type": "buy",
            "add_time": "1525656643"
        },
        {
            "trade_no": "T1525656621",
            "num": "2.0361",
            "price": "0.026567",
            "type": "sell",
            "add_time": "1525656621"
        }
    ]
}
```

 **Parameter Instructions** 

|Parameter Name |Type|Instructions|
|:-----  |:-----|-----                           |
|trade_no |string   |trade no  |
|num |float   |number  |
|price |float   |price  |
|add_time |time   |trade time  |

