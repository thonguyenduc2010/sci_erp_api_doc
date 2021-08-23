***Cập nhật Booking***
----
 Cập nhật thông tin Lead

* **URL**

  /{domain}/api/v1/booking/{id}

* **Method:**
  
  `PUT`
  
*  BODY

   /{domain}/api/v1/lead/{id}
      | Attribute  | Require  | Type  | Note | Description |
    |---|---|---|---| ---|
    | phone | True  | String  | | Số điện thoại của khách hàng |
    | contact_name | True | String | | Tên liên hệ của khách hàng |
    | gender | True | String | 'male' - Nam; 'female' - Nữ; 'other' - Khác | Giới tính của khách hàng |
    | country_id | True | Int | | Quốc gia |
    | state_id | True | Int | | Tỉnh/ Thành phố |
    | district_id | False | Int | | Quận/ Huyện |
    | street | True | String | | Địa chỉ chi tiết của khách hàng |
    | stage_id | True | Int | | Trạng thái |
    | brand_id | True | Int | | Thương hiệu |
    | company_id | True | Int | | Công ty |
    | price_list_id | True | Int | | Bảng giá |
    | category_source_id | True | Int | | Nhóm nguồn |
    | source_id | True | Int | | Nguồn |
    | campaign_id | True | Int | | Chiến dịch | 
    | crm_line_ids | True | Mảng | | Danh sách sản phẩm |
    | mobile | False | String| | Di động |
    | birth_date | False | Date | %Y-%m-%d | Ngày sinh |
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
    
    - Đối với crm_line_ids, khi cập nhật cần có id line dịch vụ và kiểu update
    - Bảng mã update dịch vụ:
     
     | Kiểu update  | Mã  | Ghi chú  | Ví dụ |
    |---|---|---|---|
    | Xoá | 0 | - Khi xoá dịch vụ bắt buộc có id của line dịch vụ | [{'id': id_line ,'type_update': 0,}] |
    | Sửa | 1 | - Khi cập nhật thông tin trên line dịch vụ bắt buộc có: id line dịch vụ và id dịch vụ; cùng các thông tin thay đổi | [{‘id’: id_line,'service_id': id_service,'type_update': 1, 'quantity': 3,}]|
    | Thêm | 2 | - Khi thêm line dịch vụ mới bắt buộc có: id dịch vụ thêm mới; cùng các thông tin liên quan | [{‘service_id': id_service,'type_update': 2, 'quantity': 4,'source_extend_id': id_source}] |
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
        "crm_line_ids": [
            {
                "id": 21515,
                "service_id": 5562,
                "service_name": "Combo Chỉnh hàm hô móm 2 hàm + Trượt cằm",
                "quantity": 1,
                "source_extend_id": 1,
                "source_extend_name": "Search engine",
                "total_before_discount": 150000000.0,
                "total_after_discount": 0
            },
            {
                "id": 21516,
                "service_id": 2282,
                "service_name": "Xóa hình xăm có sẹo  - Mức 10 (>700cm) (Giá tính trên hình)",
                "quantity": 1,
                "source_extend_id": 1,
                "source_extend_name": "Search engine",
                "total_before_discount": 70000000.0,
                "total_after_discount": 0
            }
        ]
    }
 
* **Error Response:**

  <_Most endpoints will have many ways they can fail. From unauthorized access, to wrongful parameters etc. All of those should be liste d here. It might seem repetitive, but it helps prevent assumptions from being made where they should be._>

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`

  OR

  * **Code:** 422 UNPROCESSABLE ENTRY <br />
    **Content:** `{ error : "Email Invalid" }`

* **Sample Call:**

  <_Just a sample call to your endpoint in a runnable format ($.ajax call or a curl request) - this makes life easier and more predictable._> 

* **Notes:**

  <_This is where all uncertainties, commentary, discussion etc. can go. I recommend timestamping and identifying oneself when leaving comments here._> 
