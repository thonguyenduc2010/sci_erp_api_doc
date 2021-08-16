
***1.4 Danh sách khuyến mại***
----

* **URL**
    /{domain}/api/v1/promotion
  
* **Method:**

    `GET`

* **Url Params**
  | Attribute| Type | Description |
  |---|---|---|
  | id | string  | ID chương trình khuyến mại |


* **Success Response:**

    Kết quả trả về theo thương hiệu (Brand) của user gọi API
 
  * **Code:** 200 <br />
    **Content:** 
    ```
    {
    "error": 0,
    "message": "Success",
    "count": 5,
    "data": [
            {
                "id": 3194,
                "discount_program": [
                    75,
                    "CTKM NHA KHOA"
                ],
                "type_product": "product",
                "product_ids": [
                    63880,
                    63881,
                    63882,
                    63884,
                    63890,
                    63891
                ],
                "dc_min_qty": 1,
                "dc_max_qty": 7,
                "type_discount": "percent",
                "discount": 25
            },
            {
                "id": 3195,
                "discount_program": [
                    75,
                    "CTKM NHA KHOA"
                ],
                "type_product": "product",
                "product_ids": [
                    63880,
                    63881,
                    63882,
                    63884,
                    63890,
                    63891
                ],
                "dc_min_qty": 8,
                "dc_max_qty": 15,
                "type_discount": "percent",
                "discount": 30
            },
            {
                "id": 3196,
                "discount_program": [
                    75,
                    "CTKM NHA KHOA"
                ],
                "type_product": "product",
                "product_ids": [
                    63880,
                    63881,
                    63882,
                    63884,
                    63890
                ],
                "dc_min_qty": 16,
                "dc_max_qty": 99,
                "type_discount": "percent",
                "discount": 35
            },
            {
                "id": 3197,
                "discount_program": [
                    75,
                    "CTKM NHA KHOA"
                ],
                "type_product": "product",
                "product_ids": [
                    63886,
                    63887,
                    63888
                ],
                "dc_min_qty": 1,
                "dc_max_qty": 99,
                "type_discount": "percent",
                "discount": 45
            },
            {
                "id": 3198,
                "discount_program": [
                    75,
                    "CTKM NHA KHOA"
                ],
                "type_product": "product",
                "product_ids": [
                    63989
                ],
                "dc_min_qty": 1,
                "dc_max_qty": 1,
                "type_discount": "percent",
                "discount": 0
            }
        ]
    }
    ```
 
* **Error Response:**


  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** 
    ```
    {
      "type": "access_token",
      "message": "token seems to have expired or invalid"
    }

    ```

* **Sample Call:**
``` buildoutcfg
### Python Requests
import requests

url = "{domain}/api/v1/promotion"

querystring = {"limit":"5","offset":"0"}

headers = {
    'access-token': "access_token_f328d1320ea7760339380651038eb224f4d531d3",
    'content-type': "application/x-www-form-urlencoded",
    'charset': "utf-8",
    'cache-control': "no-cache",
    'postman-token': "4c30e765-eca8-8004-7f6f-177f466183f5"
    }

response = requests.request("GET", url, headers=headers, params=querystring)

print(response.text)
```

* **Notes:**

