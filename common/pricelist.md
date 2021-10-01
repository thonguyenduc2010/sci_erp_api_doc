
*** 1.5 Danh bảng giá ***
----
Trả về danh sách bảng giá thuộc thương hiệu (brand) mà token key gọi API. 
Các trường hợp không có thông tin về chi nhánh (company) là bảng giá áp dụng cho toàn bộ chi nhánh (company) thuộc thương hiệu (brand). Nếu có thông tin về company là áp dụng đích danh cho một chi nhánh thuộc thương hiệu đó.
* **URL**

    `GET` Danh sách bảng giá: 
    `/{domain}/api/v1/price-list`
  
    `GET` Danh sách bảng giá theo ID:
    `/{domain}/api/v1/price-list/<id>`
  

* **Method:**

    `GET`

* **Url Params**
  
  | Attribute| Type | Description |
  |---|---|---|
  | id | int  | ID bảng giá |
  | code | String  | Mã dịch vụ |

* **Phản hồi thành công:**
    * **Code:** 200 <br />
    * **Content:** <br />
  
`GET` Danh sách bảng giá: 
    `/{domain}/api/v1/price-list`
  
```buildoutcfg
    {
        "error": 0,
        "message": "Success",
        "count": 10,
        "data": [
            {
                "id": 15,
                "name": "Bảng giá Hàng Bán PARIS 2021",
                "type": "product",
                "currency_id": "VND",
                "brand": [
                    {
                        "id": 3,
                        "name": "Paris"
                    }
                ],
                "company": [
                    {
                        "id": false,
                        "name": false
                    }
                ]
            },
            {
                "id": 14,
                "name": "Bảng giá Hàng Bán ĐÔNG Á 2021",
                "type": "product",
                "currency_id": "VND",
                "brand": [
                    {
                        "id": 2,
                        "name": "Đông Á"
                    }
                ],
                "company": [
                    {
                        "id": false,
                        "name": false
                    }
                ]
            },
            ...
        ]
    }
```
`GET` Danh sách bảng giá theo ID:
  `/{domain}/api/v1/price-list/<id>`
```buildoutcfg
    {
        "error": 0,
        "message": "Success",
        "count": 1,
        "data": [
            {
                "id": 11,
                "name": "Bảng giá niêm yết Đông Á 2021",
                "type": "service",
                "currency_id": "VND",
                "brand": [
                    {
                        "id": 2,
                        "name": "Đông Á"
                    }
                ],
                "company": [
                    {
                        "id": false,
                        "name": false
                    }
                ]
            }
        ]
}
```
* **Lỗi:**

  * _Lỗi đăng nhập không thành công_ <br />
    **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`
