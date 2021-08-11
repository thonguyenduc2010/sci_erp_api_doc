
***1.3 Danh sách dịch vụ***
----
  Danh sách tất cả dịch vụ của thương hiệu, công ty
* **URL**

    
   `GET` Lấy danh sách dịch vụ `/{domain}/api/v1/services`

   `GET` Lấy chi tiết dịch vụ theo ID `/{domain}/api/v1/services/{id}`


* **Method:**

  
    `GET`

* **Url Params**


  | Attribute| Type | Description |
  |---|---|---|
  | id | string  | Danh sách dịch vụ của ID |
  | brand | boolean  | Có/Không lọc theo thương hiệu |


* **Success Response:**
    * **Code:** 200 <br />
    * **Content:**
    ```
    {
	    "error": 0,
	    "message": "Success",
	    "count": 5,
	    "data": [
		{
		    "id": 67871,
		    "default_code": "CSDA01",
		    "name": "Spa - chăm sóc da cơ bản",
		    "type": "service"
		},
		{
		    "id": 67872,
		    "default_code": "CSDA02",
		    "name": "Spa - chăm sóc da nâng cao",
		    "type": "service"
		},
		{
		    "id": 67873,
		    "default_code": "CSDA03",
		    "name": "Spa - chăm sóc da chuyên sâu",
		    "type": "service"
		},
		{
		    "id": 67874,
		    "default_code": "CSDA04",
		    "name": "Spa - chăm sóc da toàn phần\n(cơ bản + nâng cao + chuyên sâu) ",
		    "type": "service"
		},
		{
		    "id": 67875,
		    "default_code": "CSDA05",
		    "name": "Spa - chăm sóc da toàn phần - Ngắn hạn\n(cơ bản + nâng cao + chuyên sâu) ",
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

url = "{domain}/api/v1/services"

querystring = {"limit":"5","offset":"0"}

headers = {
    'access-token': "access_token_f328d1320ea7760339380651038eb224f4d531d3",
    'content-type': "application/x-www-form-urlencoded",
    'charset': "utf-8",
    'cache-control': "no-cache",
    'postman-token': "8c6993a6-4487-c5d6-3246-93c1c813aeb8"
    }

response = requests.request("GET", url, headers=headers, params=querystring)

print(response.text)
```

* **Notes:**
