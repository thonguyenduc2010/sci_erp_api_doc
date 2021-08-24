***1.12 Danh sách Nhóm nguồn***
----
  Danh sách tất cả Nhóm nguồn dùng cho bản ghi Lead và Booking

* **URL**

  /{domain}/api/v1/source-category

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
        "count": 6,
        "data": [
            {
                "id": 1,
                "name": "MARKETING"
            },
            {
                "id": 2,
                "name": "TRADE MKT"
            },
            {
                "id": 3,
                "name": "DVKH"
            },
            {
                "id": 4,
                "name": "CHI NHÁNH"
            },
            {
                "id": 5,
                "name": "BP KINHDOANH"
            },
            {
                "id": 6,
                "name": "Tuyen dung"
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


* **Notes:**
