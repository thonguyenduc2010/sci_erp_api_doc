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
    | phone_no1 | True  | String  | sử dụng khi khách hàng chưa có account | Số điện thoại của khách hàng |
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
    | email_from | False | String | | Email |
    | facebook_acc | False | String | | Tài khoản facebook |
    | zalo_acc| False | String | | Tàik khoản Zalo |
    | send_info_facebook | False | String | 'not_send' - Chưa gửi; 'sent' - Đã gửi | Gửi thông tin Facebook |
    | send_info_zalo | False | String | 'no_acc' - Chưa có acc; 'not_response' - Đã gửi và chưa phản hồi; 'sent' - Đã phản hồi | Gửi thông tin Zalo |
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
    "count": 39,
    "data": {
        "id": 818801,
        "link_booking_detail": "http://localhost:13000/web#id=818801&model=crm.lead&view_type=form&action=631&menu_id=430",
        "name": "Book-687724",
        "contact_name": "Sơn",
        "gender": "male",
        "pass_port": false,
        "phone": false,
        "mobile": false,
        "birth_date": false,
        "year_of_birth": false,
        "email_from": "sondoan_026",
        "country_id": 1,
        "country_name": "Andorra",
        "state_id": 1,
        "state_name": "Australian Capital Territory",
        "district_id": false,
        "district_name": false,
        "street": false,
        "company_id": 2,
        "company_name": "BỆNH VIỆN KANGNAM HÀ NỘI",
        "facebook_acc": "abc",
        "send_info_facebook": "sent",
        "zalo_acc": "1111",
        "send_info_zalo": "sent",
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
        "amount_total": 0.0,
        "create_on": "2021-08-31T04:00:53",
        "crm_line_ids": [
            {
                "id": 21724,
                "service_id": 2046,
                "service_name": "Giảm mỡ bụng toàn thể (Trên + Dưới + Eo) cân nặng từ 50-59 kg + Căng da mini (Sửa lại)",
                "quantity": 1,
                "source_extend_id": false,
                "source_extend_name": false
            },
            {
                "id": 21725,
                "service_id": 2047,
                "service_name": "Giảm mỡ bụng toàn thể (Trên + Dưới + Eo) cân nặng từ 60 - 70 kg + Căng da mini",
                "quantity": 1,
                "source_extend_id": false,
                "source_extend_name": false
            },
            {
                "id": 21726,
                "service_id": 2048,
                "service_name": "Giảm mỡ bụng toàn thể (Trên + Dưới + Eo) cân nặng từ 60 - 70 kg + Căng da mini (Sửa lại)",
                "quantity": 1,
                "source_extend_id": false,
                "source_extend_name": false
            }
        ]
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
