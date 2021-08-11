
***1.4 Danh sách khuyến mại***
----

* **URL**
    /{domain}/api/v1/promotion
  
* **Method:**

    `GET`

* **Url Params**

* **Success Response:**
  
  * **Code:** 200 <br />
    **Content:** 
    ```
    {
    "error": 0,
    "message": "Success",
    "count": 28,
    "data": [
        {
            "id": 23,
            "code": "HH",
            "name": "BỆNH VIỆN HỒNG HÀ"
        },
        {
            "id": 2,
            "code": "HN",
            "name": "BỆNH VIỆN KANGNAM HÀ NỘI"
        },
        {
            "id": 3,
            "code": "HCM",
            "name": "BỆNH VIỆN KANGNAM HỒ CHÍ MINH"
        },
        {
            "id": 4,
            "code": "SG",
            "name": "BỆNH VIỆN KANGNAM SÀI GÒN"
        },
        {
            "id": 12,
            "code": false,
            "name": "BỆNH VIỆN THẨM MỸ ĐÔNG Á HỒ CHÍ MINH"
        },
        {
            "id": 25,
            "code": false,
            "name": "HỌC VIỆN THẨM MỸ SCI HÀ NỘI"
        },
        {
            "id": 24,
            "code": false,
            "name": "HỌC VIỆN THẨM MỸ SCI HỒ CHÍ MINH"
        },
        {
            "id": 18,
            "code": false,
            "name": "NHA KHOA PARIS 3/2"
        },
        {
            "id": 22,
            "code": false,
            "name": "NHA KHOA PARIS BÌNH DƯƠNG"
        },
        ...
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

