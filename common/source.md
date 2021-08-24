***1.13 Danh sách Nguồn***
----
  Danh sách tất cả Nguồn dùng cho bản ghi Lead và Booking

* **URL**

  /{domain}/api/v1/source

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
        "count": 3,
        "data": [
            {
                "id": 6,
                "name": "Marketing - TikTok/Viber/Zalo/livechat",
                "category_id": 3,
                "category_name": "DVKH"
            },
            {
                "id": 7,
                "name": "Marketing - Hotline",
                "category_id": 1,
                "category_name": "MARKETING"
            },
            {
                "id": 8,
                "name": "Marketing - Youtube",
                "category_id": 1,
                "category_name": "MARKETING"
            },
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


* **Notes:**
