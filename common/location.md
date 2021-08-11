***1.2 Danh sách cơ sở***
----
  Danh sách tất cả cơ sở của công ty

* **URL**

  /{domain}/api/v1/location

* **Method:**

  `GET`
  
*  **URL Params**

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

url = "http://localhost:13000/api/v1/location"

headers = {
    'access-token': "access_token_f328d1320ea7760339380651038eb224f4d531d3",
    'content-type': "application/x-www-form-urlencoded",
    'charset': "utf-8",
    'cache-control': "no-cache",
    'postman-token': "e0056f3e-ce5e-3132-b138-44814da66faa"
    }

response = requests.request("GET", url, headers=headers)

print(response.text)
```

* **Notes:**


