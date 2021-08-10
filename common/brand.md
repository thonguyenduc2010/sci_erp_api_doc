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
    **Content:** `{ error : "Log in" }`

  OR

  * **Code:** 422 UNPROCESSABLE ENTRY <br />
    **Content:** `{ error : "Email Invalid" }`

* **Sample Call:**

* **Notes:**


