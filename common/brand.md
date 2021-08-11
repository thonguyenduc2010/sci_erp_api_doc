***1.1. Danh sách thương hiệu***
----
  Danh sách tất cả thương hiệu

* **URL**

  /{domain}/api/v1/brand

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
          "count": 7,
          "data": [
              {
                  "id": 1,
                  "code": "KN",
                  "name": "Kangnam"
              },
              {
                  "id": 2,
                  "code": "DA",
                  "name": "Đông Á"
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
```
import requests

url = "{domain}/api/v1/brand"

headers = {
    'access-token': "access_token_f328d1320ea7760339380651038eb224f4d531d3",
    'content-type': "application/x-www-form-urlencoded",
    'charset': "utf-8",
    'cache-control': "no-cache",
    'postman-token': "674c962f-280d-1916-da80-3c0d6199e73f"
    }

response = requests.request("GET", url, headers=headers)

print(response.text)
```
* **Notes:**


