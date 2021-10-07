***Lấy thông tin danh sách case khiếu nại của khách hàng***
----
  Trả về danh sách các bản ghi case khiếu nại của khách hàng
* **URL**

   /{domain}/api/v1/cases

* **Method:**
  
  `GET` 
  
*  **URL Params**

   /{domain}/api/v1/cases

   **Required:**
 
    | Tham số  | Tính bắt buộc  | Kiểu dữ liệu  | Mô tả  |
    |---|---|---|---|
    | phone | yes  | string  | Số điện thoại của khách hàng  |
    | phone_2 | no  | string  | Số điện thoại 2 của khách hàng  |
    | phone_3 | no  | string  | Số điện thoại 3 của khách hàng  |
    | offset | no | Int | Số bản ghi cần bỏ qua, mặc định bằng 0 |
    | limit | no | Int | Số lượng bản ghi tối đa để trả về, mặc định bằng 10 |
    
    
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
                  "id": 6,
                  "name": "test",
                  "code": "CAS-000006",
                  "user_id": [
                      351,
                      "Admin KN"
                  ],
                  "create_on": "2021-10-06 10:51:52"
              },
              {
                  "id": 7,
                  "name": "test",
                  "code": "CAS-000007",
                  "user_id": [
                      351,
                      "Admin KN"
                  ],
                  "create_on": "2021-10-06 10:51:52"
              },
              {
                  "id": 8,
                  "name": "test",
                  "code": "CAS-000008",
                  "user_id": [
                      351,
                      "Admin KN"
                  ],
                  "create_on": "2021-10-06 10:51:52"
              },
              {
                  "id": 9,
                  "name": "test",
                  "code": "CAS-000009",
                  "user_id": [
                      351,
                      "Admin KN"
                  ],
                  "create_on": "2021-10-06 10:51:52"
              },
              {
                  "id": 10,
                  "name": "test",
                  "code": "CAS-000010",
                  "user_id": [
                      351,
                      "Admin KN"
                  ],
                  "create_on": "2021-10-06 10:51:52"
              }
          ]
      }
   ```
   
    * **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`


* **Sample Call:**



* **Notes:**
