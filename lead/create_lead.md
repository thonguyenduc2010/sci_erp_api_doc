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
    | customer_portrait | False | | | Chân dung khách hàng |
    
    ** customer_portrait
    | Attribute | Type  | Note | Description |
    |---|---|---| ---|
    | revenue_source | String | | Tài chính/ Thu nhập |
    | term_goals | String | | Mục tiêu |
    |social_influence | String | | Ảnh hưởng xã hội |
    | behavior_on_the_internet | String | | Hành vi trên Internet |
    | affected_by | String | ('family', 'Family'), ('friend', 'Friend'), ('co_worker', 'Co-Worker'), ('community', 'Community'), ('electronic_media', 'Electronic media'), ('other', 'Other') | Bị tác động bởi |
    | work_start_time | Float | | Giờ bắt đầu làm việc |
    | work_end_time | Float | | Giờ kết thúc làm việc |
    | break_start_time | Float | | Giờ bắt đầu nghỉ trưa |
    | break_end_time | Float | | Giờ kết thúc nghỉ trưa |
    | transport | String | ('bicycle', 'Bicycle'), ('scooter', 'Scooter'), ('bus', 'Bus'), ('car', 'Car'), ('other', 'Other') | Phương thức di chuyển |
    | pain_point | Mảng | VD: ['điểm đau 1', 'điểm đau 2'] | Điểm đau |
    | desires | Mảng | VD: ['mong muốn 1', 'mong muốn 2'] | Điểm đau |
    | hobby | Mảng | VD: ['sở thích 1', 'sở thích 2'] | Sở thích |
    

* **Success Response:**
  
  <_What should the status code be on success and is there any returned data? This is useful when people need to to know what their callbacks should expect!_>

  * **Code:** 200 <br />
    **Content:** 
    ```buildoutcfg 
         {
        "error": 0,
        "message": "Success",
        "data": {
            "customer_portrait": {
                "revenue_source": null,
                "term_goals": "test",
                "social_influence": "test",
                "behavior_on_the_internet": "test",
                "affected_by": "family",
                "work_start_time": 2.0,
                "work_end_time": 2.0,
                "break_start_time": 2.0,
                "break_end_time": 2.0,
                "transport": "bicycle",
                "hobby": [
                    "âm nhạc",
                    "xem phim"
                ],
                "pain_point": [
                    "point 1",
                    "point 2"
                ],
                "desires": [
                    "desires 1",
                    "desires 2"
                ]
            },
            "id_lead": 594142,
            "link_lead_detail": "http://localhost:13000/web#id=594142&model=crm.lead&view_type=form&action=630&menu_id=430"
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

