
***1.2 Danh sách dịch vụ***
----

* **URL**

    
    /{domain}/api/v1/services


* **Method:**

  
    `GET`

* **Url Params**


  | Method | Attribute| Type | Description |
  |---|---|---|---|
  | `GET` | code | string  | Mã dịch vụ |
  | `GET` | company| string  | Mã cơ sở y tế |
  | `GET` | brand| string  | Mã thương hiệu |


* **Phản hồi thành công:**
    * **Code:** 200 <br />
    * **Content:** <br />
    `{` <br />
	`'id': 28284,`  <br />
   ` 'code': 'KNPTBMM0001',` <br />
	`'name': 'Bấm mí Hàn Quốc',` <br />
    `} `<br />
      

* **Lỗi:**

  * _Lỗi đăng nhập không thành công_ <br />
    **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`
