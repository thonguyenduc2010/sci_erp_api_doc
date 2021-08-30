***TẠO BOOKING***
----
 Tạo Booking

* **URL**

  /{domain}/api/v1/booking

* **Method:**
  
  `POST`
  
*  BODY

   /{domain}/api/v1/booking
    | Attribute  | Require  | Type  | Note | Description |
    |---|---|---|---| ---|
   | account_id | True  | Int  | trong trường hợp là khách hàng mơi chưa có account thì trường này sẽ để trống và phải điền số điện thoại của khách hàng đó vào trường phone | ID account của khách hàng bên ERP |
    | phone | True  | String  | sử dụng khi khách hàng chưa có account | Số điện thoại của khách hàng |
    | phone_no2 | False  | String  | | Số điện thoại 2 của khách hàng |
    | phone_no3 | False  | String  | | Số điện thoại 2 của khách hàng |
    | ticket_id | True | Int | | ID ticket |
    | agent_email | True | String | | Email agent |
    | user_id | True | Int | | người tạo |
    | contact_name | True | String | | Tên liên hệ của khách hàng |
    | gender | True | String | 'male' - Nam; 'female' - Nữ; 'other' - Khác | Giới tính của khách hàng |
    | country_id | True | Int | | Quốc gia |
    | state_id | True | Int | | Tỉnh/ Thành phố |
    | district_id | False | Int | | Quận/ Huyện |
    | street | True | String | | Địa chỉ chi tiết của khách hàng |
    | company_id | True | Int | | Công ty |
    | price_list_id | True | Int | | Bảng giá |
    | category_source_id | True | Int | | Nhóm nguồn |
    | source_id | True | Int | | Nguồn |
    | campaign_id | True | Int | | Chiến dịch | 
    | crm_line_ids | True | Mảng | Mảng id các dịch vụ | Danh sách sản phẩm |
    | birth_date | False | Date | %Y-%m-%d | Ngày sinh |
    | year_of_birth | False | String | | Năm sinh |
    | email_from | False | String | | Email |
    | facebook_acc | False | String | | Tài khoản facebook |
    | zalo_acc| False | String | | Tàik khoản Zalo |
    | send_info_facebook | False | String | no' - Không; 'yes' - Có | Gửi thông tin Facebook |
    | send_info_zalo | False | String | no' - Không; 'yes' - Có | Gửi thông tin Zalo |
    | overseas_vietnamese | False | String | 'no' - No; 'marketing' - Marketing - Overseas Vietnamese; 'branch' - Branch - Overseas Vietnamese | Việt kiều |
    | work_online | False | Stringg | 'no' - Không; 'yes' - Có | Làm việc online |
    | booking_date | True | Date | %Y-%m-%d | Ngày hẹn lịch |
    | online_counseling | False | String | 'no' - Không; 'yes' - Có | Tư vấn trực tuyến |
    | shuttle_bus | False | String | 'no' - Không; 'yes' - Có | Xe đưa đón |
    |   |   |   |   |   |
    
    
* **Success Response:**

  * **Code:** 200 <br />
    **Content:**
     ```buildoutcfg 
    {
    "error": 0,
    "message": "Success",
    "data": {
        "id": 818637,
        "name": "Book-687631",
        "contact_name": "Nguyễn Văn A",
        "gender": "male",
        "pass_port": false,
        "phone": "012345691111",
        "mobile": "01234567890",
        "birth_date": false,
        "year_of_birth": false,
        "email_from": "test@gmail.com",
        "country_id": 1,
        "country_name": "Andorra",
        "state_id": 1,
        "state_name": "Australian Capital Territory",
        "district_id": false,
        "district_name": false,
        "street": false,
        "company_id": 2,
        "company_name": "BỆNH VIỆN KANGNAM HÀ NỘI",
        "facebook_acc": "Nguyễn Văn A",
        "send_info_facebook": false,
        "zalo_acc": "0123456789",
        "send_info_zalo": false,
        "brand_id": 1,
        "brand_name": "Kangnam",
        "price_list_id": 1,
        "price_list_name": "Bảng giá niêm yết Kangnam 2021",
        "category_source_id": 1,
        "category_source_name": "MARKETING",
        "overseas_vietnamese": "no",
        "work_online": "no",
        "online_counseling": "no",
        "shuttle_bus": "no",
        "campaign_id": 22,
        "campaign_name": "aaa",
        "amount_total": 220000000.0,
        "create_on": "23-08-2021 08:37:28",
        "booking_date": "23-08-2021 00:00:00",
        "crm_line_ids": [1,2,3]
    }
 
* **Error Response:**
    - Đối với khách hàng có Booking còn hiệu lực thì không được phép tạo mới Booking cho khách hàng đó và phải vào Booking vẫn còn hiệu lực đó để thao tác tiếp

    **Code:** 401 UNAUTHORIZED <br />
    **Content:**
    ```buildoutcfg 
    {
    "type": "Không thể tạo Booking mới do còn Booking vẫn còn hiêu lực",
    "message": "Hãy vào Booking có mã Book-687631 của thương hiệu Kangnam để thao tác tiếp"}
    
 OR <br/>
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
