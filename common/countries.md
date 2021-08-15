
***Danh sách quốc gia***
----

* **URL**

  /{domain}/api/v1/countries

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
        "count": 5,
        "data": [
            {
                "id": 238,
                "name": "Venezuela",
                "code": "VE"
            },
            {
                "id": 239,
                "name": "Virgin Islands (British)",
                "code": "VG"
            },
            {
                "id": 240,
                "name": "Virgin Islands (USA)",
                "code": "VI"
            },
            {
                "id": 241,
                "name": "Việt Nam",
                "code": "VN"
            },
            {
                "id": 231,
                "name": "Vương Quốc Anh Thống Nhất",
                "code": "GB"
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
```
<?php

$curl = curl_init();

curl_setopt_array($curl, array(
  CURLOPT_URL => "https://scisoftware.xyz/api/v1/countries?limit=5&offset=225",
  CURLOPT_RETURNTRANSFER => true,
  CURLOPT_ENCODING => "",
  CURLOPT_MAXREDIRS => 10,
  CURLOPT_TIMEOUT => 30,
  CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
  CURLOPT_CUSTOMREQUEST => "GET",
  CURLOPT_HTTPHEADER => array(
    "access-token: access_token_ed1b96f45973e9195d7072672a655ae86e32ae2c",
    "cache-control: no-cache",
    "charset: utf-8",
    "content-type: application/x-www-form-urlencoded",
    "postman-token: bf1a7a2a-a2de-8207-2af9-8077e73fcf53"
  ),
));

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
  echo "cURL Error #:" . $err;
} else {
  echo $response;
}
```
* **Notes:**

