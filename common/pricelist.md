
***1.4 Danh bảng giá***
----

* **URL**

    `GET` Danh sách bảng giá: 
    `/{domain}/api/v1/price-list`
  
    `GET` Chi tiết danh sách bảng giá theo ID: 
    `/{domain}/api/v1/price-list/<id>`
  
  
* **Method:**

    `GET`

* **Url Params**


  | Attribute| Type | Description |
  |---|---|---|
  | id | int  | ID bảng giá |


* **Phản hồi thành công:**
    * **Code:** 200 <br />
    * **Content:** <br />
  
`GET` Danh sách bảng giá: 
    `/{domain}/api/v1/price-list`
  
      
    "count": 2,
    "data": [
        {
            "id": 12,
            "name": "Bảng giá niêm yết Paris 2021",
            "brand_id": [
                3,
                "Paris"
            ],
            "start_date": false,
            "end_date": false,
            "type": "service"
        },
        {
            "id": 11,
            "name": "Bảng giá niêm yết Đông Á 2021",
            "brand_id": [
                2,
                "Đông Á"
            ],
            "start_date": false,
            "end_date": false,
            "type": "service"
        }]
      
`GET` Chi tiết danh sách bảng giá theo ID: 
`/{domain}/api/v1/price-list/<id>`


    "count": 1,
    "data": [
        {
            "id": 11,
            "name": "Bảng giá niêm yết Đông Á 2021",
            "active": true,
            "item_ids": [
                10953,
                10952,
                10951,
            ],
            "currency_id": [
                23,
                "VND"
            ],
            "company_id": false,
            "sequence": 1,
            "country_group_ids": [],
            "discount_policy": "with_discount",
            "website_id": [
                1,
                "My Website"
            ],
            "code": false,
            "selectable": true,
            "brand_id": [
                2,
                "Đông Á"
            ],
            "start_date": false,
            "end_date": false,
            "type": "service",
            "display_name": "Bảng giá niêm yết Đông Á 2021 (VND)",
            "create_uid": [
                6,
                "Admin KN666"
            ],
            "create_date": "2021-04-17T09:40:38.422577",
            "write_uid": [
                1827,
                "Nguyen Hai Dang"
            ],
            "write_date": "2021-07-09T01:49:15.901075",
            "__last_update": "2021-07-09T01:49:15.901075"
        }
    ]

* **Lỗi:**

  * _Lỗi đăng nhập không thành công_ <br />
    **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`
