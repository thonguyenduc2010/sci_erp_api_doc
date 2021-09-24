***Tạo Lead***
----
 Tạo Lead

* **URL**

  /{domain}/api/v1/lead

* **Method:**
  
  `POST`
  
*  **BODY Params**

   /{domain}/api/v1/lead
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
    | online_counseling | False | String | 'no' - Không; 'yes' - Có | Tư vấn trực tuyến |
    | shuttle_bus | False | String | 'no' - Không; 'yes' - Có | Xe đưa đón |
    | customer_portrait | False | | Chân dung khách hàng |
    |   |   |   |   |   |

* **Success Response:**
  
  <_What should the status code be on success and is there any returned data? This is useful when people need to to know what their callbacks should expect!_>

  * **Code:** 200 <br />
    **Content:** 
    ```buildoutcfg 
    {
    "error": 0,
    "message": "Success",
    "data": {
        "id": 818635,
        "name": "Nguyễn Văn A",
        "contact_name": "Nguyễn Văn A",
        "gender": "male",
        "pass_port": false,
        "phone": "0123456789",
        "mobile": "0123456789",
        "birth_date": "1999-06-02",
        "year_of_birth": "1999",
        "email_from": "sondoan026@gmail.com",
        "country_id": 1,
        "country_name": "Andorra",
        "state_id": 7,
        "state_name": "Victoria",
        "district_id": false,
        "district_name": false,
        "street": "11 Tô Vĩnh Diện",
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
        "campaign_id": 21,
        "campaign_name": "sss",
        "amount_total": 220000000.0,
        "create_on": "23-08-2021 03:13:48",
         "crm_line_ids": [1,2,3]
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

