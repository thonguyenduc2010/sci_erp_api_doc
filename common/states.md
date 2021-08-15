
***Danh sách Tỉnh thành***
----

* **URL**

  /{domain}/api/v1/states

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
                "id": 1384,
                "name": "bình định",
                "code": "77"
            },
            {
                "id": 1080,
                "name": "Lai Châu",
                "code": "VN-01"
            },
            {
                "id": 1079,
                "name": "Lào Cai",
                "code": "VN-02"
            },
            {
                "id": 1069,
                "name": "Hà Giang",
                "code": "VN-03"
            },
            {
                "id": 1055,
                "name": "Cao Bằng",
                "code": "VN-04"
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
  CURLOPT_URL => "https://scisoftware.xyz/api/v1/states?country_id=241&limit=5&offset=0",
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
    "postman-token: 765803d1-42e2-fb25-ecb9-17b1421799d0"
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

