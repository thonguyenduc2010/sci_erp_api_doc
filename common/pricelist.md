
***1.4 Danh bảng giá***
----

* **URL**

    `GET` Danh sách bảng giá: 
    `/{domain}/api/v1/price-list`
  
    `GET` Chi tiết danh sách bảng giá theo ID: 
    `/{domain}/api/v1/price-list/<id>`
    
    `GET` Chi tiết thông tin dịch vụ: 
    `/{domain}/api/v1/price-list-item`
  
    `GET` Chi tiết thông tin dịch vụ trong bảng giá theo ID: 
    `/{domain}/api/v1/price-list-item/<id>`

    `GET` Chi tiết thông tin dịch vụ trong bảng giá theo ID bảng giá: 
    `/{domain}/api/v1/price-list/price-list-item/<price_list_id>`
  
* **Method:**

  
    `GET`

* **Url Params**


  | Method | Attribute| Type | Description |
  |---|---|---|---|
  | `GET` | id | int  | ID bảng giá |
  | `GET` | brand| string  | ID thương hiệu |


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
            "company_id": false,
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
            "company_id": false,
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

`GET` Chi tiết thông tin dịch vụ: 
`/{domain}/api/v1/price-list-item`

    "count": 2,
        "data": [
            {
              "id": 10226,
              "product_id": [
                  63963,
                  "[PNCHNR0014] Niềng Răng Mắc Cài Pha Lê"
              ],
              "company_id": false,
              "fixed_price": 40000000.0,
              "date_start": false,
              "date_end": false
            },
            {
              "id": 10224,
              "product_id": [
                  63961,
                  "[PNCHNR0012] Niềng Răng Mắc Cài Kim Loại Thường mức độ khó (nhổ răng lệch lạc nhiều)"
              ],
              "company_id": false,
              "fixed_price": 40000000.0,
              "date_start": false,
              "date_end": false
            }]

`GET` Chi tiết thông tin dịch vụ trong bảng giá theo ID: 
`/{domain}/api/v1/price-list-item/<id>`

     "count": 1,
        "data": [
            {
                "id": 10224,
                "product_id": [
                    63961,
                    "[PNCHNR0012] Niềng Răng Mắc Cài Kim Loại Thường mức độ khó (nhổ răng lệch lạc nhiều)"
                ],
                "company_id": false,
                "fixed_price": 40000000.0,
                "date_start": false,
                "date_end": false
            }
        ]

`GET` Chi tiết thông tin dịch vụ trong bảng giá theo ID bảng giá: 
`/{domain}/api/v1/price-list/price-list-item/<price_list_id>`

    "count": 2,
    "data": [
        {
            "id": 10949,
            "product_id": [
                68383,
                "[DVKKHKHAC004] Phụ thu 4"
            ],
            "company_id": false,
            "fixed_price": 100000.0,
            "date_start": false,
            "date_end": false
        },
        {
            "id": 10948,
            "product_id": [
                68382,
                "[DVKKHKHAC003] Phụ thu 3"
            ],
            "company_id": false,
            "fixed_price": 50000.0,
            "date_start": false,
            "date_end": false
        }]

* **Lỗi:**

  * _Lỗi đăng nhập không thành công_ <br />
    **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`
