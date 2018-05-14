# Interface documentation

The following interface HOST: `www.9coin.com`

Visit address: https://{host}/{url}

Example: https://www.9coin.com/home/api/currency

# 1 - Available currencies

**Request URL:**
- ` /api/currency `

**Request method:**
- GET

**Return example**

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

**Return parameter description**

|Parameter name|Type|Description|
|:----- |:-----|----- |
|currency_id |int |Currency ID |
|currency_mark |string |Currency Name |


   # 2 - Available Trade Pairs

**Request URL:**
- ` /api/cy_mark_list `

**Request method:**
- GET

**Return example**

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

**Return parameter description**

|Parameter name|Type|Description|
|:----- |:-----|----- |
|cy_id |int |Trade pair ID |
|cy_mark |string |Trade pair name |

   # 3 - Latest Quotes

**Request URL:**
- ` /api/tickers `

**Request method:**
- GET

**Return example**

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

**Return parameter description**

|Parameter name|Type|Description|
|:----- |:-----|----- |
|cy_mark |string |Trade pair name |
|buy_one_price |float |Buy one price |
|sell_one_price |float | sell one price |
|new_price |float |Newest price |
|24H_max_price |float | 24 hours maximum price |
|24H_min_price |float |24 hours minimum price |
|24H_done_money |float |24 hours trading volume |

 # 4 - Market Depth, Buy (return to 40 items)

**Request URL:**
- ` /api/buy `

**Request method:**
- POST

**Parameters:**

|Parameter name|Required|Type|Description|
|:---- |:---|:----- |----- |
|cy_id |Yes |int | Trade Pair ID |


**Return example**

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

**Return parameter description**

|Parameter name|Type|Description|
|:----- |:-----|----- |
|wtlnum |float | Quantity |
|price |float |price |

# 5 - Market Depth, Selling (returns 40 items)

**Request URL:**
- ` /api/sell `

**Request method:**
- POST

**Parameters:**

|Parameter name|Required|Type|Description|
|:---- |:---|:----- |----- |
|cy_id |Yes |int | Trade Pair ID |


**Return example**

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

**Return parameter description**

|Parameter name|Type|Description|
|:----- |:-----|----- |
|wtlnum |float | Quantity |
|price |float |price |

# 6 - Closest Market Move (returns 80 messages)

**Request URL:**
- ` /api/orders `

**Request method:**
- POST

**Parameters:**

|Parameter name|Required|Type|Description|
|:---- |:---|:----- |----- |
|cy_id |Yes |int |Trade Pair ID |

**Return example**

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

**Return parameter description**

|Parameter name|Type|Description|
|:----- |:-----|----- |
|trade_no |string | transaction number |
|num |float |Quantity |
|price |float |price |
|add_time |time | Trading hours |
