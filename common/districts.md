
***Danh sách quận huyện***
----

* **URL**

  /{domain}/api/v1/districts

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
        "count": 0,
        "data": []
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
    CURLOPT_URL => "https://scisoftware.xyz/api/v1/districts?state_id=1070",
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
      "postman-token: 3e3adef0-a612-d3b1-a36f-abc9853f3c37"
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
