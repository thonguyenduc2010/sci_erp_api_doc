***Cập nhật Lead***
----
 Cập nhật thông tin Lead

* **URL**

  /{domain}/api/v1/lead/{id}

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
    | crm_line_ids | True | Mảng |  | Danh sách sản phẩm |
    | mobile | False | String| | Di động |
    | birth_date | False | Date | %Y-%m-%d | Ngày sinh |
    | email_from | False | String | | Email |
    | facebook_acc | False | String | | Tài khoản facebook |
    | zalo_acc| False | String | | Tàik khoản Zalo |
    | send_info_facebook | False | String | no' - Không; 'yes' - Có | Gửi thông tin Facebook |
    | send_info_zalo | False | String | no' - Không; 'yes' - Có | Gửi thông tin Zalo |
    | overseas_vietnamese | False | String | 'no' - No; 'marketing' - Marketing - Overseas Vietnamese; 'branch' - Branch - Overseas Vietnamese | Việt kiều |
    | work_online | False | String | 'no' - Không; 'yes' - Có | Làm việc online |
    | online_counseling | False | String | 'no' - Không; 'yes' - Có | Tư vấn trực tuyến |
    | shuttle_bus | False | String | 'no' - Không; 'yes' - Có | Xe đưa đón |
    |   |   |   |   |   |
    
    - Đối với crm_line_ids, khi cập nhật cần có id line dịch vụ và kiểu update
    - Bảng mã update dịch vụ:
     *
     | Kiểu update  | Mã  | Ghi chú  | Ví dụ |
    |---|---|---|---|
    | Xoá | 0 | - Khi xoá dịch vụ bắt buộc có id của line dịch vụ | [{'id': id_line ,'type_update': 0,}] |
    | Sửa | 1 | - Khi cập nhật thông tin trên line dịch vụ bắt buộc có: id line dịch vụ và id dịch vụ; cùng các thông tin thay đổi | [{‘id’: id_line,'service_id': id_service,'type_update': 1, 'quantity': 3,}]|
    | Thêm | 2 | - Khi thêm line dịch vụ mới bắt buộc có: id dịch vụ thêm mới; cùng các thông tin liên quan | [{‘service_id': id_service,'type_update': 2, 'quantity': 4,'source_extend_id': id_source}] |
    |   |   |   |   |   |

* **Success Response:**
  
  <_What should the status code be on success and is there any returned data? This is useful when people need to to know what their callbacks should expect!_>

  * **Code:** 200 <br />
    **Content:** `{ id : 12,
    date: '2001-08-01'
    }`
 
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
