
***1.2 Danh sách dịch vụ***
----
Trả về thông tin sản phẩm, dịch vụ của một bảng giá

* **URL**

    
   `GET` Lấy danh sách dịch vụ `/{domain}/api/v1/services`

   `GET` Lấy danh sách dịch vụ theo ID `/{domain}/api/v1/services/{id}`


* **Method:**

  
    `GET`

* **Url Params**

  | Attribute| Type | Description |
  |---|---|---|
  | company_id | Integer  | ID cơ sở |
  | pricelist_id | Integer  | ID bảng giá |


* **Phản hồi thành công:**
    * **Code:** 200 <br />
    * **Content:** <br />
  `GET` Lấy danh sách dịch vụ `/{domain}/api/v1/services`
```buildoutcfg
    {
        `"error": 0,
        "message": "Success",
        "count": 1411,
        "data": [
            {
                "id": 65491,
                "default_code": "DCPKCPK0003",
                "name": "Cắt chỉ khách bên ngoài mức độ 3 (hàm, ngực, mông, tạo hình thành bụng..)",
                "type": "service",
                "company": [
                    {
                        "id": 5,
                        "name": "THẨM MỸ VIỆN ĐÔNG Á KIM MÃ"
                    },
                    {
                        "id": 6,
                        "name": "THẨM MỸ VIỆN ĐÔNG Á HẢI PHÒNG"
                    },
                    {
                        "id": 7,
                        "name": "THẨM MỸ VIỆN ĐÔNG Á VINH"
                    },
                    {
                        "id": 8,
                        "name": "THẨM MỸ VIỆN ĐÔNG Á ĐÀ NẴNG"
                    },
                    {
                        "id": 9,
                        "name": "THẨM MỸ VIỆN ĐÔNG Á 3/2"
                    },
                    {
                        "id": 10,
                        "name": "THẨM MỸ VIỆN ĐÔNG Á BÌNH DƯƠNG"
                    },
                    {
                        "id": 11,
                        "name": "THẨM MỸ VIỆN ĐÔNG Á CẦN THƠ"
                    },
                    {
                        "id": 12,
                        "name": "BỆNH VIỆN THẨM MỸ ĐÔNG Á HỒ CHÍ MINH"
                    }
                ]
            },
            ...
        ]
    }
```
`GET` Lấy danh sách dịch vụ theo ID `/{domain}/api/v1/services/{id}`
```buildoutcfg
    {
        "error": 0,
        "message": "Success",
        "count": 1,
        "data": [
            {
                "id": 24,
                "code": "TBH01",
                "name": "Thể tích khối hồng cầu (hematocrit) bằng máy ly tâm",
                "type": "service"
            }
        ]
    }
```
* **Lỗi:**

  * _Lỗi đăng nhập không thành công_ <br />
    **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`
