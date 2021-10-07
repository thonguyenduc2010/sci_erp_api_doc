*** Lấy thông tin thẻ thành viên của khách hàng***
----
  Trả về thông tin phần thưởng thẻ khách hàng của khách hàng
* **URL**

   /{domain}/api/v1/loyalty

* **Method:**
  
  `GET` 
  
*  **URL Params**

   /{domain}/api/v1/loyalty

   **Required:**
 
    | Tham số  | Tính bắt buộc  | Kiểu dữ liệu  | Mô tả  |
    |---|---|---|---|
    | phone | yes  | string  | Số điện thoại của khách hàng  |
    | phone_2 | no  | string  | Số điện thoại 2 của khách hàng  |
    | phone_3 | no  | string  | Số điện thoại 3 của khách hàng  |
    
    
   * **Success Response:**
  
  * **Code:** 200 <br />
    **Content:**
       ```
              {
                  "error": 0,
                  "message": "Success",
                  "count": 2,
                  "data": [
                      {
                          "reward_name": "test",
                          "stage": "Được sử dụng",
                          "expiration_date": "2021-09-09T15:36:33"
                      },
                      {
                          "reward_name": "test 2",
                          "stage": "Được sử dụng",
                          "expiration_date": "2021-09-09T15:36:33"
                      }
                  ]
              }
       ```
       
    * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`


* **Sample Call:**



* **Notes:**
