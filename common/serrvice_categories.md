
***1.4 Danh sách nhóm dịch vụ ***

----

* **URL**
    /{domain}/api/v1/service_categories
***Lấy danh sách nhóm dịch vụ theo thương hiệu.***
* **Method:**

    `GET`
    
* **Success Response:**

    Kết quả trả về theo thương hiệu (Brand) của user gọi API
 
  * **Code:** 200 <br />
    **Content:** 
```
{
    "error": 0,
    "message": "Success",
    "count": 4,
    "data": [
        {
            "id": 63,
            "name": "CTKM Tháng 7",
        },
        {
            "id": 64,
            "name": "KN - ĐẸP CHẤT HÀN QUỐC",
        },
        {
            "id": 65,
            "name": "CTKM Test 001",
        },
        {
            "id": 67,
            "name": "CTKM ĐẸP CHẤT HÀN QUỐC LẦN 4",
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

url = "{domain}/api/v1/service_categories"

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
