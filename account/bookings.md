***Lấy thông tin danh sách booking của khách hàng***
----
  Trả về danh sách các bản ghi booking của khách hàng
* **URL**

   /{domain}/api/v1/bookings

* **Method:**
  
  `GET` 
  
*  **URL Params**

   /{domain}/api/v1/bookings

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
            "id": 594414,
            "name": "BOOK-211006-00011",
            "stage": "Not confirm",
            "create_on": "2021-10-06 07:03:54",
            "effect": "Hiệu lực",
            "link_detail": "http://localhost:13000/web#id=594414&model=crm.lead&view_type=form&action=633&menu_id=430",
            "company_id": [
                2,
                "BỆNH VIỆN TM KANGNAM HÀ NỘI"
            ]
        },
        {
            "id": 594412,
            "name": "BOOK-211006-00010",
            "stage": "Cancel",
            "create_on": "2021-10-06 07:03:10",
            "effect": "Hết hiệu lực",
            "link_detail": "http://localhost:13000/web#id=594412&model=crm.lead&view_type=form&action=633&menu_id=430",
            "company_id": [
                2,
                "BỆNH VIỆN TM KANGNAM HÀ NỘI"
            ]
        },
        {
            "id": 594410,
            "name": "BOOK-211006-00009",
            "stage": "Cancel",
            "create_on": "2021-10-06 07:02:39",
            "effect": "Hết hiệu lực",
            "link_detail": "http://localhost:13000/web#id=594410&model=crm.lead&view_type=form&action=633&menu_id=430",
            "company_id": [
                2,
                "BỆNH VIỆN TM KANGNAM HÀ NỘI"
            ]
        },
        {
            "id": 594408,
            "name": "BOOK-211006-00008",
            "stage": "Cancel",
            "create_on": "2021-10-06 07:02:11",
            "effect": "Hết hiệu lực",
            "link_detail": "http://localhost:13000/web#id=594408&model=crm.lead&view_type=form&action=633&menu_id=430",
            "company_id": [
                2,
                "BỆNH VIỆN TM KANGNAM HÀ NỘI"
            ]
        },
        {
            "id": 594406,
            "name": "BOOK-211006-00007",
            "stage": "Cancel",
            "create_on": "2021-10-06 06:57:41",
            "effect": "Hết hiệu lực",
            "link_detail": "http://localhost:13000/web#id=594406&model=crm.lead&view_type=form&action=633&menu_id=430",
            "company_id": [
                2,
                "BỆNH VIỆN TM KANGNAM HÀ NỘI"
            ]
        },
        {
            "id": 594404,
            "name": "BOOK-211006-00006",
            "stage": "Cancel",
            "create_on": "2021-10-06 06:57:18",
            "effect": "Hết hiệu lực",
            "link_detail": "http://localhost:13000/web#id=594404&model=crm.lead&view_type=form&action=633&menu_id=430",
            "company_id": [
                2,
                "BỆNH VIỆN TM KANGNAM HÀ NỘI"
            ]
        },
        {
            "id": 594402,
            "name": "BOOK-211006-00005",
            "stage": "Cancel",
            "create_on": "2021-10-06 06:56:44",
            "effect": "Hết hiệu lực",
            "link_detail": "http://localhost:13000/web#id=594402&model=crm.lead&view_type=form&action=633&menu_id=430",
            "company_id": [
                2,
                "BỆNH VIỆN TM KANGNAM HÀ NỘI"
            ]
        },
        {
            "id": 594400,
            "name": "BOOK-211006-00004",
            "stage": "Cancel",
            "create_on": "2021-10-06 06:56:17",
            "effect": "Hết hiệu lực",
            "link_detail": "http://localhost:13000/web#id=594400&model=crm.lead&view_type=form&action=633&menu_id=430",
            "company_id": [
                2,
                "BỆNH VIỆN TM KANGNAM HÀ NỘI"
            ]
        },
        {
            "id": 594398,
            "name": "BOOK-211006-00003",
            "stage": "Cancel",
            "create_on": "2021-10-06 06:55:40",
            "effect": "Hết hiệu lực",
            "link_detail": "http://localhost:13000/web#id=594398&model=crm.lead&view_type=form&action=633&menu_id=430",
            "company_id": [
                2,
                "BỆNH VIỆN TM KANGNAM HÀ NỘI"
            ]
        },
        {
            "id": 594396,
            "name": "BOOK-211006-00002",
            "stage": "Cancel",
            "create_on": "2021-10-06 06:54:57",
            "effect": "Hết hiệu lực",
            "link_detail": "http://localhost:13000/web#id=594396&model=crm.lead&view_type=form&action=633&menu_id=430",
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
