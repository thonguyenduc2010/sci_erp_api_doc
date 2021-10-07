***Lấy thông tin danh sách phiếu khám của khách hàng***
----
  Trả về danh sách các bản ghi phiếu khám của khách hàng
* **URL**

   /{domain}/api/v1/walkin

* **Method:**
  
  `GET` 
  
*  **URL Params**

   /{domain}/api/v1/walkin

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
        "count": 1,
        "data": [
            {
                "id": 1652,
                "name": "PK-2021-000592",
                "date": "2021-09-29",
                "department_id": 563,
                "department_name": "Phòng Khám Răng Hàm Mặt",
                "services": [
                    "Mão toàn sứ Emax Zic"
                ],
                "link_detail": "http://localhost:13000/web#id=1652&model=sh.medical.appointment.register.walkin&view_type=form&action=819&menu_id=535"
            }
        ]
    }
   ```
   
   
   * **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`


* **Sample Call:**



* **Notes:**
