
***1.5 Danh bảng giá***
----

* **URL**

    /{domain}/api/v1/price-list

* **Method:**

    `GET`

* **Url Params**



* **Phản hồi thành công:**
    * **Code:** 200 <br />
    * **Content:**
    ```
    {
        "error": 0,
        "message": "Success",
        "count": 1,
        "data": [
            {
                "id": 12,
                "name": "Bảng giá niêm yết Paris 2021",
                "brand_id": [
                    3,
                    "Paris"
                ],
                "start_date": false,
                "end_date": false,
                "type": "service"
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

url = "{domain}/api/v1/price-list"

headers = {
    'access-token': "access_token_f328d1320ea7760339380651038eb224f4d531d3",
    'content-type': "application/x-www-form-urlencoded",
    'charset': "utf-8",
    'cache-control': "no-cache",
    'postman-token': "1547a3c4-a39d-3979-59bb-6aabb209b78d"
    }

response = requests.request("GET", url, headers=headers)

print(response.text)
```

* **Notes:**

