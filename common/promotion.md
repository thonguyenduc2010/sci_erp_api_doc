
***1.3 Danh sách khuyến mại***
----

* **URL**

    `GET` Danh sách khuyến mại: 
    `/{domain}/api/v1/promotion`
  
    `GET` Danh sách khuyến mại theo ID: 
    `/{domain}/api/v1/promotion/<id>`
  
  
* **Method:**

    `GET`

* **Url Params**


  | Attribute| Type | Description |
  |---|---|---|
  | id | int  | ID chương trình khuyến mại |
  | brand | boolean  | Có/Không lọc theo thương hiệu |


* **Phản hồi thành công:**
    * **Code:** 200 <br />
    * **Content:** <br />
  
`GET` Danh sách khuyến mại: 
    `/{domain}/api/v1/promotion`
  
      
    "count": 2,
    "data": [
        {
            "id": 3194,
            "discount_program": [
                75,
                "CTKM NHA KHOA"
            ],
            "type_product": "product",
            "product_ids": [
                63880,
                63881,
                63882,
                63884,
                63890,
                63891
            ],
            "dc_min_qty": 1,
            "dc_max_qty": 7,
            "type_discount": "percent",
            "discount": 25.0
        },
        {
            "id": 3195,
            "discount_program": [
                75,
                "CTKM NHA KHOA"
            ],
            "type_product": "product",
            "product_ids": [
                63880,
                63881,
                63882,
                63884,
                63890,
                63891
            ],
            "dc_min_qty": 8,
            "dc_max_qty": 15,
            "type_discount": "percent",
            "discount": 30.0
        }
    ]
      
`GET` Chi tiết danh sách bảng giá theo ID: 
`/{domain}/api/v1/promotion/<id>`


     "count": 1,
    "data": [
        {
            "id": 3194,
            "discount_program": [
                75,
                "CTKM NHA KHOA"
            ],
            "check_switch": false,
            "brand_id": [
                3,
                "Paris"
            ],
            "index": 0,
            "used": false,
            "type_product": "product",
            "type_discount": "percent",
            "incremental": true,
            "gift": false,
            "product_ids": [
                63880,
                63881,
                63882,
                63884,
                63890,
                63891
            ],
            "product_ctg_ids": [],
            "product_ctg_id": false,
            "discount": 25.0,
            "dc_min_qty": 1,
            "dc_max_qty": 7,
            "required_combo": true,
            "discount_bonus": 0.0,
            "minimum_group": 0,
            "create_on": "2021-07-28T02:20:22",
            "create_by": [
                1801,
                "Nguyễn Ngọc Hải (IT)"
            ],
            "activity_ids": [],
            "activity_state": false,
            "activity_user_id": false,
            "activity_type_id": false,
            "activity_date_deadline": false,
            "activity_summary": false,
            "activity_exception_decoration": false,
            "activity_exception_icon": false,
            "message_is_follower": false,
            "message_follower_ids": [
                185706
            ],
            "message_partner_ids": [
                513277
            ],
            "message_channel_ids": [],
            "message_ids": [
                377899
            ],
            "message_unread": false,
            "message_unread_counter": 0,
            "message_needaction": false,
            "message_needaction_counter": 0,
            "message_has_error": false,
            "message_has_error_counter": 0,
            "message_attachment_count": 0,
            "message_main_attachment_id": false,
            "website_message_ids": [],
            "message_has_sms_error": false,
            "display_name": "CTKM NHA KHOA",
            "create_uid": [
                1801,
                "Nguyễn Ngọc Hải (IT)"
            ],
            "create_date": "2021-07-28T02:20:22.695074",
            "write_uid": [
                1801,
                "Nguyễn Ngọc Hải (IT)"
            ],
            "write_date": "2021-07-28T02:20:22.695074",
            "__last_update": "2021-07-28T02:20:22.695074"
        }
    ]

* **Lỗi:**

  * _Lỗi đăng nhập không thành công_ <br />
    **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`
