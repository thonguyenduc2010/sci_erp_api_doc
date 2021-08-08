
***1.4 Danh bảng giá***
----

* **URL**

    `GET` Danh sách bảng giá: 
    `/{domain}/api/v1/price-list`
  
    `GET` Chi tiết danh sách bảng giá theo ID: 
    `/{domain}/api/v1/price-list/<id>`
    
    `GET` Chi tiết thông tin dịch vụ trong bảng giá: 
    `/{domain}/api/v1/price-list-item`
  
    `GET` Chi tiết thông tin dịch vụ trong bảng giá theo ID: 
    `/{domain}/api/v1/price-list-item/<id>`

    `GET` Chi tiết thông tin dịch vụ trong bảng giá theo ID bảng giá: 
    `/{domain}/api/v1/price-list-item/<price_list_id>`
  
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
      

* **Lỗi:**

  * _Lỗi đăng nhập không thành công_ <br />
    **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`
