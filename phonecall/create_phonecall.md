
*** Tạo Phonecall ***
----
 Tạo Phonecall

* **URL**

  /{domain}/api/v1/phone-call

* **Method:**
  
  `POST`
  
*  **URL Params**

    | Attribute  | Require  | Type  | Note | Description |
    |---|---|---|---| ---|
    | phone | True  | String  | | Số điện thoại của khách hàng |
    | type_phonecall | True | Int | Sử dụng API lấy danh sách loại phone call | Loại phone call |
    | direction | True | Stirng | 'in' - Gọi vào; 'out' - Gọi ra | Hướng gọi |
    | contact_name | True | String | | Tên liên hệ |
    | stage_id | True | String | Sử dụng API lấy danh sách trạng thái | Trạng thái |
    | company_id | True | Int | Sử dụng API lấy danh sách cơ sở | Cơ sở |
    | country_id | False | Int | | Quốc gia |
    | state_id | False | Int | | Tỉnh/ Thành phố |
    | street | True | String | | Địa chỉ chi tiết của khách hàng |
    | booking_date | True | Date | %Y-%m-%d | Ngày hẹn lịch |
* **Success Response:**
  
  * **Code:** 200 <br />
    **Content:**
      ```buildoutcfg 
    {
    "error": 0,
    "message": "Success",
    "data": {
        "id_phonecall": 14464,
        "link_phonecall_detail": "http://localhost:13000/web#id=14464&model=crm.phone.call&view_type=form&action=713&menu_id=511"
    }
}
 
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

