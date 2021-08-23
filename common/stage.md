***1.11 Danh sách Trạng thái***
----
  Danh sách tất cả trạng thái của bản ghi Lead và Booking

* **URL**

  /{domain}/api/v1/stage

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
              "id": 27,
              "name": "Không hài lòng"
          },
          {
              "id": 6,
              "name": "Re-open"
          },
          {
              "id": 8,
              "name": "Potential"
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


