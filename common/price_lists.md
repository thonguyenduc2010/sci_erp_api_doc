
***1.4 Danh bảng giá***
----

* **URL**

    
    /{domain}/api/v1/price-list


* **Method:**

  
    `GET`

* **Url Params**


  | Method | Attribute| Type | Description |
  |---|---|---|---|
  | `GET` | code | string  | Mã bảng giá |
  | `GET` | company| string  | Mã cơ sở y tế |
  | `GET` | brand| string  | Mã thương hiệu |


* **Phản hồi thành công:**
    * **Code:** 200 <br />
    * **Content:** <br />
    `{` <br />
	`'id': 12,`  <br />
	`'code': None,`  <br />
   ` 'name': 'Bảng giá niêm yết Paris 2021',` <br />
	`'start_date': 2021-01-01,` <br />
	`'end_date': 2021-12-31,` <br />
	`'type': 'service',` <br />
    `} `<br />
      

* **Lỗi:**

  * _Lỗi đăng nhập không thành công_ <br />
    **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`
