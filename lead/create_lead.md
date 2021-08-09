***Tạo Lead***
----
 Tạo Lead

* **URL**

  /{domain}/api/v1/lead

* **Method:**
  
  `POST`
  
*  **URL Params**

   /{domain}/api/v1/lead
    | Attribute  | Require  | Type  | Note | Description |
    |---|---|---|---| ---|
    | phone | True  | String  | | Số điện thoại của khách hàng |
    | contact_name | True | String | | Tên liên hệ của khách hàng |
    | gender | True | String | 'male' - Nam; 'female' - Nữ; 'other' - Khác | Giới tính của khách hàng |
    | type | True | Sting | 'lead' - Tiềm năng | Loại bản ghi là Lead |
    | year_of_birth | True | String | | Năm sinh của khách hàng |
    | country_id | True | Int | | Quốc gia |
    | state_id | True | Int | | Tỉnh/ Thành phố |
    | street | True | String | | Địa chỉ chi tiết của khách hàng |
    | stage_id | True | Int | | Giai đoạn |
    | brand_id | True | Int | | Thương hiệu |
    | company_id | True | Int | | Công ty |
    | price_list_id | True | Int | | Bảng giá |
    | category_source_id | True | Int | | Nhóm nguồn |
    | source_id | True | Int | | Nguồn |
    | campaign_id | True | Int | | Chiến dịch | 
    | crm_line_ids | True | Mảng | [ <br/> { <br/> 'service_id': id, <br/> 'quantity': Int, <br/> 'source_extend_id': id, <br/> }, <br/> ] <br/> - service_id: Sản phẩm <br/>- quantity: Số lượng <br/>- source_extend_id: Nguồn mở rộng  | Danh sách sản phẩm |
    | mobile | False | String| | Di động |
    | birth_date | False | Date | | Ngày sinh |
    | pass_port | False | String | | Chứng minh nhân dân |
    | email_from | False | String | | Email |
    | facebook_acc | False | String | | Tài khoản facebook |
    | type_data | False | String | 'old' - Cũ; 'new' - Mới | Kiểu dữ liệu |
    | re_open | False | Boolean | | Mở lại |
    | check_booking | False | Boolean | | Check booking |
    | medium_id | False | Int | | Kênh trung gian |
    | fam_ids | False | Mảng | [ <br/> { <br/> 'phone': String, <br/> 'member_name': String, <br/> 'type_relation_id': id, <br/> }, <br/> ] <br/> - phone: Số đi thoại <br/>- member_name: Họ và tên <br/>- type_relation_id: Mối quan hệ | Thông tin người thân |
    | note | False | Text | | Ghi chú |
    | special_note | False | Text | | Ghi chú đặc biệt |
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
