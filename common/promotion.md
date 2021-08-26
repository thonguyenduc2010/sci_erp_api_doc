
***1.4 Chương trình khuyến mại***
Lấy danh sách chương trình khuyến mại theo thương hiệu và chi nhánh.
----

* **URL**
    /{domain}/api/v1/promotion
  
* **Method:**

    `GET`

* **Url Params**
  | Attribute| Type | Description |
  |---|---|---|
  | company_id | int  | ID chi nhánh |


* **Success Response:**

    Kết quả trả về theo thương hiệu (Brand) của user gọi API
 
  * **Code:** 200 <br />
    **Content:** 
    ```
   "error": 0,
    "message": "Success",
    "count": 4,
    "data": [
        {
            "id": 63,
            "code": "CTKM_KN_ALL_20217_1",
            "name": "CTKM Tháng 7",
            "campaign": [
                {
                    "id": 32,
                    "name": "Test CTKM"
                }
            ],
            "brand": [
                {
                    "id": 1,
                    "name": "Kangnam"
                }
            ],
            "company": []
        },
        {
            "id": 64,
            "code": "CTKM_KN_ALL_20217_2",
            "name": "KN - ĐẸP CHẤT HÀN QUỐC",
            "campaign": [
                {
                    "id": 21,
                    "name": "Tháng triển khai CRM"
                }
            ],
            "brand": [
                {
                    "id": 1,
                    "name": "Kangnam"
                }
            ],
            "company": []
        },
        {
            "id": 65,
            "code": "CTKM_KN_ALL_20217_4",
            "name": "CTKM Test 001",
            "campaign": [
                {
                    "id": 21,
                    "name": "Tháng triển khai CRM"
                }
            ],
            "brand": [
                {
                    "id": 1,
                    "name": "Kangnam"
                }
            ],
            "company": []
        },
        {
            "id": 67,
            "code": "CTKM_KN_ALL_20217_4",
            "name": "CTKM ĐẸP CHẤT HÀN QUỐC LẦN 4",
            "campaign": [
                {
                    "id": 32,
                    "name": "Test CTKM"
                }
            ],
            "brand": [
                {
                    "id": 1,
                    "name": "Kangnam"
                }
            ],
            "company": []
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

