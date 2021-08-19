
***1.4 Danh bảng giá***
----

* **URL**

    `GET` Danh sách bảng giá: 
    `/{domain}/api/v1/price-list`
  
    `GET`Thông tin chi tiết bảng giá theo ID bảng giá: 
    `/{domain}/api/v1/price-list-items/<id>`
  
  
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
      
`GET` Thông tin chi tiết bảng giá theo ID bảng giá: 
`/{domain}/api/v1/price-list-items/<id>`


```buildoutcfg
  {
      "error": 0,
      "message": "Success",
      "count": 2,
      "data": [
          {
              "info_price_list": {
                  "priceList": {
                      "id": 11,
                      "name": "Bảng giá niêm yết Đông Á 2021"
                  },
                  "brand": {
                      "id": 2,
                      "name": "Đông Á"
                  },
                  "company": {
                      "id": false,
                      "name": false
                  }
              }
          },
          {
              "info_price_list_item": [
                  {
                      "id": 10953,
                      "product": {
                          "id": 68383,
                          "name": "Phụ thu 4"
                      },
                      "min_quantity": 0,
                      "currency_id": null,
                      "price": "100000.0 ₫",
                      "date_start": false,
                      "date_end": false
                  },
                  {
                      "id": 10952,
                      "product": {
                          "id": 68382,
                          "name": "Phụ thu 3"
                      },
                      "min_quantity": 0,
                      "currency_id": null,
                      "price": "50000.0 ₫",
                      "date_start": false,
                      "date_end": false
                  },
                  ...
              ]
          }
      ]
  }
```

* **Lỗi:**

  * _Lỗi đăng nhập không thành công_ <br />
    **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`
