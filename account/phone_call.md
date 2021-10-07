***Lấy thông tin danh sách phone call của khách hàng***
----
  Trả về danh sách các bản ghi phone call của khách hàng
* **URL**

   /{domain}/api/v1/phones-call

* **Method:**
  
  `GET` 
  
*  **URL Params**

   /{domain}/api/v1/phones-call

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
      "count": 2,
      "data": [
          {
              "id": 3335,
              "name": "Nhắc Lịch Tái Khám Sau 1 Tuần",
              "type_crm_id": "Chăm sóc sau dịch vụ",
              "stage_id": "No process",
              "support_rating": false,
              "call_date": "2021-10-05 00:00:00"
          },
          {
              "id": 3336,
              "name": "Nhắc Lịch Tái Khám lần 2_sau 6 tháng",
              "type_crm_id": "Chăm sóc sau dịch vụ",
              "stage_id": "No process",
              "support_rating": false,
              "call_date": "2022-03-28 00:00:00"
          }
      ]
  }
   ```
   
   * **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`


* **Sample Call:**



* **Notes:**
