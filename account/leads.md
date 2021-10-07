***Lấy thông tin danh sách lead của khách hàng***
----
  Trả về danh sách các bản ghi lead của khách hàng
* **URL**

   /{domain}/api/v1/leads

* **Method:**
  
  `GET` 
  
*  **URL Params**

   /{domain}/api/v1/leads

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
          "count": 10,
          "data": [
              {
                  "id": 594413,
                  "name": "MIMI111",
                  "stage": "Booking",
                  "create_on": "2021-10-06 07:03:49",
                  "link_detail": "http://localhost:13000/web#id=594413&model=crm.lead&view_type=form&action=630&menu_id=430",
                  "company_id": [
                      2,
                      "BỆNH VIỆN TM KANGNAM HÀ NỘI"
                  ]
              },
              {
                  "id": 594411,
                  "name": "MIMI111",
                  "stage": "Booking",
                  "create_on": "2021-10-06 07:03:04",
                  "link_detail": "http://localhost:13000/web#id=594411&model=crm.lead&view_type=form&action=630&menu_id=430",
                  "company_id": [
                      2,
                      "BỆNH VIỆN TM KANGNAM HÀ NỘI"
                  ]
              },
              {
                  "id": 594409,
                  "name": "MIMI111",
                  "stage": "Booking",
                  "create_on": "2021-10-06 07:02:32",
                  "link_detail": "http://localhost:13000/web#id=594409&model=crm.lead&view_type=form&action=630&menu_id=430",
                  "company_id": [
                      2,
                      "BỆNH VIỆN TM KANGNAM HÀ NỘI"
                  ]
              },
              {
                  "id": 594407,
                  "name": "MIMI111",
                  "stage": "Booking",
                  "create_on": "2021-10-06 07:02:05",
                  "link_detail": "http://localhost:13000/web#id=594407&model=crm.lead&view_type=form&action=630&menu_id=430",
                  "company_id": [
                      2,
                      "BỆNH VIỆN TM KANGNAM HÀ NỘI"
                  ]
              },
              {
                  "id": 594405,
                  "name": "MIMI111",
                  "stage": "Booking",
                  "create_on": "2021-10-06 06:57:35",
                  "link_detail": "http://localhost:13000/web#id=594405&model=crm.lead&view_type=form&action=630&menu_id=430",
                  "company_id": [
                      2,
                      "BỆNH VIỆN TM KANGNAM HÀ NỘI"
                  ]
              },
              {
                  "id": 594403,
                  "name": "MIMI111",
                  "stage": "Booking",
                  "create_on": "2021-10-06 06:57:07",
                  "link_detail": "http://localhost:13000/web#id=594403&model=crm.lead&view_type=form&action=630&menu_id=430",
                  "company_id": [
                      2,
                      "BỆNH VIỆN TM KANGNAM HÀ NỘI"
                  ]
              },
              {
                  "id": 594401,
                  "name": "MIMI111",
                  "stage": "Booking",
                  "create_on": "2021-10-06 06:56:39",
                  "link_detail": "http://localhost:13000/web#id=594401&model=crm.lead&view_type=form&action=630&menu_id=430",
                  "company_id": [
                      2,
                      "BỆNH VIỆN TM KANGNAM HÀ NỘI"
                  ]
              },
              {
                  "id": 594399,
                  "name": "MIMI111",
                  "stage": "Booking",
                  "create_on": "2021-10-06 06:56:11",
                  "link_detail": "http://localhost:13000/web#id=594399&model=crm.lead&view_type=form&action=630&menu_id=430",
                  "company_id": [
                      2,
                      "BỆNH VIỆN TM KANGNAM HÀ NỘI"
                  ]
              },
              {
                  "id": 594397,
                  "name": "MIMI111",
                  "stage": "Booking",
                  "create_on": "2021-10-06 06:55:32",
                  "link_detail": "http://localhost:13000/web#id=594397&model=crm.lead&view_type=form&action=630&menu_id=430",
                  "company_id": [
                      2,
                      "BỆNH VIỆN TM KANGNAM HÀ NỘI"
                  ]
              },
              {
                  "id": 594395,
                  "name": "MIMI111",
                  "stage": "Booking",
                  "create_on": "2021-10-06 06:54:50",
                  "link_detail": "http://localhost:13000/web#id=594395&model=crm.lead&view_type=form&action=630&menu_id=430",
                  "company_id": [
                      2,
                      "BỆNH VIỆN TM KANGNAM HÀ NỘI"
                  ]
              }
          ]
      }
   ```
   
   * **Error Response:**

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`


* **Sample Call:**



* **Notes:**
